A PC BIOS generally adds additional constraints for disk partitioning. There is a limit to how many ``primary'' and ``logical'' partitions
a drive can contain. Additionally, there are limits to where on the drive the BIOS looks for boot information. This section will include 
a brief overview to help you plan most situations. 
``Primary'' partitions are the original partitioning scheme for PC hard disks. However, there can be only four of them. To get past this 
limitation, ``extended'' or ``logical'' partitions were invented. By setting one of your primary partitions as an extended partition, you
can subdivide all the space allocated to that partition into logical partitions. The number of logical partitions you can create is much 
less limited than the number of primary partitions you can create; however, you can have only one extended partition per drive. 
Linux limits the number of partitions per drive to 15 partitions for SCSI drives (3 usable primary partitions, 12 logical partitions), and
63 partitions for IDE drives (3 usable primary partitions, 60 logical partitions). 
The last issue you need to know about a PC BIOS is that your boot partition - that is, the partition containing your kernel image - needs
to be contained within the first 1,024 cylinders of the drive. Because the root partition is usually your boot partition, you need to make
sure your root partition fits into the first 1,024 cylinders. 
If you have a large disk, you may have to use cylinder translation techniques, which you can set in your BIOS, such as LBA translation 
mode.  If you are using a cylinder translation scheme, your
boot partition must fit within the translated representation of cylinder 1,024.
