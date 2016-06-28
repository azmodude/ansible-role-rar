ansible-role-rar
================

Install [rar](http://www.rarlab.com/) onto a Linux host.

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

    install_path: "/usr/local/bin"

Install rar and unrar into this destination path.

    arch: "x64"

Install rar for this target architecture.
Available: 'x64' and 'i32'.

    version: "5.4.b2"

Install this version.

    url_x64: "http://www.rarlab.com/rar/rarlinux-x64-{{version}}.tar.gz"
    url_i32: "http://www.rarlab.com/rar/rarlinux-{{version}}.tar.gz"

Fetch rar archive from this location.

    sha256sum_x64: ed14c9dafab6a516b258914ddaa55f71b95599e0c6653e50c70020b0442091bb
    sha256sum_i32: 0519c083e5b503ff581f3ae3cb6415b8efbe74800762f04b3ccb6735543e544e

SHA256sums for the fetched archives.


Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      vars_files:
        - vars/main.yml
      roles:
         - { role: azmodude.rar }

License
-------

BSD

Author Information
------------------

None.
