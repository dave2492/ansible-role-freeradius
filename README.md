Freeradius
==========

Install and configure freeradius with MySQL on debian 9 based on [documentation](https://wiki.freeradius.org/guide/SQL-HOWTO-for-freeradius-3.x-on-Debian-Ubuntu)

Requirements
------------

None

Role Variables
--------------


Dependencies
------------


Example Playbook
----------------
Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - uspdev.freeradius

Some checks:
------------

    insert into radcheck (username,attribute,op,value) values("maria", "Cleartext-Password", ":=", "m123");
    radtest maria m123 localhost 0 mysecret
    tail -f /var/log/freeradius/radius.log

