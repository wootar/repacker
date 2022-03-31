# Repacker
A simple script that I made for fun
# How to use
First we need to get the decimals for the pack 
-
To do that we use binwalk:
``
binwalk (firmware file)
DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
262144        0x40000         Linux EXT filesystem, blocks count: 4096, image size: 4194304, rev 2.0, ext2 filesystem data, UUID=84173db5-fa99-e35a-95c6-28613cc73cc7, volume name "kernel"
17301504      0x1080000       Squashfs filesystem, little endian, version 4.0, compression:xz, size: 4156562 bytes, 1348 inodes, blocksize: 262144 bytes, created: 2022-02-16 20:29:10
``
-
Once we have the decimals put in the starting one the ending of another header and add a 1 to the starting decimal else the out file will by off by one
-
For the first one put 0 as the starting decimal
-
Example:
-
Backup the 512 bytes from a file/disk
`
parts[1] = {}
parts[1].name = "mbr"
parts[1].startdecimal = 0
parts[1].decimal = 512
`
# TODO
[ ] Fix when the input file is large
