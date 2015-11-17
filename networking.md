|Vagrant|DotVm|Remarks|
|-------|:---:|-------|
|guest|:white_check_mark:||
|guest_ip|:white_check_mark:||
|host|:white_check_mark:||
|host_ip|:white_check_mark:||
|protocol|:white_check_mark:||
|auto_correct|:white_check_mark:||
|type|:white_check_mark:||
|ip|:white_check_mark:||
|netmask|:white_check_mark:|you can use `mask` or `netmask`|
|auto_config|:white_check_mark:||
|bridge|:white_check_mark:||
|virtualbox__intnet|:white_check_mark:|you can use `virtualbox__intnet` or `interface`|

Network identifier is passed by parameter `net`.

## Private networking
To configure private networking you need to use `private_network` net.
You can also use shorter alias `private` to do the same.

### Static IP

Example:
```yaml
- nick: main
  networks:
    - net: private_network
      type: static
      ip: 192.168.56.100
      mask: 255.255.255.0
      interface: "intnet0"
```

### DHCP

Example:
```yaml
- nick: main
  networks:
    - net: private_network
      type: dhcp
      interface: "intnet0"
```

## Public networking
To configure public networking you need to use `public_network`.
You can also use shorter aliases `public` or `bridged` to do the same.
You need also to specify network interface it will be bridged to.

### Static IP

Example:
```yaml
- nick: main
  networks:
    - net: public_network
      type: static
      ip: 192.168.56.100
      mask: 255.255.255.0
      bridge: "en0: Wi-Fi (AirPort)"
```

### DHCP

Example:
```yaml
- nick: main
  networks:
    - net: public_network
      type: dhcp
      bridge: "en0: Wi-Fi (AirPort)"
```

## Port forwarding
To forward port from host to guest machine you need to use `forwarded_port` net.
You can also use alias `port` to do the same.

Example:
```yaml
- nick: main
  networks:
    - net: forwarded_port
      guest: 80
      host: 1080
```
