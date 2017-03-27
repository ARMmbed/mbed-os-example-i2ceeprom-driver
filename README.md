# Getting Started With The mbed-os Example for the I2C EEPROM Block Device 

This is the mbed-os example for the I2CEEBlockDevice driver. 
See the [i2ceeprom-driver](https://github.com/armmbed/i2ceeprom-driver) repository for more information.

This guide outlines the steps to get the I2C EEPROM part working on an mbed OS platform fitted with the CI Test Shield.

Please install [mbed CLI](https://github.com/ARMmbed/mbed-cli#installing-mbed-cli).

## Hardware Requirements

This example can be used on an mbedos platform with a CI Test Shield inserted into the Arduino header.

This document uses the K64F as an example. Simply change the relevant options (e.g. -m K64F) to be appropriate for your target.

## Create the Example Application

From the command-line, import the example:

```
mbed import mbed-os-example-i2ceeprom-driver
```

You should see: 

	[mbed] Importing program "mbed-os-example-i2ceeprom-driver" from "https://github.com/ARMmbed/mbed-os-example-i2ceeprom-driver" at latest revision in the current branch
	[mbed] Adding library "mbed-os" from "https://github.com/ARMmbed/mbed-os" at rev #f4864dc6429e

Move into the newly created directory:

```
cd mbed-os-example-i2ceeprom-driver
```
	
If the mbed-os library was not automatically added (see trace above), do the following to import mbed-os:

```
mbed new .
```

Add the i2ceeprom-driver repository: 

```
mbed add i2ceeprom-driver
```

## Build the Example

Invoke `mbed compile`, and specify the name of your platform and your favorite toolchain (`GCC_ARM`, `ARM`, `IAR`). For example, for the GCC_ARM toolchain:

```
mbed compile -m K64F -t GCC_ARM
```

Your PC may take a few minutes to compile your code. At the end, you see the following result:

	[snip]
	todo: paste snippet here
	
## <a name="run-the-example-binary-on-the-k64f"></a> Run the Example Binary on the K64F 

Copy the binary from `<root_dir>/mbed-os-example-i2ceeprom-driver/BUILD/K64F/GCC_ARM/mbed-os-example-i2ceeprom-driver.bin` to the K64F:

1. Connect your mbed device to the computer over USB.
1. Copy the binary file to the mbed device.
1. Press the reset button to start the program.
1. Open the UART of the board in your favorite UART viewing program. For example, `screen /dev/ttyACM0`.

After connecting a serial console and resetting the target, the following trace should be seen:

	<to be updated>


# Troubleshooting

1. Make sure `mbed-cli` is working correctly and its version is newer than `1.0.0`.

 ```
 mbed --version
 ```

 If not, update it:

 ```
 pip install mbed-cli --upgrade
 ```
 
