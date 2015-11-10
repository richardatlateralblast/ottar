![alt tag](https://raw.githubusercontent.com/richardatlateralblast/ottar/master/Freyja-and-Ottar.jpg)

OTTAR
=====

OVF Tools Tars and installers.

A Collection of VMware's OVF tools, including a tar of ovftools that can be used
for ESXi.

The tools can be downloaded from here:

https://my.vmware.com/group/vmware/details?downloadGroup=OVFTOOL410&productId=353#product_downloads

Creating OVF tar file for ESXi
------------------------------

```
# chmod +x /export/isos/VMware/6.0/VMware-ovftool-4.1.0-2459827-lin.x86_64.bundle 
# sh /export/isos/VMware/6.0/VMware-ovftool-4.1.0-2459827-lin.x86_64.bundle
# mkdir /tmp/ovf
# mkdir /tmp/ovf/tools
# mkdir /tmp/ovf/files
# rsync -au /usr/lib/vmware-ovftool/* /tmp/ovf/tools/
# sed -i 's/bash/sh/' /tmp/ovf/tools/ovftool
# cd /tmp
# tar cf vmware-ovftools.tar ovf
# gzip -9 vmware-ovftools.tar
```

