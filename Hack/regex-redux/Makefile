compile:
	/usr/bin/hh_client

measure:
	sudo modprobe msr
	sudo ../../RAPL/main "/usr/bin/hhvm  regexredux.hack 0 < ../../regexredux-input5000000.txt" Hack regex-redux

run:
	/usr/bin/hhvm  regexredux.hack 0 < ../../regexredux-input5000000.txt
	killall hh_server
mem:
	/usr/bin/time -v /usr/bin/hhvm  regexredux.hack 0 < ../../regexredux-input5000000.txt
	 killall hh_server

valgrind:
	valgrind --tool=massif --stacks=yes  /usr/bin/hhvm  regexredux.hack 0 < ../../regexredux-input5000000.txt
	 killall hh_server
