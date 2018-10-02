# Arduino-System-Monitor
This is CPU + RAM usage monitor using an Arduino and a Java program. Java app was tested on Windows.
<br /> Java app is using ![rxtx](http://rxtx.qbang.org/wiki/index.php/Main_Page) and ![javasysmon](https://github.com/jezhumble/javasysmon) libs.
<br />![photo](https://raw.githubusercontent.com/IvanYarovyi/Arduino-System-Monitor/master/photo.png)
#### Software you need:
| Software | LINK |
| ------ | ------ |
| Java 8 | [https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html] |
| Gradle | [https://gradle.org/install/] |
|Arduino IDE| [https://www.arduino.cc/en/Main/Software] |
##### Stuff you Need:
- 1 * Arduino Uno board
- 1 * Breadboard
- 1 * LCD1602
- 1 * Potentiometer (50kΩ)
- Jumper wires
- 1 * USB cablea

### Step 1: Connect the LCD to the Arduino
![schematic_diagram](https://raw.githubusercontent.com/IvanYarovyi/Arduino-System-Monitor/master/schematic_diagram.png)
### Step 2: Uploading the sketch
Upload arduino/pc_monitor.ino to Arduino Uno
### Step 3: Building the Java Application
```sh
cd pc
gradle fatJar
```
### Step 4: Running the Java Application
```sh
java -Djava.library.path=libs\rxtx\win-x64\ -jar  pc/build/libs/sys_monitor-all-1.0-SNAPSHOT.jar COM5
```
Where "COM5" is your Serial Port port value, 
<br /> and do not forget to specify a library path according to your OS
### You are now finished!
