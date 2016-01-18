What is Kolibre?
---------------------------------
Kolibre is a Finnish non-profit association whose purpose is to promote
information systems that aid people with reading disabilities. The software
which Kolibre develops is published under open source and made available to all
stakeholders at github.com/kolibre.

Kolibre is committed to broad cooperation between organizations, businesses and
individuals around the innovative development of custom information systems for
people with different needs. More information about Kolibres activities, association 
membership and contact information can be found at http://www.kolibre.org/

What is libkolibre-xmlreader?
---------------------------------
Libkolibre-xmlreader is a library for fetching and parsing XML data. 
It is a SAX wrapper library for libxml2. The library can load XML/XHTML/HTML-
documents from disk or http. A caching function is built in to speed up re-parsing 
of previous XML documents. It also has an optional dependency on libtidy, which 
can be used as a fallback for cleaning up messy and malformed XML files. 
These features makes the usage of xmlreader simple, fast and reliable.

Documentation
---------------------------------
Kolibre client developer documentation is available at 
https://github.com/kolibre/libkolibre-builder/wiki

This library is documented using doxygen. Generate documentation by executing

    $ ./configure
    $ make doxygen-doc

Platforms
---------------------------------
Libkolibre-xmlreader has been tested with Linux Debian Squeeze and can be built
using dev packages from apt repositories.

Dependencies
---------------------------------
Major dependencies for Kolibre-xmlreader:

* libxml2
* liblog4cxx
* libpthread
* libcurl
* libz
* libtidy (optional)

Building from source
---------------------------------
If building from GIT sources, first do a:

    $ autoreconf -fi

If building from a release tarball you can skip the above step.

    $ ./configure
    $ make
    $ make install

see INSTALL for detailed instructions.

Known issues
---------------------------------
There is currently a bug in libxml2 version 2.7.8 causing xml parsing to fail
when the document type declaration contains an empty internal subset declaration.
If this package is compiled with libtidy then tidy will remove the empty
declaration and thus work normally.

The bug has been reported to the libxml2 community along with a patch. Visit
https://bugzilla.gnome.org/show_bug.cgi?id=684201 to check the status of the bug
or download the patch.

Licensing
---------------------------------
Copyright (C) 2012 Kolibre

This file is part of libkolibre-xmlreader.

Libkolibre-xmlreader is free software: you can redistribute it and/or modify
it under the terms of the GNU Lesser General Public License as published by
the Free Software Foundation, either version 2.1 of the License, or
(at your option) any later version.

Libkolibre-xmlreader is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Lesser General Public License for more details.

You should have received a copy of the GNU Lesser General Public License
along with libkolibre-xmlreader. If not, see <http://www.gnu.org/licenses/>.

