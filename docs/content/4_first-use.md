# First Use
(set-up/unboxing)=
## Unboxing and setting-up the device

The device is delivered to the user pre-assembled and boxed.

The unboxing of the device should be performed with utmost care.

The user must connect the components and set up the entire system as described in this section before running the first acquisition.

:::{Caution}
If the device was placed in an environment with climatic conditions that sharply diverge from normal office conditions, it should undergo a process of acclimatization before the first use. This comprises of leaving the device out of the transport packaging for a minimum of 12 hours.
:::

The packaging should include:

-   **us4R™** device (with probe adapter) -- 1 pcs.;
-   PCIe cables -- 4 or 8 pcs.;
-   PCIe adapter card -- 1 or 2 pcs.;
-   mains power cable -- 1 pcs.;
-   PCIe cable ferrites -- 8 or 16 pcs.;
-   (optional) PC system controller -- 1 pcs.;
-   (optional) ultrasound probe(s).

In case of any missing items, the Customer is advised to contact the
Manufacturer.

Before the first use, it is necessary to ensure that the room has ample
space, stable ground and 120/230VAC mains power source with a protective
bonding.

The device should be placed to facilitate a safe operation: the power
cables must be neither strained nor hanging too loose in a manner that
may lead to tripping, wrenching out of cables or otherwise damaging them
through breaking or cutting.

Procedures using the **us4R™** should not be performed if the device is
in proximity to another working ultrasound device. Ultrasound probes can
cause interference, resulting in a falsification of the image.

A proper operation of the device is described in the next chapters of
this manual.

:::{Caution}
The power cable should be plugged into the 120V,60Hz or 230V,50Hz mains power supply with a protective bonding.
:::
## Power supply connection

:::{Caution}
The 120/230VAC power socket used to power the us4R™ must be equipped with a protective earth wire. It is imperative to ensure that the electrical system provides the fire protection required for the class I devices.
:::

A loss of mains power during operation will result in an immediate shutdown of the device. The us4R™ will enter standby mode
once the mains power is restored. ON/OFF button must be pressed to power the us4R™ back on. After power on the host PC must 
be restarted to restore the communication with the system.

:::{Caution}
To shut down the us4R™ in case of malfunction, remove the mains power cable from the electrical socket. The electrical sockets should be situated in proximity to the device and be easily accessible.
:::


(set-up/probe-adapters)=
## Probe Adapters

Several adapters are available for use with the **us4R™** system. Please ensure that your device is equipped with one. The list of adapters can be found in Ultrasound Probe Adapters section (see: {numref}`Section %s <hardware/probe-adapters>`).

Always keep the ultrasound probe connected to the **us4R™** system during operation. It is required for the proper functioning of the device.

:::{Caution} 
Never unplug the probe from the device during transmission, and never transmit with no load! This can result in damage to the transmission unit of the us4R™. 
:::


(set-up/system-setup)=
(set-up/System setup)=
## System setup

The **us4R™** should be positioned so that operation is safe --- i.e. on
a stable, flat surface in a place with no risk of spillage on the device
and away from the sources of interference and radiation. To limit unintentional radiation from the device, ferrites for PCIe cables should be mounted on each cable, on both sides of the PCIe cable and as close to the connectors as possible. The external
power supply and/or power strip should be placed nearby the device. 

<!-- For more details
see section: {numref}`Section %s <hardware/general>`. -->

The heat is dissipating by the **us4R™**  system during normal work
conditions and may slightly increase the temperature of the device
surroundings. The ventilation holes on each side of the device must
remain uncovered to ensure free flow of air. Covering the ventilation
holes risks overheating, shutting down or damaging the **us4R™.** The
power and probe cables must not be strained or hang too loosely in a
manner that may lead to tripping, mechanical damage, wrenching the
cables out of the socket and/or damaging them through breaking or
cutting. The audio frequency noise is coming from the fans and sometimes
from the HV power supply during transmit during normal work conditions.

Please consult the Manufacturer guidelines in section {numref}`Section %s <guidelines/general>`.

(setup/software-installation)=
## Software installation and firmware update

The device is delivered with the current stable version of the firmware pre-installed.

User has to prepare his host PC only:
1. Check and install the PCIe adapter card as described in the {numref}`Section %s <hardware/pcie-ports>`.
2. Install the required software according to instructions provided [here](https://us4useu.github.io/arrus-toolkit/content/installation/index.html).


If, for any reason, a firmware update is required, please follow the instructions provided [here](https://us4useu.github.io/arrus-toolkit/content/installation/index.html#firmware).
Always ensure that compatible software, firmware, and hardware components are used; otherwise, when running the examples, a version incompatibility message for the software and firmware will appear.

Links to the ARRUS™ SDK package documentation are available
[here](https://github.com/us4useu/arrus).


(setup/system-running)=
## Running the acquisition

Before first run of the acquisition, you must ensure that:

* The device has been set up according to the manufacturer's guidelines from {numref}`Section %s <guidelines>`, and all steps described in the sections from {numref}`Section %s <set-up/unboxing>` to {numref}`Section %s <setup/software-installation>` are ensured.
* Proper probe adapter has been installed.
* An external host PC has been prepared (all required software and drivers are installed).

Step-by-step instruction:

1. Connect the mains to the **us4R™** and turn the *Power Switch* on.
2. Connect the ultrasound probe.
3. Connect the **us4R™** to the host PC
4. Now, turn on the **us4R™** device by clicking the ON/OFF button.
5. Turn on the host PC (it is crucial for proper functioning to turn on the **us4R™** prior to turning on the host PC).
6. Before login check the color of the LEDs on the back of the PCIe card(s) -- all 4 or 8 LED indicators (from the top and/or bottom card) should light up GREEN, see {numref}`pcie-cables-1234`.

```{figure} img/pcie-cables-1234.jpeg
:name: pcie-cables-1234
:scale: 6 %
:alt: The PCIe card interface.

The host PC: the PCIe card interface with four connected PCIe cables and the PCIe links LEDs.
```

>IMPORTANT NOTE: If any of the LED indicators light up ORANGE, please reboot the PC. Keep rebooting until both LEDs turn green.

7.  Make sure to check that the device and its software is starting correctly. If any errors are signaled by the device or messages displayed on screen, proceed according to instructions.

8.  Follow the instruction on how to run "PWI 3D" example script on your setup. Python example is provided [here](https://github.com/us4useu/arrus/tree/master/api/python/examples/pwi_3d.py).
**Please remember to use the provided configuration file (.prototxt)** -- set the appropriate path to the session configuration file in the `arrus.Session` constructor.

9.  Once the test is over, close the image window.

10. The host PC can now be turned off by shutting down the operational system as normal.

11. Turn off the **us4R™** by pressing the ON/OFF button.

12. After 5 seconds turn off the Power Switch.


:::{CAUTION}
Never unplug the probe from the device during transmission, and never transmit with no load!
This can result in damage to the transmission unit of the us4R™.
:::

:::{CAUTION}
Running the **us4R™** device with the proper configuration file is crucial. Always ensure that the parameters entered there are correct and aligned with the intended ones, especially those concerning the probe adapter and the desired transmission voltage.
In extreme cases, using incorrect parameters can result in damage to the transmission unit of the **us4R™**
:::

## Setting high-voltage (HV) supply for the transmitters

:::{Caution}
Voltages above 46.7VAC peak or 70VDC constitute a life hazard according to EN 61010-1 and great care must be takes when using the power supply at voltages above this level!
:::

The system TX voltage (so called HV -- High Voltage) is one of the most
crucial parameters from the system/probe safety point of view. Because
the **us4R™** is a research system, it enables the user to change many TX parameters (TX scheme, PRF, TX voltage, pulse length, etc.).

**However, some combinations of the TX parameters can be dangerous for
the connected ultrasound probe and/or the system itself!** 

Therefore, the user is fully responsible for verifying a safe set of TX parameters that can be used with the connected probe in a given application. Our recommendation is to start experimenting with lower HV voltages, e.g., 10V instead of 50V, and gradually increase the voltage after ensuring that the signal from all transducer elements is received correctly.
%CZY MAMY PRZYKŁAD JAK SPRAWDZIĆ NA NITCE CZY WSZYSTKIE KANAŁY WIDAĆ OK?

**Application of an excessive TX voltage or power to the probe can
(will) result in damage to the system and/or the probe!**

We strongly advise to use the lowest TX voltage possible -- as low as
reasonably achievable (ALARA rule). Also, please consult us4us® and the
probe producer to get advice on the max TX voltage and power that can be
delivered to the probe.
