# CLMDB

CLMDB is a SwiftPM package wrapper for [LMDB](http://www.lmdb.tech/doc/), a key-value database storage solution created for fast read and write processes. You can read more about this project at: <http://www.lmdb.tech/doc>.

This wrapper provides exposure of the library's C interfaces to Swift, allowing a Swift application or service to easily create, read, and manage database instances of LMDB.

Changes in LMDB will be pulled into this repository as the upstream project evolves. The LMDB repository is mirrored here: <https://github.com/LMDB/lmdb>.

## Changes to LMDB

Swift LMDB makes two local changes to LMDB in order to pass thread sanitization checks in [IndexStoreDB](https://github.com/swiftlang/indexstore-db). These changes are:
 - Use `_Atomic` instead of `volatile` for transaction types
 - Build with POSIX mutexes enabled and robust mutexes disabled on Linux and macOS

## License

The included LMDB database project is released under [The OpenLDAP Public License](https://git.openldap.org/openldap/openldap/-/blob/mdb.master/libraries/liblmdb/LICENSE). This same license applies to the Swift code included in this repository.
