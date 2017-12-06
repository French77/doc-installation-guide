Partitioning
============

Device and partition names
--------------------------

The Linux naming scheme for devices and partitions is simple but it can be confusing to novice users. If you are not familiar with it, please click `here <https://www.debian.org/releases/wheezy/amd64/apcs04.html.en>`_.

Filesystem and mount points
---------------------------

If you are not familiar with the Linux filesystem and the concept of mount points, please click `here <http://etutorials.org/Linux+systems/red+hat+linux+9+professional+secrets/Part+II+Exploring+Red+Hat+Linux/Chapter+7+Red+Hat+Linux+Basics/Understanding+the+Linux+File+System/>`_.

Dedicated /home partition
-------------------------

In Linux, the ``/home`` directory is used to store user data and preferences.

This directory usually contains one subdirectoy for each user account. So if your username is ``john``, your home directory is likely to be ``/home/john``, your downloads are likely to be in ``/home/john/Downloads``, your documents in ``/home/john/Documents``, your Firefox bookmarks somewhere in ``/home/john/.mozilla`` and so on...

By placing ``/home`` on its own dedicated partition, you separate the user data from the rest of the operating system.

The advantage is that you can wipe the operating system and replace it without affecting the user data.

When installing Linux Mint:

1. Assign the ``/`` mount point to the partition dedicated to the operating system, and tell the installer to format it.

2. Assign the ``/home`` mount point to the partition dedicated to the user data, and if it contains user data already, make sure to tell the installer **not to format it**.

.. warning::
    This is not recommended for novice users. A misstep during the installation could wipe all your data. Always make backups, make sure to select the right partitions and to carefully review formatting options.

.. note::
    A Linux Mint operating system roughly takes 15GB. Account for additional software and give it 50GB if you can spare the size. Keep most of your free space for your home partition, since your downloads, videos, pictures and user data is what will take the biggest amount of space.
