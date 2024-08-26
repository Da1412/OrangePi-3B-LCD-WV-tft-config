# OrangePi-3B-LCD-WV-tft-config
Explain 2 option  step for Orange Pi 3B with Waveshare 5 inch HDMI USB touch configuration (Works and tested with Ubuntu jammy and Orange Pi os (Arch)
====================================================
A). STEP 1
====================================================
1). download a image (Ubuntu jammy dekstop or Orange Pi os (Arch) on this website:
    http://www.orangepi.org/html/hardWare/computerAndMicrocontrollers/service-and-support/Orange-Pi-3B.html <br>
2). Burn and flash the image into SD Card using a BalenaEtcher (https://etcher.balena.io/).<br>
3). Once you've done with the flashing process, eject SD Card and insert to Orange Pi 3B SD Card slot. <br>
4). Booting process will begin. <br>
5). Clone or you can download directly from Orange Pi using chronium browser to this repo :
-----------------------------------------------------------------------------------------------------
``` sudo git clone https://github.com/Da1412/OrangePi-3B-LCD-WV-tft-config.git ``` <br>
``` chmod -R 755 OrangePi-3B-LCD-WV-tft-config ``` <br>
``` cd OrangePi-3B-LCD-WV-tft-config/ ``` <br>
-----------------------------------------------------------------------------------------------------
6). Execute driver's file according to LCD type (in this case LCD5-show) <br>
-----------------------------------------------------------------------------------------------------
``` sudo ./LCD5-show ``` <br>
-----------------------------------------------------------------------------------------------------
7). Before you execute driver files, i recommend to move file config-5.txt into your /boot directory. <br>
-----------------------------------------------------------------------------------------------------
```sudo mv config-5.txt /boot ```
-----------------------------------------------------------------------------------------------------
8). After you've done all that, the Orange Pi will reboot itself and the touchscreen should be working. <br>
 *NOTE: if the touchscreen is still messing around try download xinput-calibrator. <br>
 ----------------------------------------------------------------------------------------------------
 ``` sudo apt-get update ``` <br>
 ``` sudo apt-get install xinput-calibrator ``` <br>
 ``` xinput_calibrator ``` <br>
 ----------------------------------------------------------------------------------------------------
 And just follow the instruction on the screen. <br>
 IMPORTANT: do not change the Matchproduct "ads7846" line in /etc/X11/xorg.conf.d/99-calibration.conf <br>
 ----------------------------------------------------------------------------------------------------

 Touchscreen should be working by now. but if for some reasons the touchscreen is still not working, you can try using the following step.
 
 B.) STEP 2
 ================================================
 
