# Blink

A semantically aware data translator for SCADA applications.

Instead of being a simple data converter, blink is capable of interpreting the data that you are using
into intended uses.  This allows end devices to be written with much less difficulty.

# Services
There are 4 primary services with the blink device.

* The Data service
* The License service
* The Status service
* The Configuration Service

Each advertise under their own specific uuid and can be discovered separately. 



## Data Service
The data service creates a bank of characteristics, dynamically sized to allow data
to be sent.  This is the main routine.

## Status Service

The Status service will let the client know what sort of state the blink is currently in.

* Error, with error code
* Reading Data
* Serving Data


###

## License Service

This service reads and writes license info 


## Configuration Service
This service allows things like wifi and tried baud rates to be changed.
