System snapshots
================

Before you start using your operating system, set up system snapshots. Then if anything goes wrong, you can restore your system from an earlier backup.

1. Launch :menuselection:`Menu --> Administration --> Timeshift`.

2. Select ``RSYNC`` and click :guilabel:`Next`.

.. figure:: images/timeshift-1.png
    :align: center

3. Select the device where you want system snapshots to be saved and click :guilabel:`Next`.

.. figure:: images/timeshift-2.png
    :align: center

.. note::
    The selected device is not formatted and no data is lost. System snapshots are saved into a newly created ``timeshift`` directory on the root of the selected device.

4. Select when system snapshots are saved.

.. figure:: images/timeshift-3.png
    :align: center

.. note::
    System snapshots are incremental so although the first snapshot takes a significant amount of spaces, new snapshots only take additional space for files which have changed.

.. note::
    ``Boot`` snapshots are performed in the background and do not impact the speed of the boot sequence.

5. Click :guilabel:`Finish`.

.. figure:: images/timeshift-4.png
    :width: 500px
    :align: center