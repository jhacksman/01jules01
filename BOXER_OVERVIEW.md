# OTTO 100 SDV Boxer Overview

This document provides an overview of the Clearpath Robotics Boxer, which is based on the OTTO Motors OTTO 100 Self-Driving Vehicle (SDV) / Autonomous Mobile Robot (AMR).

## Key Information:

*   **Base Platform:** The Boxer is an industrial-grade mobile robot derived from the OTTO 100 AMR. It is designed for research and development of robotics applications, particularly those requiring integration of custom payloads.
*   **"Yellow Stripe" Variant:** Research indicates that a "yellow stripe" on the robot is likely a cosmetic distinction or related to a previous specific payload/configuration from a prior owner. Current documentation for the Boxer and OTTO 100 does **not** describe a "yellow stripe" version with a fundamentally different accessory or backpack PC interface compared to the standard models (V2.4, V2.5). Any unique interfacing aspects would likely be part of the removed custom payload, not the base robot itself.
*   **Backpack PC Interface:** The Boxer is designed to be augmented with a "Backpack Computer" for user software and peripheral integration. Since your unit is missing this PC, you will need to interface your NVIDIA Jetson Orin Nano with the robot's existing connection points. These are:
    *   **Ethernet Port:** A standard RJ45 Ethernet connection. This is the primary way to communicate with the robot's internal computer using the ROS 2 API. This port may also provide Power-over-Ethernet (PoE), which could potentially power a low-power device, but this needs to be verified.
    *   **USB Type-A Port:** A standard USB port, likely for connecting peripherals to the backpack computer.
    *   **37-Position Connector:** A D-sub style connector (specifically, a TE Connectivity 206305-1 receptacle on the robot side) that provides power and other signals for the backpack PC and other payloads. The detailed pinout for this connector is critical for integrating a custom compute solution and is typically found in the "OTTO 100 Operation and Maintenance Manual." This connector also includes a pre-wired motion stop loop that must be maintained for robot operation.

## Versions:

*   The Boxer (and underlying OTTO 100) has different versions (e.g., V2.4, V2.5 mentioned in manuals). These versions may have minor differences (like the location of an E-stop button) but the core backpack interface architecture (Ethernet, 37-pin connector) appears consistent.

This overview should help in understanding the baseline capabilities of your Boxer robot as you move towards integrating the NVIDIA Jetson Orin Nano. The most critical next step for hardware integration is to determine the exact pinout and specifications of the 37-pin connector.
