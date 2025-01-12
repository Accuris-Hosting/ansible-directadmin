Ansible-directadmin
=========

Deploy [DirectAdmin](https://directadmin.com/) with Ansible

Requirements
------------

- A DirectAdmin license is required.
- A clean machine is required. DirectAdmin will actively overwrite existing packages.
- A publicly reachable IP is required.
- Root access to the target machine is required. For details, read: [Step 3](https://www.directadmin.com/installguide.php)

Ansible 2.1 is highly recommended.

Role Variables
--------------

Its recommended that you use either the `group_vars` / `host_vars` to set the required variables per server:

    directadmin_client_id:
    directadmin_license_id:
    directadmin_hostname:
    directadmin_ip_address:

If you wish to use a custom custombuild configuration, please configure:

    directadmin_custombuild_options_conf: http://yourdomain.com/options.conf

Dependencies
------------

As of present there are no dependent roles. (They may be added later)

Recommended to have installed on your server are:

    - Firewall
    - SSH protection (Fail2Ban)
    - Kernel hardening

FreeBSD support may be added later.

Example Playbook
----------------

    - hosts: localhost
      become: yes
      roles:
         - ansible-directadmin

License
-------

MIT

Author Information
------------------
Peter Potvin <peter.potvin@accurishosting.ca>

Original Author: Gerben Geijteman <gerben@hyperized.net>
