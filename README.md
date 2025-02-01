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

MIT

Author Information
------------------

[https://github.com/waal70]
