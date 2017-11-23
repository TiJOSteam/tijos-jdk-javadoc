# TiJOS JDK Overview 

The TiJOS JDK includes two parts: the standard Java JDK and the TiJOS Framework, the standard Java JDK part is compatible with the Oracle standard Java JDK, and the standard Java code can be used directly on the TiJOS platform; The TiJOS Framework is mainly used to operate hardware peripherals and sensors, while also supporting the configuration of the platform itself, such as the network.  

# Standard Java core class support

The TiJOS JDK contains most of the commonly used Java base core classes, including java.lang, java.io, java.net, java.util, etc. The classes in these packages are the base of the entire JAVA JDK to meet the various application development requirements.

Given that TiJOS runs under the very limited resources of the MCU, the following Java features are not supported in the TiJOS JDK:

1. Reflection:  Unsupported
2. Serialization : Unsupported
3. Regular Expression : Unsupported, You can use string - related operation functions to achieve the corresponding functions
4. Locale :  Unsupported
5. finalize:  Do not execute code in an object's finalize method, which is not invoked




The TiJOS JDK supports core packages provided in the standard Java JDK, including

| Standard Java Package | Description                              |
| --------------------- | ---------------------------------------- |
| java.lang             | the basic classes of the Java language   |
| java.io               | IO Stream support, which contains all of the output stream classes |
| java.net              | Network classes                          |
| java.util             | Contains collections and various utility classes |



## java.lang Package Support

TiJOS JDK contains most of the classes of the standard java.lang package, but the reflection reletated methons are not supported, like ClassLoader, etc. 

The following list only lists the standard Java classes and interfaces supported by the TiJOS JDK, and you can refer to the standard Java documentation for specific use.

**Supported Class List**

- Boolean
- Byte
- Character
- Class
- Double
- Enum
- Float
- Integer
- Long
- Math
- Number
- Object
- Runtime
- Short
- String
- StringBuffer
- StringBuilder
- System
- Thread
- Throwable
- Void


## java.io Package Support

TiJOS JDK contains most of the classes of the standard java.io package, but serialization is not supported.

The following list only lists the standard Java classes and interfaces supported by the TiJOS JDK, and you can refer to the standard Java documentation for specific use.

**Supported Class List**

- BufferedInputStream
- BufferedOutputStream
- BufferedReader
- BufferedWriter
- ByteArrayInputStream
- ByteArrayOutputStream
- CharArrayReader
- CharArrayWriter
- DataInputStream
- DataOutputStream
- File
- FileInputStream
- FileOutputStream
- FileReader
- FileWriter
- FilterInputStream
- FilterOutputStream
- FilterReader
- FilterWriter
- InputStream
- InputStreamReader
- LineNumberInputStream
- LineNumberReader
- OutputStream
- OutputStreamWriter
- PipedInputStream
- PipedOutputStream
- PipedReader
- PipedWriter
- PrintStream
- PrintWriter
- PushbackInputStream
- PushbackReader
- Reader
- SequenceInputStream
- StreamTokenizer
- StringBufferInputStream
- StringReader
- StringWriter
- Writer

## java.net Package Support

TiJOS JDK contains standard java.net core package, including TCP, UDP, DNS network protocols related classes, like Socket and ServerSocket, DatagramSocket, URI, and so on.  Proxy, HTTP, URL related classes are not include so far.

The following list only lists the standard Java classes and interfaces supported by the TiJOS JDK, and you can refer to the standard Java documentation for specific use.

**Supported Class List **

- DatagramPacket
- DatagramSocket
- Inet4Address
- InetAddress
- InetSocketAddress
- RemoteSocket
- ServerSocket
- Socket
- SocketAddress
- URI

## java.util Package Support

The TiJOS JDK supports most of the classes in java.util, including collections, clocks, and so on, which do not support functions such as Locale, TimeZone, etc.

The following list only lists the standard Java classes and interfaces supported by the TiJOS JDK, and you can refer to the standard Java documentation for specific use.

**Supported Class List**

- AbstractCollection
- AbstractList
- AbstractMap
- AbstractMap.SimpleEntry
- AbstractMap.SimpleImmutableEntry
- AbstractQueue
- AbstractSequentialList
- AbstractSet
- ArrayDeque
- ArrayList
- Arrays
- BitSet
- Calendar
- Collections
- Date
- Dictionary
- GregorianCalendar
- HashMap
- HashSet
- Hashtable
- IdentityHashMap
- LinkedHashMap
- LinkedHashSet
- LinkedList
- Observable
- PriorityQueue
- Properties
- Random
- Stack
- StringTokenizer
- Timer
- TimerTask
- TreeMap
- TreeSet
- UUID
- Vector



## Summary

The above is the package and related classes supported in the current TiJOS JDK, which are the same usage as standard Java and are the most commonly used core classes in Java programming, we will gradually add more and more classes on requirements.

# TiJOS Framework 

The other large part of the framework class in the TiJOS JDK is to operate on hardware resources and sensor in the application, including the operation of various hardware interfaces and sensor, while also providing some of the tools that might be used, such as BASE64, JSON, and so on



## framework  Components

| Pakcage Name                      | Description                              |
| --------------------------------- | ---------------------------------------- |
| tijos.framework.platform          | System Settings related classes, like host name and other settings |
| tijos.framework.eventcenter       | Event center class, which deals with events from hardware peripherals such as GPIO events |
| tijos.framework.networkcenter     | Network center class, management network related configuration and status, such as: WLAN, DNS, etc |
| tijos.framework.devicecenter      | Device bus related classes, such as GPIO I2C, PWM, etc., can be used to develop the sensor which is not supported in the standard library |
| tijos.framework.sensor.button     | Button classes                           |
| tijos.framework.sensor.distance   | Range detection classes                  |
| tijos.framework.sensor.gas        | Gas sensing classes                      |
| tijos.framework.sensor.humiture   | Temperature and humidity sensing classes |
| tijos.framework.sensor.infrared   | Infrared classes                         |
| tijos.framework.transducer.buzzer | Buzzer classse                           |
| tijos.framework.transducer.led    | LED display classes                      |
| tijos.framework.transducer.relay  | Relay classes                            |
| tijos.framework.net.ntp           | Network time protocol client class       |
| tijos.framework.net.mqtt          | MQTT3.1.1 client                         |
| tijos.framework.ota               | Application online upgrade class         |
| tijos.util.base64                 | BASE64                                   |
| tijos.util.json                   | JSON                                     |
| tijos.util.logging                | Logger class, output to the print port   |



# More Resources

| Name                                     | Url                                      |
| ---------------------------------------- | ---------------------------------------- |
| TiJOS Web Site                           | <http://www.tijos.net>                   |
| TiJOS Community                          | <http://bbs.tijos.net>                   |
| TiJOS Introduction                       | <http://dev.tijos.net/overview>          |
| TiJOS Application Development Guide      | <http://dev.tijos.net/manual>            |
| TiJOS JDK API Document                   | <http://dev.tijos.net/javadoc>           |
| TiJOS Development Enviornment Setup Guide | <http://dev.tijos.net/setup>             |
| TiJOS JDK Software Examples              | <https://github.com/TiJOSteam/tijos-software-example> |
| TiJOS Hardware Access Examples           | <https://github.com/TiJOSteam/tijos-hardware-example> |
| TiKit-T600-ESP8266A Development Kit Manual | <http://dev.tijos.net/tikit/tikit-t600-esp8266a/> |
|                                          |                                          |