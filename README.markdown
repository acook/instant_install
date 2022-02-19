Instant Install
===============

Simple script that lets you use the same set of commands for all(-ish) package managers, regardless of distro or OS.

Every package manager has its own quirks and weird edge cases and forgettable syntax for common operations. This is my attempt to streamline that inconsistency since I use so many different systems all the time.

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

Supported Package Managers
--------------------------

Package manager listed with its command coverage and notes:

- eopkg [complete]
- apt/apt-get [complete - will use apt over apt-get if possible, will install apt-file as needed automatically]
- homebrew [nearly complete]
- pacman [nearly complete - inin is essential unless you enjoy googling basic functions]
- emerge [only updating - the most ridiculous task to get right]

I haven't used an RPM-based system in ages, which is why its omission is glaringly obvious. Pull requests accepted!

This script uses a couple bashisms and invokes bash on its shebang line. A pure d/a/sh version would be great, I just haven't gotten around to testing it. Works on every version of bash released this millenium and probably beyond.
