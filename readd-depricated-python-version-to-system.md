# Adding a new Python implementation

### Eclass and profile changes

When adding a new Python target, please remember to perform all the following tasks:

* add the new target flags to **`profiles/desc/python_targets.desc`** and **`python_single_target.desc`**.

* force the new implementation on **`dev-lang/python-exec`** via **`profiles/base/package.use.force`**.

* mask the new target flags on stable profiles via **`profiles/base/use.stable.mask`**.

* add the new target to **`_PYTHON_ALL_IMPLS`** and update the patterns in **`_python_impl_supported()`** in **`python-utils-r1.eclass`**.

* add the new implementation to the list in **`app-portage/gpyutils/files/implementations.txt`**.

# Resources

[Gentoo Wiki](https://dev.gentoo.org/~mgorny/python-guide/interpreter-maintenance.html)

[youtube](https://www.youtube.com/watch?v=9dM8bYvpWCc)
