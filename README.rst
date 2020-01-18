Lumenera(r) USB Camera Interface
================================

Lucam is a Python library that provides two interfaces to the Lumenera(r)
LuCam API:

* **API**, a low level ctypes interface to the lucamapi.dll version 5,
  exposing the definitions/declarations found in the lucam.h C header.

* **Lucam**, a high level object interface wrapping most of the ctypes
  interface, featuring exception based error handling and numpy.array type
  images.

:Author:
  `Christoph Gohlke <https://www.lfd.uci.edu/~gohlke/>`_

:Organization:
  Laboratory for Fluorescence Dynamics. University of California, Irvine

:License: BSD 3-Clause

:Version: 2020.1.1

Requirements
------------
* `CPython >= 3.6 <https://www.python.org>`_
* `Numpy 1.14 <https://www.numpy.org>`_
* `Lumenera USB camera and drivers 5.0 <https://www.lumenera.com/>`_

Revisions
---------
2020.1.1
    Remove support for Python 2.7 and 3.5.
    Update copyright.

Notes
-----
"Lumenera" is a registered trademark of Lumenera Corporation (1).

Lucam is no longer being actively developed.

Lucam has been tested with the Lu165M monochrome camera on Windows only.

Some LuCam API functions are not available in the Lucam wrapper due to
lack of documentation or hardware for testing.

Naming of functions, methods, and constants that have an equivalent in
the LuCam API follows the LuCam API conventions, else PEP8 is followed.

References
----------
1. `Lumenera Corporation <https://www.lumenera.com/>`_
2. Lumenera USB Camera API Reference Manual Release 5.0. Lumenera Corporation.

Examples
--------
>>> from lucam import Lucam
>>> camera = Lucam()
>>> image = camera.TakeSnapshot()
>>> camera.SaveImage(image, 'test.tif')
>>> camera.CameraClose()

Refer to the test() function at the end of the module for more examples.
