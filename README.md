# Blink

A semantically aware data translator for SCADA applications.

Instead of being a simple data converter, blink is capable of interpreting the data that you are using
into intended uses.  This allows end devices to be written with much less difficulty.

# Services
There are 4 primary services with the blink device.
Each has its own advertising string and primary data type

* The Data service
* The License service
* The Status service
* The Configuration Service
* The Write Service
Each advertise under their own specific uuid and can be discovered separately. 



## Data Service
The data service creates a bank of characteristics, dynamically sized to allow data
to be sent.  This is the main routine.
* Advertisement UUID: `aa4d6e22-badf-4983-8b45-04b9f55f6e0a`
* Primary Data Type: MeterRunPeriodicReport

## Write Service

Write data to a PLC 

* Advertisement UUID: `2b1af31f-1c10-483f-b27c-41bad18e3286`
* Primary Data Type : WriteValue

### Uses
* reset device and data

## Status Service
The Status service will let the client know what sort of state the blink is currently in.

+ Advertisement UUID: `0c139d79-a034-4884-9bcb-6401b746c66d`
+ Primary Data Type : BlinkStatus
+ Extra info held in the status:
  * Current Epoch Time on the Roc Device
  * Battery Percent as a decimal (1.0 being 100% charged)
  * Charge Amps in mA

### Status Examples
* Error, with error code
* Checking Time
* Checking Battery
* Reading Data
* Serving Data



###

## License Service

This service reads and writes license info 


## Configuration Service
This service allows things like wifi and tried baud rates to be changed.

* Service UUID: `a9d064dd-6635-4a1f-97f9-4dd34132be86`
* Primary Data Types : RocConfiguration and RocVersion

### Characteristics

* Read `Restart blink process` UUID: `da892460-e203-4937-80b0-172cc3f892d9`
* Read  `RocVersion`           UUID: `e12ab614-da73-42af-81e6-0a9311b076ba`
* Read  `RocConfiguration`     UUID: `a4519451-5837-4687-873f-0dfef0a9a1b9`
* Write `RocConfiguration`     UUID: `b2dd0114-7dc8-4c64-800e-1ea0e8ddf1a2`

