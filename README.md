# gcsee-testdata

## Introduction

Test assets for [GCSee](https://github.com/kcpeppe/gcsee). This collection of files is unlikely to change other than an occasional
addition.

---
NOTE

This project relies on [Git Large File Storage (LFS)](https://git-lfs.github.com/) to store log files that
exceed the GitHub file size limit. Please make sure you have this installed for your local system before working
with this repository (including cloning it).

---

## Getting Started

This test data is used by [gcsee](https://github.com/kcpeppe/gcsee).

When the Maven test phase is run in GCSee, the test data assets are downloaded as a zip file, which is then unzipped and used in the GCSee unit tests.

## Cloning the Repository

To add test artifacts (GC logs) to this repository you should first clone it. *WARNING* Please note that it relies on [Git Large File Storage (LFS)](https://git-lfs.github.com/). 

Consider cloning with a `--depth=1` to reduce the size. This will only clone the last commit.
Make sure you have `git-lfs` installed, and then perform the following commands after a successful `git clone`.

```bash
cd gcsee-testdata
git reset --hard
git lfs install
git lfs pull
```
## Adding Test Data

The GC logs sit in directories who's path helps identify and categorize the data contained in the log. For example, the gc1gc_details_adaptivesizing_reset.log is a JDK 8 G1GC log that contains adaptive sizing and RSet information. It resides in the gclogs/preunified/details/adaptivesize/rset directory.
This convention should be used when adding a new GC log. Additionally, please choose a name that annonimizes the source of the data and ensure that the log file contains no data that would allow one to trace it back to its source.


## Contributing

This project welcomes contributions and suggestions that you have the right to grant us the rights to use your contribution.
