# Instructions

## Required

```bash
conda install conda-build anaconda-client
```

## Building and pushing to https://anaconda.org/prody

```bash
conda build . --no-anaconda-upload
PACKAGE_OUTPUT=`conda build . --output`
anaconda login
anaconda upload --user prody $PACKAGE_OUTPUT
conda build purge
anaconda logout
```

## Installing from conda

```
conda install -c prody prody
```

## Additional Info
https://docs.anaconda.com/anaconda-cloud/user-guide/tasks/work-with-packages

