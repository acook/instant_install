Instant Install
===============

Wrapper for stupid package managers (all of them).

Usage
-----

~~~sh
usage: inin command [options]
	unified and simplified cross-distro and cross-platform package management

commands:
	inin (d)own(l)oad		# download a package without installing it
	inin (fi)les			# list the files from a named package
	inin (f)i(n)d			# find which package provides given file (some can only search installed packages)
	inin i(nf)o			# display description for package
	inin (in)stall			# install a package
	inin (re)fresh			# get latest package list (may also upgrade package manager itself)
	inin (r)e(m)ove			# remove and uninstall package
	inin (se)arch			# search for a package by name
	inin (up)grade			# upgrade all outdated packages

in progress:
	inin search --all package   # TODO: find a package by looking in description and tag fields as well
	inin search --regex "^pack" # TODO: find a package by regex
	inin install ./package.deb  # TODO: install package from local file
	inin upgrade package        # TODO: upgrade just this one package to the latest without touching depdendencies
	inin upgrade --deps package # TODO: upgrade just this package and its dependencies
	inin -m eopkg               # TODO: specify a package manager (for when multiple are available)
	more package managers       # TODO: scoop (Windows), pkgman (Haiku), others...

Feel free to add your own OS/distro or missing functionality:
	https://github/com/acook/instant_install

~~~
