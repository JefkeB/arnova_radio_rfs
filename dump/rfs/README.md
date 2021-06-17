extracted from a 'broken' device with  
>nanddump --noecc -f mtd5_ /dev/mtd5  
Block size 524288, page size 4096, OOB size 128
Dumping data starting at 0x00000000 and ending at 0x10000000...

extract rfs from mtd5.dump  
git clone https://github.com/justsoso8/yaffs2utils.git
cd yaffs2utils/src
make
./unyaffs2 -p 4096 -s 128  ../../../nfs/mtd5.dump extracted
