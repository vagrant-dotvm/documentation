# How to install
Install DotVm using builtin Vagrant plugin manager:
```
$ vagrant plugin install vagrant-dotvm
$ vagrant plugin install vagrant-group # recommended
```

# Configuration layout
```text
.
├── Vagrantfile
├── options
│   └── ssh.yaml
├── projects
│   └── main
│       ├── machines
│       │   └── main.yaml
│       ├── variables
│       │   └── main.yaml
│       └── files
│           └── default.pp
└── variables
    ├── directories.yaml
    └── parameters.yaml
```

* `options` - contains `yaml` files storing [Options](options.md)
* `projects/project/machines` - contains `yaml` files storing machines configuration
* `projects/project/variables` - contains `yaml` files storing [Project variables](variables.md#project-variables)
* `projects/project/files` - reserved for your needs, e.g. provisioning files
* `variables` - contains `yaml` files storing [Global variables](variables.md#global-variables)

# Example Vagrantfile
```ruby
require 'vagrant-dotvm'

Vagrant.configure(2) do |config|
  dotvm = VagrantPlugins::Dotvm::Dotvm.new __dir__
  dotvm.inject(config)
end
```

# Example configuration
You can see example configurations [here](https://github.com/vagrant-dotvm/examples).
