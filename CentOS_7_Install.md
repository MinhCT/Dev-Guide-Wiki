## This guide will help you easily set up your CentOS 7, works on both host and virtual machine

1. First, download the iso file [here](http://isoredirect.centos.org/centos/7/isos/x86_64/) - you can choose the DVD file (around 4.4 GB) for faster installation.
2. Boot the ISO file up through USB, or use a virtual machine (I prefer this way).
3. Go through the installation step, including user creation.
4. After the installation has finished, the system will reboot.
5. Enter root credentials.
6. Now the tricky part, after login, run: `yum update`.


   **Note**: For some reason, you may get error: "yum update could not resolve host mirrorlist.centos.org" . Go to step 7 to fix this.
7. [Optional] Run the following command:


      `vi /etc/sysconfig/network-scripts/ifcfg-ens33`.
 
8. [Optional] Change the last line to: `ONBOOT=yes`. Save and close the file.
9. [Optional] Now run: `dhclient`.
10. [Optional] Try running `yum install` again, it should now update your CentOS system!
