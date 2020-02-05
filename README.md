# XT862
A project using Android Debug Bridge (ADB) with the Droid 3.

###### Things Already Attempted for root access
Exploit found [here.](http://vulnfactory.org/blog/2011/08/25/rooting-the-droid-3/)
```
mv /data/local/12m /data/local/12m.bak
ln -s /data /data/local/12m
```
(reboot device)
```
rm /data/local/12m
mv /data/local/12m.bak /data/local/12m
mv /data/local.prop /data/local.prop.bak
```

shell@solana $ Permission Denied.
Next steps of this exploit are below when local.prop can be moved.

```
echo "ro.sys.atvc_allow_netmon_usb=0" > /data/local.prop
echo "ro.sys.atvc_allow_netmon_ih=0" >> /data/local.prop
echo "ro.sys.atvc_allow_res_core=0" >> /data/local.prop
echo "ro.sys.atvc_allow_res_panic=0" >> /data/local.prop
echo "ro.sys.atvc_allow_all_adb=1" >> /data/local.prop
echo "ro.sys.atvc_allow_all_core=0" >> /data/local.prop
echo "ro.sys.atvc_allow_efem=0" >> /data/local.prop
echo "ro.sys.atvc_allow_bp_log=0" >> /data/local.prop
echo "ro.sys.atvc_allow_ap_mot_log=0" >> /data/local.prop
echo "ro.sys.atvc_allow_gki_log=0" >> /data/local.prop
```
Did not work.
