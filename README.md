# vcpkg-cmake-cpp-template
This is a C++ GitHub template for getting up and running with C++ quickly using CMake for build automation and vcpkg for C++ package management.

## How to compile

...

## How to run & API reference

...

## Development

...

### Branching strategy

1. **`devel`** - development and experiments, might be inconsistent or broken regularly. Consistent, and fully functional changes from the branch `devel` might be merged into the branch `testing`. The `devel` branch is expected to be broken from time to time (e.g. when working on larger changes "per partes" or experimenting). New changes are usually pushed to the `devel` branch directly, however, very large changes can have an individual feature branch.
2. **`testing`** - shouldn't be broken or inconsistent most of the time. This branch has changes from `devel` queued to be accepted to the `stable` branch (or rejected). If a change is rejected from `testing` it will be dropped via a commit into `devel` that will be fast-forward merged to the `testing` branch again.
3. **`stable`** - tested, stable, useful, production-ready, and not expected to change more than a few times a year.
4. **`feature-<name of the feature>`** - all feature branches should be branched off and merged to `devel`. Features and bugfixes of `testing`, or `stable` should always go through the `devel` branch first (following the change workflow below).
5. **`archived/<branch-name>-<YYYY-MM-DD>`** - archived branches e.g. before a `push --force`.

### Change workflow

```text
                    functional &         tested, stable, useful
    impl.            consistent**          & production-ready
O---------> devel ---------------> testing -----------------> stable
|             ∧    ff-only merge             ff-only merge
| impl.       |
|             |
+-----> feature-branch
 large
 change
```

## TODOs

- empty
