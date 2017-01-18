## BnrOmni3MD_Raspberry

Botnroll Omni3MD library for RaspberryPi and other Linux-based ARM devices.

This library interfaces Omni3MD Omnidirectional motor controller using ARM's I2C Bus. It uses Linux native system calls (using i2c-dev lib for user-space calls) and includes every feature implemented in the original library (please refer to [Omni3MD Homepage](http://botnroll.com/omni3md/)). 

This library is still in development and testing, it requires caution when using it. Problems caused to any hardware it's up to the user.

###Pre-build process
* First enable I2C bus in your development board   
* Install dependencies
  * $ sudo apt-get install cmake build-essential
  * $ sudo apt-get install libi2c-dev

###Build process
* $ git clone https://github.com/botnroll/BnrOmni3MD_Raspberry/
* $ cd BnrOmni3MD_Raspberry
* $ mkdir build
* $ cd build
* $ cmake ..
* $ make

Also, refer to software and hardware manuals in doc/ directory. Apart from the funcionalities from the original library, this library includes a built-in safety timeout. This timeout safety only triggers if no movement commands are sent. Furthermore, it will be added configuration files in JSON schema. For now, this library only supports RaspberryPi's I2C bus addressing.


###Botnroll
