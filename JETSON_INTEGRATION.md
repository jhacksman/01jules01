# NVIDIA Jetson Orin Nano Integration Approach for Boxer

This document outlines the planned approach for integrating an NVIDIA Jetson Orin Nano as a replacement backpack PC on the Clearpath Robotics Boxer AMR.

## Connection Strategy:

The primary connections between the Boxer base unit and the Jetson Orin Nano will be for data and power.

1.  **Data Connection (Ethernet & ROS 2):**
    *   The Boxer's internal computer exposes a ROS 2 API over an Ethernet connection.
    *   Connect the NVIDIA Jetson Orin Nano's Ethernet port to the Boxer's available Ethernet port on the attachment interface panel.
    *   The Jetson will then communicate with the Boxer's systems (locomotion, sensors, safety) via this ROS 2 API, similar to how the original backpack PC operated.
    *   Refer to the Clearpath Boxer User Manual for details on the ROS 2 topics and services available.
    *   The Boxer's Ethernet port may offer Power-over-Ethernet (PoE). While the Jetson Orin Nano Developer Kit can be powered by PoE (802.3at, ~25W), it's essential to verify if the Boxer's port supports this standard and if the power provided is sufficient for your intended Jetson workload. Relying on the 37-pin connector for main power is advisable for robust operation.

2.  **Power Connection (37-Pin Connector):**
    *   The primary source of power for the Jetson Orin Nano will be the 37-position D-sub connector on the Boxer's attachment interface. This connector is known to provide power to the original backpack PC.
    *   **CRITICAL UNKNOWN:** The exact pinout (which pins provide voltage and ground) and the power specifications (voltage level - e.g., 12V, 24V, 48V; and maximum current available) for this 37-pin connector are **currently unknown.** This information is essential for safely powering the Jetson.
    *   **Jetson Orin Nano Power Requirements:** The Jetson Orin Nano Developer Kit typically requires a DC power supply (e.g., 9V-20V, depending on the specific model and carrier board; some can run on 5V but it's less common for the Nano). The power consumption will vary with workload (typically 5W-15W for the module, but the dev kit might consume more).
    *   **Voltage Regulation:** Depending on the voltage supplied by the Boxer via the 37-pin connector, a DC-DC voltage regulator may be required to step the Boxer's output voltage up or down to a level compatible and safe for the Jetson Orin Nano.

## Action Required: Determine 37-Pin Connector Specifications

Before connecting any custom wiring, you **MUST** determine the correct pinout and power specifications of the 37-pin connector. Incorrect wiring can damage the Boxer, the Jetson, or both.

Recommended methods to find this information:

*   **Contact Manufacturer Support:**
    *   Reach out to OTTO Motors (Rockwell Automation) or Clearpath Robotics customer support. They are the most likely sources for the "OTTO 100 V2.5 Operation and Maintenance Manual" or direct pinout details for the attachment connector.
*   **Search Online Communities:**
    *   Post queries on robotics forums such as the ROS Discourse (discourse.ros.org) or other AMR-related communities. Other users or integrators may have encountered this and shared information.
*   **Inspect Any Existing Cabling:**
    *   If you have any cables that previously connected to the Boxer's 37-pin port (even if disconnected from the old backpack PC), inspect them carefully for any labels, wire colors, or markings that might give clues about pin functions. (Use a multimeter to check for continuity or existing voltages **with extreme caution** and only if you are experienced with electronics).
*   **Professional Assistance:**
    *   If you are not comfortable with electronics, consider seeking help from a qualified technician or robotics integrator.

## Motion Stop Loop:

*   The Boxer Integration guide mentions that the 37-pin connector has two pre-populated wires that complete the robot's "Motion Stop loop." This safety feature allows the robot to move.
*   When designing your interface to the 37-pin connector, ensure that this motion stop circuit remains correctly wired (either passed through your new connector or re-established if you modify the existing plug).

Once the power specifications from the 37-pin connector are known, and a suitable power regulation strategy for the Jetson Orin Nano is designed, you can proceed with the physical integration.
