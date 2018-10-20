KERN_DIR = /home/book/Desktop/work/linux/linux-3.5

TCC = arm-none-linux-gnueabi-gcc
TCFLAGS = -march=armv4t -mtune=arm920t

MODULE_NAME1 = led_dev
MODULE_NAME2 = led_drv
TEST_NAME = led_test

obj-m	+= $(MODULE_NAME1).o $(MODULE_NAME2).o

.PHONY :all clean
all:
	make -C $(KERN_DIR) M=`pwd` modules 
	$(TCC) $(TCFLAGS) -o $(TEST_NAME) $(TEST_NAME).c
clean:
	make -C $(KERN_DIR) M=`pwd` modules clean
	rm -rf modules.order
	rm -f $(TEST_NAME)