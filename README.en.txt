==========================================================================
          ePOS-Print SDK for iOS  Version 1.10.1

          Copyright Seiko Epson Corporation 2012-2015 All rights reserved.
==========================================================================

1. About this software

The ePOS-Print SDK for iOS is an SDK aimed at development engineers who 
are developing iOS applications for printing on an EPSON TM printer.
Applications are developed using the APIs provided by ePOS-Print SDK.
ePOS-Print SDK for Android for Android devices is also provided in 
ePOS-Print SDK.
For detailed information, please see ePOS-Print SDK for iOS User's Manual.

iOS Versions
  iOS 4.2 to 4.3.5
  iOS 5.0 to 5.1.1
  iOS 6.0 to 6.1.6
  iOS 7.0 to 7.1.2
  iOS 8.0 to 8.0.2
  iOS 8.2 to 8.4.1
  iOS 9.0 to 9.1

iOS Devices
  iPhone ( 3G / 3GS / 4 / 4S / 5 / 5c / 5s / 6 / 6 Plus / 6s / 6s Plus )
  iPod touch ( 2nd generation / 3rd generation / 4th generation / 5th generation
  / 6th generation )
  iPad / iPad2 / iPad ( 3rd generation / 4th generation ) / iPad Air / iPad Air 2
  iPad mini / iPad mini 2 (iPad mini with Retina display) / iPad mini 3
  / iPad mini 4

Supported Printers
  EPSON TM-T88V
  EPSON TM-T70
  EPSON TM-T70II
  EPSON TM-T20
  EPSON TM-T82
  EPSON TM-T81II
  EPSON TM-T82II
  EPSON TM-U220 series
  EPSON TM-P60
  EPSON TM-P60II
  EPSON TM-T90II
  EPSON TM-T20II
  EPSON TM-P80
  EPSON TM-U330 series
  EPSON TM-P20
  EPSON TM-m10
  EPSON TM-m30

Supported Interfaces
  Wired LAN
  Wireless LAN
  Bluetooth


2. Supplied Files

- ePOS-Print.h
  Header file that includes class definitions and error value / device type 
  constant definitions.
- ePOSEasySelect.h
  Header file for selecting a printer easily.
- ePOSBluetoothConnection.h
  Header file that includes bluetooth connection class definitions and error value.
- libeposprint.a
  Library for function execution. (armv6, armv7, armv7s, arm64, i386, x86_64 supported)
- libeposeasyselect.a
  Library for selecting a printer easily.(armv7, armv7s, arm64, i386, x86_64 supported)
- ePOS-Print_Sample_iOS.zip
  A sample program file.
- EULA.en.txt
  Contains the SOFTWARE LICENSE AGREEMENT.
- EULA.jp.txt
  Contains the SOFTWARE LICENSE AGREEMENT. (The Japanese-language edition)
- ePOS-Print_SDK_iOS_en_revR.pdf
  A user's manual.
- ePOS-Print_SDK_iOS_ja_revO.pdf
  A user's manual. (The Japanese-language edition)
- ePOS-Print_SDK_iOS_AppDevGuide_E_RevA.pdf
  A developer's guide
- ePOS-Print_SDK_iOS_AppDevGuide_J_RevA.pdf
  A developer's guide (The Japanese-language edition)
- README.en.txt
  This file.
- README.jp.txt
  The Japanese-language edition of this file.

3. Remarks

- For detailed information, please see ePOS-Print SDK for iOS User's Manual.

- Under TCP/IP connection at iOS9.x, set the default gateway address to the network router.

4. Modification from the old version

  Version 1.10.1
    - Added the support iOS version.
      - iOS 9.0 to 9.1
    - Added the support iOS Devices.
      - iPhone 6s
      - iPhone 6s Plus
      - iPod touch 6th generation
      - iPad mini 4

  Version 1.10.0
    - Added the support printers.
      - TM-m30
    - Bug Fixed.
      - When application prints a compressed image data, if image data having a size larger than the printing area,
        it can not be printed correctly. (Horizontal width of approximately 700 dot - 1000 dot)
      - At printing process. If the system notify signal to the application before process returns from the SDK, print error may occur.
      - At the printer that supports interrupt printing function. When the printer prints graphics from some smart device, print error may occur.

  Version 1.9.0a
    - Added the support iOS version.
      - iOS 8.4
    - Bug Fixed.
      - In ePOSReceiptPrintSample, when the TM-T88V is to print on the paper of the paper width 58mm,
        a new line enters the middle of a line.

  Version 1.9.0
    - Added the support iOS version.
      - iOS 8.3
    - Added the beginTransaction API for beginning transaction.
    - Added the endTransaction API for ending transaction.
    - Added the getStatus API for getting the printer status.
    - Added the support printers.
      - TM-m10
      - TM-P80 Autocutter model
    - Bug Fixed.
      - Under Bluetooth connection, application may crash if application calls the openPrinter
        immediately after the closePrinter, during the 2-5 seconds after the printer turn off.

  Version 1.7.1
    - Bug Fixed.
      - Under Bluetooth connection, the openPrinter method may fail if application calls it immediately
        after the closePrinter method.

  Version 1.7.0
    - Added the Bluetooth connection and disconnection APIs.
    - Added the support iOS version.
      - iOS 8.2
    - Added the support iOS Devices.
      - iPad Air 2
      - iPad mini 3
    - Added the support languages.
      - Indian
    - Improved the openPrinter API.
      - The openPrinter method succeeds even if the small letter is specified for the MAC address.
        (Only Bluetooth connection)

  Version 1.6.0a
    - Added the support iOS version.
      - iOS 8.0 to 8.0.2
    - Added the support iOS Devices.
      - iPhone 6
      - iPhone 6 Plus
    - Supported the SamplePrograms on iOS8.

  Version 1.6.0
    - Added the support printers.
      - TM-P20
    - Added an printer search API for getting the device name.
    - Added the support iOS version.
      - iOS 7.1.2
    - Added the openPrinter API for timeout settings.
    - Improved the openPrinter API.
      - Not only IP address also MAC address or the host name can be set to the deviceName.
        (Only TCP/IP connection)
    - Improved the log function.
      - Compression of the backup file.
      - Improved the output content.
    - Specification change.
      - openPrinter returns an error after specified time passed if the target
        printer is already opened. (Only TCP/IP connection)

  Version 1.5.0
    - Added the support iOS version.
      - iOS 7.1 to 7.1.1
    - Added the support printers.
      - TM-U330
    - Added an API for compression image data processing.

  Version 1.4.2
    - Bug Fixed.
      - Status when calling sendData method was incorreect.

  Version 1.4.1
    - Bug Fixed.
      - The openPrinter and sendData method causes one second delay,
        when printer doesn't have a battery.
    - Improved the status monitoring function.
      - Improved the communication efficiency of status acquisition.
    - Bug Fixed.
      - Added the support API of TM-P80 the addCut, addFeedPosition, addLayout API.

  Version 1.4.0
    - Added the support interface.
      - Bluetooth

  Version 1.3.5
    - Added the support iOS version.
      - iOS 7.0.4
    - Added the support iOS Devices.
      - iPad mini with Retina display
    - Improved the printer search function for iOS 7.

  Version 1.3.4a
    - Added the support iOS Devices.
      - iPad Air

  Version 1.3.4
    - Added the support iOS version.
      - iOS 7.0 to 7.0.3
    - Added the support iOS Devices.
      - iPhone 5c
      - iPhone 5s
    - Bug Fixed.
      - The closePriner method may fail during printer status monitoring.
      - When printer is offline, the openPrinter method may not return 
        the correct printer status under Bluetooth connection.

  Version 1.3.3
    - Improved the text printing speed.

  Version 1.3.2
    - Added the support printers.
      - TM-T20II
      - TM-P80

  Version 1.3.1
    - Added the support printers.
      - TM-T90II

  Version 1.3.0
    - Added the log output function.
    - Added the support printers.
      - TM-T70II
    - Added the support iOS version.
      - iOS 6.0.2 to 6.1.4

  Version 1.2.0
    - Added a command generation API for controlling the label.
    - Added a command generation API to set the paper layout.
    - Added the support printers.
      - TM-T82II
    - Added the support iOS version.
      - iOS 6.0.1
    - Added the support iOS Devices.
      - iPad ( 4th generation )
      - iPad mini

  Version 1.1.0
    - Added the printer status monitoring function.
    - Added the halftone method for raster graphic printing.
    - Support multiple tone printing.
    - Added the support languages.
      - Simplified Chinese
      - Traditional Chinese
      - Korean
      - Thai
      - Vietnamese
    - Added the battery status monitoring function.
    - Added the support printers.
      - TM-T20
      - TM-T82
      - TM-T81II
      - TM-P60II
      - TM-P60 (Wireless LAN)

  Version 1.0.1
    - Added the support iOS version.
      - iOS 6.0
    - Added the support iOS Devices.
      - iPhone 5
      - iPod touch ( 5th generation )
      - iPad ( 3rd generation )

  Version 1.0.0
    - New release. 
