Create the bootable media
=========================

The easiest way to install Linux Mint is with a bootable USB stick.

Alternatively, if you do not have a spare USB stick or if your computer cannot boot from USB, you can create a bootable DVD.

How to make a bootable USB stick
--------------------------------

Using Linux Mint
````````````````

In Linux Mint, right-click the ISO file and select ``Make Bootable USB Stick``, or launch the ``USB Image Writer`` from the application menu.

.. figure:: images/mintstick.png
    :width: 500px
    :align: center

    Using the USB Image Writer in Linux Mint

Select your USB device and press the ``Write`` button.

Using Windows, Mac, or other Linux distributions
````````````````````````````````````````````````

Download `Etcher <https://etcher.io/>`_, install it and run it.

.. figure:: images/etcher.png
    :width: 500px
    :align: center

    Using Etcher

Press the ``Select image`` button and select your ISO file.

Press the ``Select drive`` button and select your USB stick.

Press the ``Flash!`` button.


How to make a bootable DVD
--------------------------

Optical discs are slow and burning to disc is prone to errors.

.. warning::
	Make sure to burn at the lowest possible speed to prevent issues.

.. warning::
	Make sure to burn the ISO onto the DVD, and not into the DVD. When finished, you shouldn't obtain a DVD which contains a single .iso file, but a DVD which contains all the files present within the ISO image (``boot/``, ``casper/``, etc..).

Using Linux
```````````
In Linux, install and use ``xfburn``.

Using Windows
`````````````
In Windows, right-click the ISO file and select ``Burn disk image``.

Select ``Verify disc after burning`` to make sure the ISO was burned without any errors.

Using Mac
`````````
In Mac OS, right-click the ISO file and select ``Burn Disk Image to Disc``.
