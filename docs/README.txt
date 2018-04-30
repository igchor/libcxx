THIS REPO CONTAINS AN EXPERIMENT AND IS NOT APPROPRIATE FOR USE IN PRODUCTION.

The PMDK repo, at https://github.com/pmem/pmdk, contains a fully-validated
C++ API for persistent memory programming, described here:
	http://pmem.io/pmdk/cpp_obj/

To build on that, the experiment in this repo took the LLVM libcxx release 3.9
and attempted to modify it to be persistent memory aware.  The results are
interesting, but not complete enough to use as a production solution.  The code
is supplied here as a reference.  The strategy for STL-style containers is to
create persistent memory versions of the most useful containers over time and
add them to PMDK.


[original README from LLVM libcxx follows...]

libc++ Documentation
====================

The libc++ documentation is written using the Sphinx documentation generator. It is
currently tested with Sphinx 1.1.3.

To build the documents into html configure libc++ with the following cmake options:

  * -DLLVM_ENABLE_SPHINX=ON
  * -DLIBCXX_INCLUDE_DOCS=ON

After configuring libc++ with these options the make rule `docs-libcxx-html`
should be available.
