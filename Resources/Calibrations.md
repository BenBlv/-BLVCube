### Navigation
[Overview](Resources/Overview.md) | [Start](Resources/Start.md) | [Bill of Materials (BOM)](Resources/BOM.md) | [Download & Print](Resources/Download_&_Print.md) | [Assembly Guide](Resources/Assembly_Guide.md) | [Wiring](Resources/Wiring.md) | [Calibrations](Resources/Calibrations.md) | [Community Remixes](Resources/Remixes.md) | [License](#license)


# CALIBRATIONS

This is the calibration step. Before starting the calibration process, ensure the appropriate firmware is installed on your Duet board. The Duet board initially ran Reprap 2.x.x when the project was released but has since been upgraded to Duet 3 running Reprap firmware v3.x.x. If you are still using the Duet 2 WiFi board, check out David Husolo’s GitHub for a well-calibrated configuration file for both Duet 2 WiFi and Duet 3 running Reprap 3.x.x.

The following steps will refer to the excellent Duet guide platform. With these guides, you will be able to calibrate your board and achieve high-quality prints.

---

## UPDATING YOUR DUET FIRMWARE

Before using any BLV mgn Cube firmware configuration files, make sure your Duet board is running the updated Reprap firmware 3.x.x. Duet boards have extensive documentation, including step-by-step guides for almost everything. 

1. **Download the latest firmware**: [Download Here](#)
2. **Follow the firmware updating guide**: [Guide](#)

After updating, copy the basic BLV Config files onto your SD card. If the SD card is new or empty, reconstruct it using the provided guide. Inside the project’s zip file, there are SD content zip files for Duet 3 and the old Reprap version 2.x.x. If you’ve updated to version 3.x.x, use David Husolo’s config files from his GitHub. 

If you have the FYSETC kit, you can use the firmware provided by FYSETC.

The Duet has an internal web interface for full printer control. After updating, configure your network settings to access your board.

[Network Setup Guide](#)

---

## WARNINGS

Important do's and don'ts to protect your hardware:

- Never disconnect cables from your Duet board when connected to power, except for the USB cable.
- Avoid short circuits, especially with fan wires, motors, and heaters.
- Do not supply more than 24 volts to your board.
- Ground the frame, bed carriage, and motors.
- Be careful not to damage the electronics when installing.
- Never remove the memory card while the printer is running.
- Use a multimeter to check your crimped connectors.
- Triple-check the polarity of wires.
- Do not manually move axes with stepper motors connected.

---

## CONFIGURING YOUR BLV 3D PRINTER

Although the provided config files cover most settings, you may need to make changes, such as bed centering, motor directions, macros, and temperature settings.

- [Full Duet 2 WiFi Guide](#)
- [Full Duet 3 Guide](#)
- [Reprap 3 Overview - Must Read](#)

### Guides to Follow:

- **Centering Your Bed**: [Guide](#)
- **Testing Endstop Switches**: [Guide](#)
- **Setting Up a Different Z Sensor**: [Guide](#)
- **Setting Up PT100 Sensor**: Only if using PT100 [Guide](#)

### Stepper Motor Setup

- If you have the FYSETC kit, skip this section.
- If using BOM or Blurolls kit motors, follow these steps:

1. **Identify Coil Wires**: Each stepper has 4 wires (2 per coil). [Identification Guide](#)
2. **Connect Your Steppers**: Follow the Duet wiring diagram.
3. **Test and Configure**: Use the Duet documentation. [Testing Video](#)

Additional configuration guides:
- **Tuning Stepper Motor Drivers**
- **Mesh Bed Compensation**
- **Multiple Independent Z Motors Setup**
- **Filament Sensor Setup**
- **PT100 Sensor Setup**

---

## CALIBRATIONS

Follow these essential calibration steps carefully to ensure optimal performance.

### Hotend PID

To perform PID tuning for your hotend:

1. Use the latest beta firmware (3.x.x).
2. Define tools (T0) and fans correctly.
3. Run the command: `M303 T0 S200` (replace 200 with your usual printing temperature). Ensure the layer fan is off, as the new algorithm adjusts heater settings automatically.

---

## OPTIONAL CALIBRATIONS

Consider calibrating these features:

- **Reducing Standby Noise**: Minimize motor noise.
- **Stall Detection and Sensorless Homing**
- **Pressure Advance**: Compensate for filament elasticity.
- **Resume Print After Power Failure**
- **Experimental Accelerometer**: Identify ringing frequencies for DAA.

---

## USEFUL GUIDES

- **Macros**: How to use macros with Reprap firmware.
- **Adding External Buttons & Customizing the Web Interface**
- **G-code Dictionary**: Comprehensive list of supported G-codes.
- **Duet Community Projects**

---

*Bottom of Page*

