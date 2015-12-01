# packer-libvirt-profiles

This is a simple packer configuration for generating qemu compatiable
VMs and then creating vagrant boxes.

Thanks to skamithi for creating the initial readme. Check out his blog
for creating [libvirt-vagrant](http://linuxsimba.com/building-qcow-vagrant-box/)
compatible boxes.

## Requirements
* Install [Libvirt](http://libvirt.org)

## Download Packer

[Packer](http://www.packer.io/intro) is for creating machine images from a
single source configuration.

Packer ships in a zip package that contains binary files. Example of how
download packer and update the executable path search location.

```
mkdir $HOME/packer
cd $HOME/packer
wget https://dl.bintray.com/mitchellh/packer/packer_0.8.5_linux_amd64.zip
unzip packer_0.8_5_linux_amd64.zip
export PATH=$HOME/packer:$PATH
```

You can download the latest version of packer
[here](http://www.packer.io/downloads.html).

## Build a  Libvirt Compatible Box.

```
git clone https://github.com/jtoppins/packer-libvirt-profiles.git
cd packer-libvirt-profiles
packer build debian-8.1-amd64.json
```
