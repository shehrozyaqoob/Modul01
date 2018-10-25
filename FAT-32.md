FAT File Systems. FAT32, FAT16, FAT12. The File Allocation Table (FAT) file system is a simple file system originally designed for
small disks and simple folder structures. The FAT file system is named for its method of organization, the file allocation table,
which resides at the beginning of the volume.
***Why is there a 4gb limit on fat32?**
Because FAT32 stores 32-bit file sizes and the maximum you can store in 32 bits is 2^32-1 ~= 4.29e9. 2^32-1 bytes = 4GB - 1 byte. 
