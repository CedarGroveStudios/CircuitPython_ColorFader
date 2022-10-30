Introduction
============




.. image:: https://img.shields.io/discord/327254708534116352.svg
    :target: https://adafru.it/discord
    :alt: Discord


.. image:: https://github.com/CedarGroveStudios/CircuitPython_ColorFader/workflows/Build%20CI/badge.svg
    :target: https://github.com/CedarGroveStudios/CircuitPython_ColorFader/actions
    :alt: Build Status


.. image:: https://img.shields.io/badge/code%20style-black-000000.svg
    :target: https://github.com/psf/black
    :alt: Code Style: Black

A CircuitPython helper for brightness and gamma adjustment of an integer RGB
color value. Gamma is optionally applied after the brightness calculation.
Transparency is preserved. Returns an adjusted integer color value.
To adjust a ``displayio`` palette or multiple color list, use the
``cedargrove_palettefader.PaletteFader`` class.

Dependencies
=============
This driver depends on:

* `Adafruit CircuitPython <https://github.com/adafruit/circuitpython>`_

Please ensure all dependencies are available on the CircuitPython filesystem.
This is easily achieved by downloading
`the Adafruit library and driver bundle <https://circuitpython.org/libraries>`_
or individual libraries can be installed using
`circup <https://github.com/adafruit/circup>`_.

Installing to a Connected CircuitPython Device with Circup
==========================================================

Make sure that you have ``circup`` installed in your Python environment.
Install it with the following command if necessary:

.. code-block:: shell

    pip3 install circup

With ``circup`` installed and your CircuitPython device connected use the
following command to install:

.. code-block:: shell

    circup install cedargrove_colorfader

Or the following command to update an existing version:

.. code-block:: shell

    circup update

Usage Example
=============

Scale a 24-bit RGB source color value in proportion to the brightness setting
(0 to 1.0). The adjusted color's gamma value is typically from 0.0 to 2.0 with
a default of 1.0 for no gamma adjustment. Returns an adjusted 24-bit RGB color
value or None if the source color is None (transparent).

.. code-block:: python

    >>> from cedargrove_colorfader import color_fader
    >>> # Dim a pure red color to 50%; no gamma adjustment
    >>> print(hex(color_fader(source_color=0xFF0000, brightness=0.5, gamma=1.0)
    0x7f0000


Documentation
=============
API documentation for this library can be found `here <https://circuitpython-colorfader.readthedocs.io/>`_.

For information on building library documentation, please check out
`this guide <https://learn.adafruit.com/creating-and-sharing-a-circuitpython-library/sharing-our-docs-on-readthedocs#sphinx-5-1>`_.

Contributing
============

Contributions are welcome! Please read our `Code of Conduct
<https://github.com/CedarGroveStudios/CircuitPython_ColorFader/blob/HEAD/CODE_OF_CONDUCT.md>`_
before contributing to help this project stay welcoming.
