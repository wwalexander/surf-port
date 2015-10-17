surf-port
=========

A patch for FreeBSD's `www/surf` port that adds a necessary runtime dependency

About
-----

The `www/surf` port in FreeBSD's port system requires `x11/xprop` to be
installed in order for the search-bar and URL-bar to function. `Makefile.patch`
adds `xprop` as a runtime dependency in the `surf` port's `Makefile`.

Usage
-----

If `surf` is already installed, in `${PORTSDIR}/www/surf`, run `make deinstall`,
then run `patch < Makefile.patch` and reinstall the port.
