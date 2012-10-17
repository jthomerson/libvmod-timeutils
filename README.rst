==============
vmod_timeutils
==============

-------------------------
Varnish Time Utils Module
-------------------------

:Manual section: 3
:Author: Jeremy Thomerson
:Date: 2012-10-17
:Version: 0.1

SYNOPSIS
========

TODO: enter documentation here

DESCRIPTION
===========

Varnish Module (vmod) that assists with date-related functions in VCL,
including manipulation of date-formatted headers.  For instance, if you
always want to add a specific amount of time to an Expires header, this
module provides an easy way to do so.

FUNCTIONS
=========

TODO: enter VCL examples here

version
-------

Prototype
        timeutils.version()
Returns
        string
Description
        Returns the string constant version-number of the timeutils vmod.
Example
        ``set resp.http.X-timeutils-version = timeutils.version();``


INSTALLATION
============

Installation requires the Varnish source tree (only the source matching the
binary installation).

1. `./autogen.sh`  (for git-installation)
2. `./configure VARNISHSRC=/path/to/your/varnish/source/varnish-cache`
3. `make`
4. `make install` (may require root: sudo make install)
5. `make check` (Optional for regression tests)

VARNISHSRCDIR is the directory of the Varnish source tree for which to
compile your vmod. Both the VARNISHSRCDIR and VARNISHSRCDIR/include
will be added to the include search paths for your module.

Optionally you can also set the vmod install dir by adding VMODDIR=DIR
(defaults to the pkg-config discovered directory from your Varnish
installation).


ACKNOWLEDGEMENTS
================

This plugin was heavily influenced by two modules developed by the Varnish team:
vmod_header and vmod_example.

Author: Jeremy Thomerson <jeremy@thomersonfamily.com>, Expert Tech Services, LLC

HISTORY
=======

Version 0.1: Initial version, testing my first vmod ever.

BUGS
====

I'm sure there will be some.  Leaving this as a placeholder to document them.

SEE ALSO
========

* varnishd(1)
* vcl(7)
* https://github.com/jthomerson/libvmod-timeutils

COPYRIGHT
=========

This document is licensed under the same license as the
libvmod-timeutils project. See LICENSE for details.

* Copyright (c) 2012 Jeremy Thomerson, Expert Tech Services, LLC
