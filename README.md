ffmpeg
=========

This role can be used to install FFmpeg [static builds](https://johnvansickle.com/ffmpeg/) created by John Van Sickle.

Requirements
------------

None.

Role Variables
--------------

```yml
ffmpeg_download_channel: builds # builds | release | old-releases

# Use `20190701` like pattern when `ffmpeg_download_channel` is set to `builds`.
# Use the last release from https://johnvansickle.com/ffmpeg/ when `ffmpeg_download_channel` is set to `release`.
# Use `4.0.3`, `3.3.4` etc. when `ffmpeg_download_channel` is set to `old-releases`.
ffmpeg_version: 20190701
```

For the other **generated** variables please take a look `task/main.yml`'s `set_fact` section, `vars/main.yml`. And the defaults are in `defaults/main.yml`

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
      ffmpeg_download_channel: 'builds' # builds | release | old-releases
      ffmpeg_version: 20190701
```

For the `release`:

```yml
- hosts: servers
  roles:
    - role: azizunsal.ffmpeg
      ffmpeg_download_channel: 'release' # builds | release | old-releases
      ffmpeg_version: 4.1.4
```

And for any older releases:

```yml
- hosts: servers
  roles:
    - role: azizunsal.ffmpeg
      ffmpeg_download_channel: 'old-releases' # builds | release | old-releases
      ffmpeg_version: 3.4.2
```

License
-------

BSD

Author Information
------------------

[Aziz Unsal](https://azizunsal.github.io/blog/)
