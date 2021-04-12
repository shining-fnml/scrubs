# NAME

Scrubs - Scrubs Checks and Repairs Un(encrypted) Blocks Suddenly

# SYNOPSIS

scrubs \[--luks PARTNO\] imagefile

or

scrubs --help|--install|--man|--version

# DESCRIPTION

**Scrubs** is an interactive tool to check the status of the partitions found in a disk image file.
It can create new filesystems, repair or enlarge old ones, mount them transparently through losetup(8) and perform the other common operations required in data recovery.
**Scrubs** will scan _imagefile_ assuming it's a disk image and can explore a loop mounted filesystem launching mc(1) (midnight commander) if found in the _$PATH_.

# OPTIONS

- **--help**

    Print a brief help message and exits.

- **--install**

    Install the program and the man page in the usual paths.

- **--luks PARTNO**

    Use this option if _imagefile_ contains a _Luks_ partition and this partition, once decrypted, contains a whole disk image.
    **Scrubs** will use the unencrypted contents as disk image.
    When using this option _imagefile_ can be a block device.

- **--man**

    Prints the manual page and exits.

- **--version**

    Prints the program version and exists.

# BUGS

It's not surprising that (like every program that plays with partitions and filesystems) **scrubs** can destroy your data.
There are no unfixed bugs at the moment, but you must be careful and backup, copy, dd(1) and everything you usually do before the beginning.

# COPYRIGHT

Copyright 2021 Shining (shining-fnml on github.com).
License  GPLv3+:  GNU GPL version 3 or later &lt;https://gnu.org/licenses/gpl.html>.
This  is  free  software:  you  are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
