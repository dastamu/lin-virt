# lin-virt
How use virtualization in Linux

## Full virtualization
### KVM
#### Dependences
```
sudo dnf install qemu-kvm libvirt virt-install virt-viewer
sudo systemctl daemon-reload
sudo systemctl enable --now libvirtd
```
#### Runing
```
qemu-img create -f qcow2 vm-test.qcow2 16G
virt-install --name=VMTest --vcpus=2 --memory=4096 --disk path=vm-hd.qcow2,size=16 --cdrom=img.iso --os-variant=generic --network default --graphics vnc
```
#### Usefull commands
```sh
# List VM
virsh list --all
# Stop VM

# Start VM

```

## Paravirtualization
### Xen

## Contenerization
### Docker
### LXC/LXD

## Soft Emulation
### QEMU

## Host Virtualization
### VirtualBox
### VMVare
