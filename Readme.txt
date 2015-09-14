Original Readme.txt can (and should) be found as: Readme-original.txt
Please read it!

From the original documentation:

"USBasp is a USB in-circuit programmer for Atmel AVR controllers. It simply
 consists of an ATMega88 or an ATMega8 and a couple of passive components.
 The programmer uses a firmware-only USB driver, no special USB controller
 is needed."

This repository contains a patched version of the original USBasp firmware
compared to the "official" firmware. Please note, that you may have problems
with this one, use this at your OWN risk! If you are a regular user not so
interested in extra features, please stick with the official firmware!

The official firmware can be found here: http://www.fischl.de/usbasp/

History, important changes compared to the original firmware:

Step 1:

	http://www.fischl.de/usbasp/
	usbasp.2011-05-28.tar.gz
	Original/official firmware
	Readme-original.txt contains the original Readme of the project
	Changelog-original.txt contains the original Changelog of the project

Step 2:

	https://github.com/stefanbeller/USBasp
	Original firmware was imported to a Github respository by Stefan
	Beller. It was then modified/extended by him, key features:

	* Missing "const" keywords at "PROGMEM" directives to allow to compile
	  the source with newer avr-gcc versions (older ones seems to ignore
	  the problem so it worked)

	* Target pushed data (as target being the SPI master) via SPI is stored
	  in the communication buffer, which can be read from your PC. A simple
	  Python based tool is provided by him for this purpose. It's only
	  uni-directional

	Greetings, great work of the author, thanks!

Step 3:

	http://www.avrfreaks.net/projects/usbasp-tty-usbasp-programmer-modified-serial-support-and-terminal-program
	"Emklaus" (aka EMK) patched the original (step 1) firmware to
	allow to use the RX/TX (TTL serial) lines of the programmer, so the
	target device can communicate with the PC through the USBasp which
	"relays" (bi-directional) the information towards the PC. A Windows
	based client software is also provided in the archive. Currently I
	did not import the client software itself, as it's too platform
	dependent (Windows only, I do not use Windows).
	EMK's work often referred as "USBasp-TTY".

	Greetings, great work of the author, thanks!

Step 4:

	https://github.com/lgblgblgb/USBasp
	I (LGB, lgblgblgb on github) have forked Stefan Beller's repository on
	Github (step 2), and merged EMK's (step 3) changes into the repository
	with some manual work (it wouldn't apply automatically by "patch").
	Also, some cosmetical changes, and unify line endings hell (mixed
	DOS / UNIX style). Of course much more work is planned for the future.
	Changelog.txt contains the changelog of my changes (including my work
	and using other's work as well, as it noted above)

Step 5:

	Plans, ongoing new work from me, testing.

	Including:

	utils/usbasp.py will be a python based utility with functions including
	pipeout.py's but also USBasp-tty client works later.

