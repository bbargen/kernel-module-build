KERNEL_TREE_PATH?=/lib/modules/$(shell uname -r)/build
EXTRA_CFLAGS="-DDEBUG"

obj-m += soft_uart.o

soft_uart-objs := module.o raspberry_soft_uart.o queue.o

all:
	$(MAKE) -C $(KERNEL_TREE_PATH) M=$(PWD) modules

clean:
	make -C $(KERNEL_TREE_PATH) M=$(PWD) clean

.PHONY: all clean
