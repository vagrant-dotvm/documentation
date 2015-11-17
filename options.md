`Vagrant` provides ability to change its behaviour by setting global options.
In `DotVm` You can pass these options using yaml files in `options` directory.
Remember that these settings are used for all machines defined in configuration.
Setting the same options multiple times from different YAML files gives undefined behaviour.

`options` dictionary in config gives you ability to set global options for:
* ssh
* winrm
* vagrant

### Example
options/something.yaml:
```yaml
ssh:
  - name: forward_x11
    value: true

winrm:
  - name: username
    value: vagrant

vagrant:
  - name: host
    value: linux
```

### Related documentation
* https://docs.vagrantup.com/v2/vagrantfile/ssh_settings.html
* https://docs.vagrantup.com/v2/vagrantfile/winrm_settings.html
* https://docs.vagrantup.com/v2/vagrantfile/vagrant_settings.html
