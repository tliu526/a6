now:	target1 target2 target3 target4 target5 target6 target7

target1:	target1.c
	gcc -g -o target1 target1.c

target2:	target2.c
	gcc -g -o target2 target2.c

target3:	target3.c
	gcc -g -fomit-frame-pointer -O2 -o target3 target3.c

target4:	target4.c
	gcc -g -o target4 target4.c

target5:	target5.c tmalloc.c tmalloc.h
	gcc -g -c tmalloc.c
	gcc -g -o target5 target5.c tmalloc.o

target6:	target6.c
	gcc -g -o target6 target6.c

target7:	target7.c
	gcc -g -o target7 target7.c

clean:
	@rm -f target? *.o *~

install:	now
	cp target? /usr/local/bin
	chown t1:t1 /usr/local/bin/target1
	chown t2:t2 /usr/local/bin/target2
	chown t3:t3 /usr/local/bin/target3
	chown t4:t4 /usr/local/bin/target4
	chown t5:t5 /usr/local/bin/target5
	chown t6:t6 /usr/local/bin/target6
	chown t7:t7 /usr/local/bin/target7
	chmod 4755 /usr/local/bin/target?
	@echo Installed.
