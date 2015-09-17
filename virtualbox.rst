virtualbox
==========

* Convert a VMDK to VDI:

    .. code-block:: console

        $ VBoxManage clonehd -format VDI /path/to/disk.vmdk /path/to/disk.vdi
