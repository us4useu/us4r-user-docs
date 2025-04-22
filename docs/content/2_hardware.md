(hardware/general)=
# Hardware description


(system-overview)=
## System Overview
The **us4R™** system is an ultrasound research device designed for transmission and acquisition of ultrasound signals using connected piezoceramic probes/transducers (use with pMUT/cMUT is feasible but may require a dedicated circuitry -- please consult us4us).

**The us4R™ is a peripheral device, so in addition to an ultrasound probe, it always requires an external Host PC to work.**

The us4R-lite™ is connected using PCIe cables ({numref}`us4r+pc`) to a PC running ARRUS™ SDK. 
An open-source ARRUS™ SDK (Software Development Kit) is provided to be installed and run on the host PC to execute User’s applications/scripting for device configuration, data acquisition, and custom processing.
  
The ready to use setup consists of the **us4R™** device, a host PC computer ({numref}`us4r+pc`), an LCD monitor and a set of cables.

```{figure} img/us4r+pc.jpeg
:name: us4r+pc
View of the us4R™ connected to the host PC.
```
**As standard, a host PC, an LCD monitor and ultrasound probes are not provided by the Manufacturer.**

(hardware/versions)=
## Hardware Models
The table below summarizes all hardware models of the us4R™:

:::{list-table} us4R™ Hardware Models
    :widths: 20 20 20
    :header-rows: 1

*   - Model
    - Options
    - External Interface
*   - R-2021 <span style="color:red">(EOL)</span>
    - 128RX, 192RX, 256RX
    - PCIe (4x or 8x gen3 4 lanes)
*   - R-2023
    - 128RX, 192RX, 256RX
    - PCIe (4x or 8x gen3 4 lanes)

:::

(hardware/probe-adapters)=
## Ultrasound Probe Adapters
The **us4R™** research system features changeable ultrasound probe adapter. Depending on the configuration, it can be equipped with an adapter supporting either a single ultrasound probe with up to 1024 elements or two probes (linear/phase/convex) with 256 elements each.
Two connectors (*CONN #0* and *CONN #1*) are situated at the top of the device; For matrix-array probe, an dedicated probe adapter is available with 4x DLM6-360 connectors.
Only a single probe (linear/phase/convex) probe connector is active at a time. An active probe is used to transmit and receive ultrasound signals that are acquired and processed by the system. 
The active connector/probe is chosen in software.


Several adapters are available for use with the **us4R™** system. Please
consult the list of adapters as shown below:

:::{list-table} Probe adapters 
:widths: 15 20 30
:header-rows: 1

*   - Options \*
    - Probes compatibility
    - Probe adapters
*   - 128 RX (4xus4OEM) 
    - up to 128-element probes (linear/array/convex) 
    - 
        - PAU (Ultrasonix Probe Adapter)
        - VPA (ATL/Philips Probe Adapter)
        - Custom Probe Adapter (on request)
*   - 192 RX (6xus4OEM) 
    - up to 192-element probes (linear/array/convex) 
    - 
        - EPA (Ultrasonix Probe Adapter)\**
        - PAU (Ultrasonix Probe Adapter)\**
        - VPA (ATL/Philips Probe Adapter)\**
        - Custom Probe Adapter (on request)
*   - 256 RX (8xus4OEM) 
    - up to 256-element probes (linear/array/convex) and up to 1024-element matrix-array probes
    - 
        - EPA (Ultrasonix Probe Adapter)
        - PAU (Ultrasonix Probe Adapter)
        - VPA (ATL/Philips Probe Adapter)
        - DLPx (GE/RCA Probe Adapter)
        - 2D MATRIX 2372 Vermon probe
        - Custom Probe Adapter (on request)
:::

*\* Switching between 4x, 6x and 8x us4OEM module options can be done by
the Manufacturer only.*

*\*\* Not easily interchangeable! If you plan to use probes above 128
elements from various manufacturers (e.g. Esaote and Philips probes) please contact us4us to find the best
solution for you.*

Depends on connector type, we offer the following adapters:

:::{list-table} Probe adapters 
   :widths: 20 20 20 50 40
   :header-rows: 1

*   - Connector <br>
    Type
    - Name
    - Rev
    - Supported Probes
    - List of tested probes
*   - QLC-260
    - EPA
    - 3.0
    - ESAOTE compatible <br>
    _up to 192-element probes <br>
    (linear/array/convex)_
    - 
        - SL1543 linear-array
        - AL2442 linear-array
        - SP2430 phased-array
        - AC2541 convex-array
*   - DL1-156
    - PAU
    - 1.0
    - ULTRASONIX compatible <br>
    _[up to 128-element probes (linear/array/convex)]_
    - 
        - L14-5/38 linear-array
        - L9-4/38 linear-array
*   - DL5-260
    - VPA
    - 1.0
    - ATL / Philips compatible <br>
    _[up to 128-element probes (linear/array/convex)]_<br>
    _in-probe MUX is not supported!_
    - 
        - L7-4/38 linear-array
        - C5-2 convex-array
*   - DLP-408
    - DLPx
    - 2.0
    - GE compatible <br>
    RCA compatible <br>
    _[up to 256-element probes (linear/array/convex/row-column)]_
    - 
        - GE L3-9i-D
        - RCA 128x128 & 64x64
*   - DL6-360
    - MAT-2732
    - 0.1
    - 2D MATRIX 2372 Vermon probe compatible <br>
    _[up to 1024-element probes (matrix-array)]_<br>
    _in-probe MUX is not supported!_
    - 
        - MAT 2372

:::

If you cannot find the adapter that suits your application, it is
possible to order a custom probe adapter from the us4us®. Please contact
us at <support@us4us.eu> to discuss the options.

:::{Note}
The system is supplied with one selected probe adapter. 
Additional adapters can be purchased separately.
:::


(hardware/inputs-outputs)=
## Inputs and outputs

The **us4R™** is equipped with:

-   up to 2 or 4 probe connectors (depends on the probe adapter
    installed),

-   4x or 8x PCIe ports (see {numref}`us4r-back`),

-   2x digital inputs,

-   2x digital outputs,

-   1x IEC mains power input.


```{figure} img/us4r-back.jpeg
:name: us4r-back
:alt: Back-side of the us4R™ device. 
Back-side of the us4R™ device.
```

**PLEASE NOTE:** External devices should be connected via cables no
longer than 3m.

(hardware/power-switch)=
## Power switch, cable and ON/OFF button

The power cable connection is shown in the picture below ({numref}`us4r-back-ac`).

```{figure} img/us4r-back-ac.jpg
:name: us4r-back-ac
The us4R™ AC power connector and ON/OFF button.
```
(hardware/connecting-probes)=
## Connecting ultrasound probes

Ultrasound probes require special care, as they can be easily damaged by
an impact. The damaged transducers could have internal element
short-circuits or open-circuits, both can cause malfunction or even
breakdown of the **us4R™** transmit circuitry. **Therefore, it is vital
that the probes are handled with extreme care and defective probes are
never connected to the system.**

Probes should be disconnected from the device during the transport.

The ultrasound probe connectors are situated at the top of the device.
2D probes (linear/phase/convex) connectors are marked as ***CONN #0***
and ***CONN #1*** on the figure below.

Please refer to section {numref}`Section %s <hardware/probe-adapters>` for other probe
adapters options.

```{figure} img/us4r-top-conn.jpg
:alt: Top-view of the us4R™ with 2D (linear/phase/convex) CONN #0 and CONN #1 connectors.
Top-view of the us4R™ with 2D (linear/phase/convex) CONN #0 and CONN #1 connectors.
```

A video instruction on how to change the probe adapter for 2D (linear/phase/convex) probes is available on our YouTube channel:

[![A picture containing text, electronics, display Description automatically generated](img/us4r-lite-change-adapter-video.png)](https://www.youtube.com/watch?v=v9DwhbGclBE)

**PLEASE NOTE:** Only a probe prepared and configured for use with the **us4R™** can be connected to the device. For assistance, please contact the Manufacturer.

```{Caution}
Using non-compatible or broken probes can result in damage to the transmission section of the us4R-lite™!
Such damages are NOT covered under the warranty!
```
(hardware/pcie-ports)=
## PCIe ports 

The **us4R™** is equipped with 4 or 8 PCIe ports on the back of the
device.

The PCIe ports are intended for connecting the system to an external host PC using dedicated PCIe cables. The **us4R™** is provided with compatible host PCIe adapter card(s) that should be properly installed in the host PC controller before first use. For the PXH832 PCIe adapter cards follow the instructions available [here](https://www.dolphinics.com/download/PX/OPEN_DOC/PXH832_users_guide.pdf) 

### Connecting the PCIe cables

The delivered PCIe cables are marked #1 to #4 or #8, to help with proper
connection of the **us4R™** ports numbered 1...4 or 1...8 to the
corresponding ports on the host PC side -- also numbered. **The proper
order of the PCIe cables is essential for device operation and cannot be
changed!**

When connecting the PCIe cables you should hear/feel "a click" to be
sure that the connector is latched properly ({numref}`us4r-back-cables`).

```{figure} img/us4r-back+cables.jpg
:name: us4r-back-cables
Back panel of the us4R™ showing the PCIe connectors and properly connected cabling. 
```
### Connecting host PC & display

The **us4R™** requires an external host PC with an LCD monitor to function correctly. The only way to connect the **us4R™** device to the PC is through the PCIe cables.

The host PC must be equipped with one or two PCIe adapter cards. Example of the host PC with two PCIe adapter cards installed -- one at the top, one at the bottom of the enclosure ({numref}`pc-back-cables`).

```{figure} img/pc-back+cables.jpeg
:name: pc-back-cables
Back-side view of the host PC showing cables connection with two PCIe adapter cards installed.
```
To disconnect PCIe cables pull the green tab at the bottom of the PCIe cable plug ({numref}`pc-pcie-cables`).

```{figure} img/pc+pcie-cables.jpeg
:name: pc-pcie-cables
The host PC: the PCIe cables #1..#4 connected to the bottom PCIe interface card. Disconnect by pulling the green tab.
```

```{figure} img/pcie-cables-5678.jpeg
:name: pcie-cables-5678
The host PC: the PCIe cables #5..#8 connected to the top PCIe interface card.
```

## Digital I/O ports

The **us4R™** provides four digital I/O signals in the LVTTL 3.3V
standard available on the SMA-type connectors:

1.  CLOCK IN -- input of an external reference clock signal.

2.  TRIG IN -- input of an external trigger signal -- can be used to
    synchronize transmit events with other devices/systems.

3.  CLOCK OUT -- output of an internal reference clock signal.

4.  TRIG OUT -- output of an internal trigger signal -- can be used to synchronize other external devices/systems with the **us4R™**.


```{figure} img/us4r-back-io.jpg
:name: us4r-back-io
Back panel of the us4R™ showing the 4x digitial I/O signals
```
