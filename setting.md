# Ubuntu 세팅

## kvm 설치
```
$ sudo apt update
$ sudo apt install cpu-checker
$ sudo apt install qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils virtinst virt-manager
$ kvm-ok
$ sudo systemctl is-active libvirtd
$ sudo usermod -aG libvirt $USER
$ sudo usermod -aG kvm $USER
```

https://www.minzkn.com/moniwiki/wiki.php/UbuntuVirtualMachineServerInstall

## 네트워크
```
$ brctl show
```


## vi /tmp/br0.xml
```
<network>
  <name>br0</name>
  <forward mode='bridge'/>
  <bridge name='br0'/>
</network>
```

```
$ virsh net-define /tmp/br0.xml
$ virsh net-start br0
$ virsh net-autostart br0
```
