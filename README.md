# Repacker
<p>A simple script that I made for fun</p>
# How to use
<p>First we need to get the decimals for the pack </p>
-
<p>To do that we use binwalk</p>
<p>Once we have the decimals put in the starting one the ending of another header and add a 1 to the starting decimal else the out file will by off by one</p>
-
<p>For the first one put 0 as the starting decimal</p>
-
<p>Example:</p>
-
<p>Backup the 512 bytes from a file/disk</p>

``parts[1] = {}``
``parts[1].name = "mbr"``
``parts[1].startdecimal = 0``
``parts[1].decimal = 512``

# TODO<
</p>[ ] Fix when the input file is large</p>
