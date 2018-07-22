tz2js
=====

IANA timezone database parser.
Intended for and will produce a native javascript data structure.

The javascript data structure is destined for use within an interpreter
without disk or network access.  All script content must be contained
within the initial file used at execution time.

This can also be used as a module to return python dicts to process 
however you'd like.

References:
http://www.iana.org/time-zones


License
=======

The MIT License (MIT)

Copyright (c) 2013 Carlos (nzlosh@yahoo.com)

Permission is hereby granted, free of charge, to any person obtaining a
copy of this software and associated documentation files (the "Software"),
to deal in the Software without restriction, including without limitation
the rights to use, copy, modify, merge, publish, distribute, sublicense,
and/or sell copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included
in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS
OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL
THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.


Installation
============

  * Requirements
    * Python 2.7 or Python 3
    * IANA tz data archive

  1 Download the IANA timezone data archive file.
    > wget 'http://www.iana.org/time-zones/repository/releases/tzdb-2018e.tar.lz'
    > new ones are released every few months

  2 Extract the archive to your desired directory.
    > mkdir /tmp/tzdb-2018e

    > tar xzvf tzdb-2018e.tar.gz /tmp/tzdb-2018e

Usage
============
For js data structures, execute tz2js.py with tzdata's directory as an argument:

   
    > python tz2js.py /tmp/tzdb-2018e

Or in your python code:
```
import tz2js
...
tz2js.tzpath = '/tmp/tzdb-2018e'
data = tz2js.parseZoneFile()
...

```

Thanks to ...
=============

The group of people who maintain the extremely detailed and
complex timezone database.  Great work people!
