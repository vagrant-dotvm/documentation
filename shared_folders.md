### List of options

|Vagrant|DotVm|
|-------|:---:|
|create|:white_check_mark:|
|disabled|:white_check_mark:|
|group|:white_check_mark:|
|mount_options|:white_check_mark:|
|owner|:white_check_mark:|
|type|:white_check_mark:|
|nfs_export|:white_check_mark:|
|nfs_udp|:white_check_mark:|
|nfs_version|:white_check_mark:|
|rsync__args|:white_check_mark:|
|rsync__auto|:white_check_mark:|
|rsync__chown|:white_check_mark:|
|rsync__exclude|:white_check_mark:|
|rsync__rsync_path|:white_check_mark:|
|rsync__verbose|:white_check_mark:|
|smb_host|:white_check_mark:|
|smb_password|:white_check_mark:|
|smb_username|:white_check_mark:|

Host location of shared folder should be specified using `host` key,
guest location by using `guest` key.

### Example
```yaml
- nick: main
  shared_folders:
    - host: ~/projects
      guest: /srv/www
```

### Related documentation
* https://docs.vagrantup.com/v2/synced-folders/index.html
