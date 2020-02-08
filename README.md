# vera-tp-link-hs1xx

Implementation file for Vera home automaton system and TP-Link HS1xx WiFi-plug integration

## Installation ##

Upload implementation file I_TP-Link-HS1xx-Switch.xml to Vera via the Web UI from menu :
Apps->Develop apps->Luup files->Upload

Then you can create the TP-Link HS1xx device using this URL from browser, filling in appropriate values to VERA-IPADDRESS and PLUG-IPADDRESS.

http://VERA-IPADDRESS:3480/data_request?id=action&serviceId=urn:micasaverde-com:serviceId:HomeAutomationGateway1&action=CreateDevice&deviceType=urn:schemas-upnp-org:device:BinaryLight:1&internalID=&Description=TP-Link%20HS-1xx&UpnpDevFilename=D_BinaryLight1.xml&UpnpImplFilename=I_TP-Link-HS1xx-Switch.xml&RoomNum=0&Reload=1&IpAddress=PLUG-IPADDRESS

TP-Link-HS1xx needs to have static IP assigned in the router it connects to and the Kasa (TP-Link) app should not be used as connecting may disable the local mode this 
Tested on Vera Edge using HS100 V2.0 SW version 1.5.4 Build 180815 Rel.121440

## Other Information ##

The implementation uses the same Smart Home protocol as this python tool
https://github.com/softScheck/tplink-smartplug

That is very useful tool for setting up the plug initially

   `tplink_smartplug.py -t 192.168.0.1 -j '{"netif":{"set_stainfo":{"ssid":"<WIFI SSID>","password":"<WIFI PASSWORD","key_type":3}}}'`


Discussion on Vera forums :
https://community.getvera.com/t/tp-link-smart-plug-hs110/193678/9
