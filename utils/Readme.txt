Files in this directory:

99-USBasp.rules
linux-install-udev-rule

	For Linux systems to allow non-root (eg: without sudo) access of USBasp
	as a regular user. For that, you need to copy file 99-USBasp.rules into
	directory /etc/udev/rules.d/
	linux-install-udev-rule will does this exactly, if you prefer that way

pipeout.py

	Stefan Beller's utility to use his feature in his USBasp repository,
	namely to dump communication buffer filled by the target MCU being
	SPI master and providing data (not bi-directional ...).
	You need to Python, and some of its components (eg: USB python
	modules) to be able to use it. 

