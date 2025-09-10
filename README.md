waal70.tftp
=========

Installs tftp to host the trivial FTP server in order to enable network booting.  
It will download the Debian netboot image, and place it into the appropriate folder for the tftp-server.  
It will configure the netboot image, in order to set some defaults, SAY things to the user and use a preseed.cfg for Debian installs.  
If requested, it will purge the pihole adlist database and repopulate, using mongodb commands.

Requirements
------------


Role Variables
--------------

Maximum age of the netboot image. If the currently installed netboot image is older than this, it will re-download  

    netboot_max_age: "98d"  
    netboot_url: ["https://deb.debian.org/debian/dists/bookworm/main/installer-amd64/current/images/netboot/netboot.tar.gz"]  

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - waal70.tftp

License
-------

[GPLv3](https://www.gnu.org/licenses/gpl-3.0.html#license-text)

Author Information
------------------

Unless otherwise noted, this entire repository is (c) 2024 by André (waal70). [See github profile](https://github.com/waal70)

Please contact me if you need a commercial license for any of these files
