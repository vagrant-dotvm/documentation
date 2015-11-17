You can use few types of variables in DotVm configuration:
* [Global](#global-variables)
* [Project](#project-variables)
* [Environment](#environment-variables)
* [Special](#special-variables)

## Global variables
Global variables are configured in `variables/*.yaml` files.
You can use these variables in configuration files within all projects.

### Example
variables/example.yaml
```yaml
memory: "1024"
```

projects/example/machines/example.yaml
```yaml
- nick: example1
  name: example1
  box: "chef/centos-7.0"
  memory: "%global.memory%"
```

## Project variables
Project variables are configured in `projects/*/variables/*.yaml` files.
These variables are visible in all configuration files within particular project.

### Example
projects/example/variables/example.yaml
```yaml
memory: "1024"
```

projects/example/machines/example.yaml
```yaml
- nick: example1
  name: example1
  box: "chef/centos-7.0"
  memory: "%project.memory%"
```

## Environment variables
DotVm passes environment variables into your configuration files.
You can use them by inserting `%env.VARIABLE_NAME%` in your configuration.

### Example
```yaml
- nick: example1
  name: example1
  box: "chef/centos-7.0"
  memory: "%env.MEMORY%"
```

```shell
$ export MEMORY=1024
$ vagrant up example1
```

## Special variables
To prevent hardcoding paths to project specific files you can use below variables:
* host.project_dir
* host.files_dir
* guest.project_dir
* guest.files_dir
