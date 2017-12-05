Verify your ISO image
=====================

It is important to verify the integrity and authenticity of your ISO image before using it to install Linux Mint.

The integrity check confirms that your ISO image was properly downloaded and that your local file is an exact copy of the file present on the download servers. An error during the download could result in a corrupted file and trigger random issues during the installation.

The authenticity check confirms that the ISO image you downloaded was signed by Linux Mint, and thus that it isn't a modified or malicious copy made by somebody else.

Download the SHA256 sums provided by Linux Mint
-----------------------------------------------

All `download mirrors <https://www.linuxmint.com/mirrors.php>`_ provide the ISO images, a ``sha256sum.txt`` file and a ``sha256sum.txt.gpg`` file. You should be able to find these files in the same place you downloaded the ISO image from.

If you are unable to find them, you can browse `this mirror <https://ftp.heanet.ie/mirrors/linuxmint.com/stable/>`_ and select the version corresponding to the Linux Mint release you downloaded.

Download both the ``sha256sum.txt`` and the ``sha256sum.txt.gpg`` files. These two files are used to check the integrity and authenticity of your ISO image.

Integrity check
---------------

To check the integrity of your local ISO file, generate its SHA256 sum and compare it with the sum present in the ``sha256sum.txt`` file.

.. code-block:: console

    sha256sum -b yourfile.iso

.. hint::
    If you are using Windows you can get the sha256sum (and gpg) command utility by installing `Cygwin <http://www.cygwin.com/>`_.

If the sums match, your file was successfully downloaded. If they don't, download it again.

.. hint::
    Choose a different download server if this check keeps failing.


`````

Authenticity check
------------------

To verify the authenticity of the ``sha256sum.txt`` file, we need to check the signature on the ``sha256sum.txt.gpg`` file.

Import the Linux Mint signing key:
``````````````````````````````````
.. code-block:: console

   gpg --keyserver keyserver.ubuntu.com --recv-key "27DE B156 44C6 B3CF 3BD7  D291 300F 846B A25B AE09"

.. note::
    If gpg complains about the key ID, try the following commands instead:

    .. code-block:: console

        gpg --keyserver keyserver.ubuntu.com --recv-key A25BAE09
        gpg --list-key --with-fingerprint A25BAE09

    Check the output of the last command, to make sure the fingerprint is ``27DE B156 44C6 B3CF 3BD7 D291 300F 846B A25B AE09``.

Verify the authenticity of the sha256sum.txt file:
``````````````````````````````````````````````````
.. code-block:: console

    gpg --verify sha256sum.txt.gpg sha256sum.txt

The output of the last command should tell you that the file signature is 'good' and that it was signed with the following key: ``A25BAE09``.

.. note::
    Unless you trusted the Linux Mint signature in the past, or a signature which trusted it, GPG should warn you that the Linux Mint signature is not trusted. This is expected and perfectly normal.

.. hint::
    For more information on ISO verification, or to verify BETA, LMDE or old releases, please click `here <https://linuxmint.com/verify.php>`_.
