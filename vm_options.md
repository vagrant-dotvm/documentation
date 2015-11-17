### List of options

|Vagrant|DotVm|Remarks|
|-------|:---:|-------|
|boot_timeout|:white_check_mark:||
|box|:white_check_mark:||
|box_check_update|:white_check_mark:||
|box_download_checksum|:white_check_mark:||
|box_download_checksum_type|:white_check_mark:||
|box_download_client_cert|:white_check_mark:||
|box_download_ca_cert|:white_check_mark:||
|box_download_ca_path|:white_check_mark:||
|box_download_insecure|:white_check_mark:||
|box_download_location_trusted|:white_check_mark:||
|box_url|:white_check_mark:||
|box_version|:white_check_mark:||
|communicator|:white_check_mark:||
|graceful_halt_timeout|:white_check_mark:||
|guest|:white_check_mark:||
|hostname|:white_check_mark:|under `name` or `hostname` option|
|post_up_message|:white_check_mark:||
|usable_port_range|:white_check_mark:|||

### Example
```yaml
- nick: machine1
  name: machine1.example.com
  box: chef/centos-7.0
  memory: 1024
  cpus: 1
  cpucap: 100
  primary: true
  natnet: 192.168.22.0/24
  boot_timeout: 300
  box_check_update: true
  box_version: ">= 0"
  graceful_halt_timeout: 60
  post_up_message: "hello!"
  autostart: true
```

### Related documentation
* https://docs.vagrantup.com/v2/vagrantfile/machine_settings.html

