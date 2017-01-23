Blink BLE Services
-------------------

The Blink BLE platform is comprised of several categories of services.


+ Scada Device access
+ Authentication
+ Authorization
+ Update

# Scada Device Access

* Currently there is only one supported Scada Service.
  That is, the Fisher Roc line of devices.

* The ROC record is encoded using Googles Protobuffer system.
  This is a nice standard way of encoding data which has tight 
  space and version requirements.
  
* Every new SCADA line will have its own service and protobuffer.  

## Fisher Roc Bluetooth record

