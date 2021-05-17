# EAZAO-Zero Ceromic3D Printer Firmware

The firmware of EAZAO-Zero and the system firmware of the open source EAZAO-Zero printer are modified based on the popular marlin firmware, mainly using functions such as M163. We hope to use EAZAO as an open platform to provide services to ceramic artists and enthusiasts who are beginning to contact ceramic printing.

## Communication

You can find [more models]( https://www.thingiverse.com/eazao/designs) that can be printed directly with EAZAO-zero printers.

You can submit a bug or feature request, [file an issue](https://github.com/Eazao/EAZAO-Zero-controller/issues/new) in github issues.

You can join the [EAZAO facebook group](:https://www.facebook.com/groups/eazao) to exchange questions and share experiences with everyone.

## Development 

As of recommended in Marlin's development settings, we use **PlatformIO plug-in in VScode** or **Arduino IDE** to develop EAZAO-Zero-controller.

### Download & install software

- Follow [Setting up Visual Studio Code](https://code.visualstudio.com/docs/setup/setup-overview) to install and setup **VSCode**.

  Follow the [Guide](https://platformio.org/install/ide?install=vscode) to install PlatformIO extension in **VSCode**.

- Follow the [Guide](https://www.arduino.cc/en/Guide) to install Arduino IDE.

- Download [EAZAO-Zero-controller](https://github.com/Eazao/EAZAO-Zero-controller) firmware to your local folder.

### Configure environment & update firmware

EAZAO-Zero printer firmware can be updated using Visual Studio Code and Ardunio IDE software

- #### Ardunio IDE  configure environment
  - Use a USB cable to connect your PC to the mainboard
  - Use the **Open…** command in the **Arduino File** menu to open the downloaded firmware
  - Use the **Tools** command in the Ardunio menu to configure ***Tools->Boards->Ardunio AVR board->Ardunio Mega or Mega 2560***
  - Use the **Tools** command in the Ardunio menu to configure ***Tools->Processor->ATmega2560(Mega2560)***
  - Use the **Tools** command in the Ardunio menu to configure ***Tools->Port->COMx***（COMx refers to the COM interface added after USB connection）

- #### Ardunio IDE update firmware
  - Use the **Verify/Compile** command in the **Ardunio sketch** menu to compile the firmware code

  - Use the **Upload** command in the **Ardunio sketch** menu to upload the firmware to main controller

- #### Visual Studio Code configure environment
  - Use a USB cable to connect your PC to the mainboard
  - Use the **Open Folder…** command in the **VSCode** **File** menu to open the **EAZAO-Zero-Controller** firmware

  - After opening the source code in **VSCode**, you will see an alien avatar icon on the left status bar, which also indicates that PlatformIO has been successfully installed.

- #### Visual Studio Code update firmware
  - Click on the alien icon **(PlatformIO)** on the left side of VScode
  - Use ***Project Tasks->Default->General->Build***  command to compile the code

  **NOTE:** if you build the source for first time, PlatformIO will download the relative libraries and toochains. It may take a few minutes

  - Use ***Project Tasks->Default->General->Upload*** command to upload the firmware to main controller
  - To clean previous build, just click the **clean** icon, or type command ***pio run -t clean*** in the terminal

## License

Marlin is published under the [GPL license](https://github.com/COPYING.md) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.

