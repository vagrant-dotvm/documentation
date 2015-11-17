You can authorize SSH key using DotVM, so you can login later into VM using your SSH key pair.
This option is not directly available in `Vagrant` but realized by helper script included in `DotVm`.
You can authorize key from specified file or hardcoded as a string in YAML file.

Example:
```yaml
- nick: main
  authorized_keys:
    - type: file
      path: "~/.ssh/id_rsa.pub"
    - type: static
      key: "ssh-rsa fakeSSHpubKEY km@laptop"
```
