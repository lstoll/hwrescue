# Ready Image

This image wil be the default PXE boot target.

It should be light enough to boot fast, but have enough of an OS to be useful.

It should also serve a secondary purpose as a rescue and recovery image.

## Development

A vagrant environment is provided, with the necessary tools and apt caching. Run ./script/vagrantbuild in there

### Running the kernel/initrd with a serial console

the `./script/kernel_run` command will launch the generated kernel and initrd inside qemu, with the console being emulated serial. Exit this with `C-a x`

### Running the iso
