aosjdf;lakjsdf;lakjsdf;llasjdf NOT DONE, GET EXAMPLE LS _AIN OUTPUT
## UID: 705747359

(IMPORTANT: Only replace the above numbers with your true UID, do not modify spacing and newlines, otherwise your tarfile might not be created correctly)

# Hey! I'm Filing Here

This sets up a basic ext2 file system with a root dir, lost+found dir, hello-world file, and symlink to the hello world file called hello.

## Building

run `make`

## Running

run `./ext2-create` to create cs111-base.img
you can check if it is correct by runnning `fsck.ext2 cs111-base.img`, which should run without any errors

to mount, first create a dir called mnt `mkdir mnt`, then run `sudo mount -o loop cs111-base.img mnt`, which will mount the image
you can now run `cd mnt` to enter mnt and it will be treated as its own file system. 

Running `ls -ain` will output: 

you can also check the files are cor`rect with: 
`cat hello` and `cat hello-world`, both should output Hello world

## Cleaning up

first return to the original dir `cd ..`
then you can run `make clean` to remove the img and executables
to unmount, run `sudo umount mnt`