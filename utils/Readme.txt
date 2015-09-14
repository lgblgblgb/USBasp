Files in this directory:

99-USBasp.rules
linux-install-udev-rule

	For Linux systems to allow non-root (eg: without sudo) access of USBasp
	as a regular user. For that, you need to copy file 99-USBasp.rules into
	directory /etc/udev/rules.d/
	linux-install-udev-rule does this exactly, if you don't want to do it
	manually.

pipeout.py

	Stefan Beller's utility to use his feature in his USBasp repository,
	namely to dump communication buffer filled by the target MCU being
	SPI master and providing data (not bi-directional ...).
	You need to Python, and some of its components (eg: USB python
	modules) to be able to use it. 

usbasp.py

	My Python utility with various (done or planned) functions, including
	the functionality of pipeout.py as well. Start it without arguments
	to get some help. Warning! Some functions can behave an USBasp
	with older firmware oddly, with crashing usbasp.py. It's harmless
	though.

