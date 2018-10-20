KERN_DIR = /home/book/Desktop/work/linux/linux-3.5

TCC = arm-none-linux-gnueabi-gcc
TCFLAGS = -march=armv4t -mtune=arm920t

MODULE_NAME = s3c_ts

obj-m	+= $(MODULE_NAME).o

.PHONY :all clean
all:
	make -C $(KERN_DIR) M=`pwd` modules 
clean:
	make -C $(KERN_DIR) M=`pwd` modules clean
	rm -rf modules.order