eigenbahn.plan9port
=========

Install [Plan 9 from User Space](https://9fans.github.io/plan9port/) (aka **plan9port**) from source.


Requirements
------------

Any Unix-like operating system with a graphical server and essential build tools.


Role Variables
--------------

The main variables are:

 - `plan9port_version`: Version / commit to install, defaults to `HEAD`.
 - `plan9port_install_location`: Whre the root plan9port directory gets installed, defaults to `/usr/local/plan9`.

 Please note that the role has a mechanism to not skip all tasks if one of the binaries (`rio`) is found on the system.

If for any reason you'd like to re-install it (e.g. due to upstream changes in the code) you can force the reinstallation by setting var `plan9port_force_reinstall` to `yes`.


Dependencies
------------

None.


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: eigenbahn.plan9port }


License
-------

MIT


Author Information
------------------

Jordan Besly [@p3r7](https://github.com/p3r7) ([blog](https://www.eigenbahn.com/)).
