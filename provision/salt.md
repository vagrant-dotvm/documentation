### List of options

|Vagrant|DotVm|
|-------|:---:|
|minion_config|:white_check_mark:|
|run_highstate|:white_check_mark:|
|install_master|:white_check_mark:|
|no_minion|:white_check_mark:|
|install_syndic|:white_check_mark:|
|install_type|:white_check_mark:|
|install_args|:white_check_mark:|
|install_command|:white_check_mark:|
|always_install|:white_check_mark:|
|bootstrap_script|:white_check_mark:|
|bootstrap_options|:white_check_mark:|
|version|:white_check_mark:|
|minion_key|:white_check_mark:|
|minion_id|:white_check_mark:|
|minion_pub|:white_check_mark:|
|grains_config|:white_check_mark:|
|masterless|:white_check_mark:|
|master_config|:white_check_mark:|
|master_key|:white_check_mark:|
|master_pub|:white_check_mark:|
|seed_master|:white_check_mark:|
|run_highstate|:white_check_mark:|
|run_overstate|:white_check_mark:|
|orchestrations|:white_check_mark:|
|colorize|:white_check_mark:|
|log_level|:white_check_mark:|
|pillar|:x:|

### Example
```yaml
provision:
  - type: salt
    minion_config: "%host.project_dir%/salt/minion"
    run_highstate: true
```

### Related documentation
* https://docs.vagrantup.com/v2/provisioning/salt.html
