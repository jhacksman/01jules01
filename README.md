# OTTO 100 SDV Boxer - Backpack PC Replacement & Charger Info

This repository contains documentation and research to assist with replacing a missing backpack PC on an OTTO 100 SDV (Boxer version) with an NVIDIA Jetson Orin Nano, and to identify a suitable trickle charger.

## Project Goal:

The primary goal is to understand the interface requirements of the OTTO 100 SDV Boxer to allow for the integration of a custom compute solution (NVIDIA Jetson Orin Nano) and to find a compatible charger that can maintain the robot's battery health.

## Documentation:

This repository is organized into the following documents:

*   **[Boxer Overview](./BOXER_OVERVIEW.md):** Provides an overview of the Clearpath Robotics Boxer, its relation to the OTTO 100, clarification on the "yellow stripe" marking, and details of the known backpack PC interface points.
*   **[Jetson Orin Nano Integration](./JETSON_INTEGRATION.md):** Outlines the proposed approach for integrating the NVIDIA Jetson Orin Nano, including data and power connection strategies. It highlights the critical need to identify the pinout of the 37-pin attachment connector.
*   **[Charger Information](./CHARGER_INFORMATION.md):** Details the recommended charger, likely the Grin Technologies Cycle Satiator, and explains how its programmability can be used for battery health maintenance (fulfilling the "trickle charger" requirement).

## Current Status & Critical Missing Information:

*   The general architecture of the Boxer and its backpack PC interface (Ethernet, 37-pin connector) is understood.
*   A suitable smart charger (Grin Cycle Satiator) has been identified, which can be programmed for partial charging to ensure battery longevity.
*   **The most critical piece of missing information is the detailed pinout and electrical specifications (voltage, current capacity) of the 37-pin attachment connector on the Boxer.** This information is essential for safely powering the Jetson Orin Nano. Recommendations for how to find this information are included in the [Jetson Orin Nano Integration](./JETSON_INTEGRATION.md) document.

It is strongly advised to obtain the 37-pin connector details before attempting to connect any custom power wiring to the Jetson Orin Nano.
