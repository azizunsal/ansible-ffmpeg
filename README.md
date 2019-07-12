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
ffmpeg_version: 20190701  # If `ffmpeg_download_type` set to `git` then use ` 20190701` pattern otherwise use the desired release number like 4.1.4, 3.3.4 etc.
```

You just need to change `ffmpeg_version`.

Dependencies
------------

None.

Example Playbook
----------------

For `git master` build:

```yml
- hosts: servers
  roles:
    - role: azizunsal.ffmpeg
      ffmpeg_download_type: git
      ffmpeg_version: 20190701
```

For any `release`:

```yml
- hosts: servers
  roles:
    - role: azizunsal.ffmpeg
      ffmpeg_download_type: release
      ffmpeg_version: 4.1.4
```

License
-------

BSD

Author Information
------------------

[Aziz Unsal](https://azizunsal.github.io/blog/)
