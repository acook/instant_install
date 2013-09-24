Instant Install
===============

Wrapper for stupid package managers.

Usage
-----

~~~sh
inin download package       # download package file

inin install package        # install package by name
inin install ./package.deb  # install package from file

inin refresh                # get latest package list

inin upgrade                # upgrade most outdated packages without getting all crazy
inin upgrade --all          # upgrade all outdated packages, getting crazy in the process
inin upgrade package        # upgrade just this one package
inin upgrade --deps package # upgrade just this package and its dependencies
~~~
