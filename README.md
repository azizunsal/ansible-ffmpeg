ffmpeg
=========

This role can be used to install FFmpeg [static builds](https://johnvansickle.com/ffmpeg/) created by John Van Sickle.

Requirements
------------

None.

Role Variables
--------------

```yaml
ffmpeg_download_type: git # git or release
ffmpeg_version: 20190701  # If `ffmpeg_download_type` set to `git` then use ` 20190701` pattern otherwise use the desired release number like 4.1.4, 3.3.4 etc.
```

For the other *generated* variables please take a look `vars/main.yml` and the defaults are in `defaults/main.yml`

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
