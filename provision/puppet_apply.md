### List of options

|Vagrant|DotVm|
|-------|:---:|
|binary_path|:white_check_mark:|
|facter|:white_check_mark:|
|hiera_config_path|:white_check_mark:|
|manifest_file|:white_check_mark:|
|manifests_path|:white_check_mark:|
|module_path|:white_check_mark:|
|environment|:white_check_mark:|
|environment_path|:white_check_mark:|
|options|:white_check_mark:|
|synced_folder_type|:white_check_mark:|
|synced_folder_args|:white_check_mark:|
|temp_dir|:white_check_mark:|
|working_directory|:white_check_mark:|

### Example
```yaml
provision:
  - type: puppet
    manifests_path: "%host.project_dir%/puppets"
    manifest_file: "site.pp"
```

### Related documentation
* https://docs.vagrantup.com/v2/provisioning/puppet_apply.html
