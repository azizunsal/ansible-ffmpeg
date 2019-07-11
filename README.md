ffmpeg
=========

This role can be used to install FFmpeg [static builds](https://johnvansickle.com/ffmpeg/) created by John Van Sickle.

Requirements
------------

None.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

```yaml
ffmpeg_download_type: git # git or release
ffmpeg_version: "{{ 4.14 if ffmpeg_download_type=='release' else 20190701 }}"
```

You just need to change `ffmpeg_version`.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yml
- hosts: servers
  roles:
    - azizunsal.ffmpeg
```

License
-------

BSD

Author Information
------------------

[Aziz Unsal](https://azizunsal.github.io/blog/)
