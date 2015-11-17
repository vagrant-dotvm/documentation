### List of options

|Vagrant|DotVm|
|-------|:---:|
|inline|:white_check_mark:|
|path|:white_check_mark:|
|args|:white_check_mark:|
|binary|:white_check_mark:|
|privileged|:white_check_mark:|
|upload_path|:white_check_mark:|
|keep_color|:white_check_mark:|
|name|:white_check_mark:|
|powershell_args|:white_check_mark:|

### Examples
```yaml
provision:
  - type: shell
    inline: "mkdir /home/vagrant/settings"
```

```yaml
provision:
  - type: shell
    path: "%host.project_dir%/provisioner.sh"
```

### Related documentation
* https://docs.vagrantup.com/v2/provisioning/shell.html
