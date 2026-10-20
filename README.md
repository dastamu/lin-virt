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
#### Starting VM with ISO Image
```
virt-install --name=VMTest --vcpus=2 --memory=4096 --disk path=vm-hd.qcow2,size=16 --cdrom=img.iso --os-variant=generic --network default --graphics vnc
```
#### Usefull commands
```sh
# List VM
virsh list --all
# Stop VM

# Start VM

# Create virtual HD
qemu-img create -f qcow2 vm-hd.qcow2 16G
```

## Paravirtualization
### Xen

## Contenerization
### Docker
### LXC/LXD
### Incus
#### Dependences
```sh
#@ EL 10
sudo wget -P /etc/yum.repos.d/ https://copr.fedorainfracloud.org/coprs/neelc/incus/repo/rhel+epel-10/neelc-incus-rhel+epel-10.repo
sudo dnf update
sudo dnf install incus incus-tools
```

## Soft Emulation
### QEMU

## Host Virtualization
### VirtualBox
```sh
VBoxManage list vms
VBoxManage startvm "MY_VM_NAME"
VBoxManage startvm "MY_VM_NAME" --type headless
```
### VMVare
