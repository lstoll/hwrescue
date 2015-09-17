# Rescue Image

[![Build Status](https://magnum.travis-ci.com/lstoll/hwrescue.svg?token=UhypCbZxcoMpXfTko3wu)](https://magnum.travis-ci.com/lstoll/hwrescue)

This is a simple framework to build a PXE/iPXE bootable distibution containing the base essentials to interact with and repair a system. It is built using [debirf](http://cmrg.fifthhorseman.net/wiki/debirf)

The intention is for this project to also serve as or provide a base for the "ready" default image that audits hardware

## Development

A vagrant environment is provided, with the necessary tools and apt caching. Run ./script/vagrantbuild in there

### Running the kernel/initrd with a serial console

`./script/run_kernel_qemu` command will launch the generated kernel and initrd inside qemu, with the console being emulated serial. Exit this with `C-a x`

*note* this doesn't correctly bring up a login prompt. Unsure if this is a serial bug or qemu issue right now

### Running the iso

`./script/run_iso_virtualbox` will launch the ISO image inside virtualbox

## Deployment

changes on master will trigger a build, and upload artifacts. These can be retrieved from:

* kernel: http://cdn.lstoll.net/artifacts/hwrescue/vmlinuz
* initrd: http://cdn.lstoll.net/artifacts/hwrescue/initrd.cgz

* iso image: http://cdn.lstoll.net/artifacts/hwrescue/image.iso
