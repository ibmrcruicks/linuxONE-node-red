# linuxONE-node-red

## setup
+ need nodejs8 as nodejs10+ requires gcc-c++ >=4.9 -- not currently available
+ for Db2 support, either ibmdb2, or dashdb, need XLC/C++ Runtime
  + https://www-01.ibm.com/support/docview.wss?uid=swg24041489#DNLD
  + download tarball with rhel and sles rpms
  + install
  + copy /opt/ibm/lib/libibmc++.so.1 /usr/lib
  + copy /opt/ibm/lib64/libibmc++.so.1 /usr/lib64

## remote access
if using the Marist hosting environment [LineONE Community Cloud](https://linuxone.cloud.marist.edu/cloud/#/index), firewall rules prevent direct access from the outside; use an ssh tunnel instead -
```
  ssh -L 8888:<marist-instance-ip>:1880 -i <marist-key>.pem linux1@<marist-instance-ip>
```
