# Charger Information for OTTO 100 / Boxer

This document provides information regarding a suitable charger for the OTTO 100 / Clearpath Robotics Boxer AMR, focusing on the "trickle charging" requirement.

## Identified Charger: Grin Technologies Cycle Satiator

*   The Clearpath Boxer User Manual states it ships with an "OTTO 100 Manual Charger." Research strongly suggests this is a **Grin Technologies Cycle Satiator** charger.
*   Website: [https://ebikes.ca/product-info/grin-products/cycle-satiator.html](https://ebikes.ca/product-info/grin-products/cycle-satiator.html)

## Suitability for "Trickle Charging" / Battery Health:

*   The Cycle Satiator is a highly programmable "smart charger," not a traditional trickle charger that provides continuous low current.
*   **Programmable Charge Profiles:** Its key feature is the ability to create custom charge profiles. This allows you to:
    *   Charge the battery to its full voltage for maximum range when needed.
    *   Program a profile to charge to a lower percentage (e.g., 80% or 90%) of its maximum capacity. Charging lithium-ion batteries to a partial voltage significantly improves their cycle life and long-term health, especially when the robot is not in continuous use. This effectively fulfills the need for a "trickle" or "maintenance" charging strategy.
*   **Power:** It's a relatively high-power charger (360W), capable of charging the battery quickly when a full charge is desired.

## Recommended Model:

*   The OTTO 100 / Boxer likely uses a 48V nominal battery system (this is common for robots of this size).
*   The **Cycle Satiator 4808 model** (output: 12-63V, up to 8A) is the most probable match for a 48V system.
*   **Action Required:** It is advisable to confirm your robot's specific battery voltage before purchasing. This might be indicated on the battery itself (if accessible) or in any remaining fleet management documentation you might have received.

## Purchasing and Connectors:

*   The Cycle Satiator can be ordered directly from Grin Technologies (ebikes.ca) or various distributors listed on their site.
*   **Standard Connector:** The Satiator typically ships with a 3-pin male XLR connector for its DC output.
*   **Robot Charge Port:** You will need to inspect the charging port on your Boxer robot to determine if it directly accepts a 3-pin female XLR connector.
*   **Adapters:** Grin Technologies offers a variety of adapter cables if the Boxer's port is different (e.g., DC barrel jack, Anderson, etc.). Identify your robot's port and order a suitable adapter if necessary.

## Important Considerations:

*   **Safety:** Only use chargers specifically designed for your robot's battery chemistry and voltage. The Boxer manual warns against using other chargers. The Satiator's programmability makes it adaptable, but it must be configured correctly for your specific battery.
*   **Initial Setup:** You will need to program the Satiator with appropriate charge profiles for your Boxer's battery (e.g., a full charge profile and a storage/maintenance charge profile). Consult the Satiator manual and potentially Grin Tech's resources for guidance on setting this up for your battery type (likely Lithium-Ion).

Using the Cycle Satiator with a correctly programmed partial charge profile will provide a robust and battery-health-conscious charging solution for your Boxer.
