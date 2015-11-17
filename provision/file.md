### List of options

|Vagrant|DotVm|
|-------|:---:|
|source|:white_check_mark:|
|destination|:white_check_mark:|

### Example
```yaml
provision:
  - type: file
    source: "%host.project_dir%/settings.ini"
    destination: "/home/vagrant/settings.ini"
```

### Related documentation
* https://docs.vagrantup.com/v2/provisioning/file.html
