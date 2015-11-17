If you have installed plugin `vagrant-group` plugin then you
are able to associate VM to many groups, and then do basic
operations like `up`, `halt`, `provision`, `destroy` on specific group of VMs.

### Example
```yaml
- nick: machine1
  groups:
    - webservers
    - main
```

### Related documentation
* https://github.com/vagrant-group/vagrant-group/blob/master/README.md
