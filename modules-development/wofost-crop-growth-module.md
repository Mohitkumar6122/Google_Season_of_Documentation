# Wofost Crop Growth Module

WOFOST (WOrld FOod STudies) is a mechanistic module that simulates crop growth on the basis of photosynthesis, respiration and the prevailing environmental conditions. It is similar to the hybrid forest growth module. It is not included in the FLINT and is specially designed for **KENYA**.

It is similar to the [DayCent](https://en.wikipedia.org/wiki/DayCent). This module runs on a **Daily time step** and allows users to model the potential production, attainable production and actual production for a given site (region). The simulation runs from sowing to maturity and is based on the response of crop to weather (all production levels) and soil moisture conditions.

## INPUTS :

-   Time step (Daily)
-   Crop Type
-   Pool 1: stem
-   Pool 2: Leaves
-   Pool 3: Storage Organs
-   Pool 4: Roots
-   Maximum and Minimum Temperature
-   Global Radiation

## OUTPUTS :

- It calculates how much carbon moves between pools

Here is the pictorial representation of WOFOST Module. 

![WOFOST](assets/WOFOST.png)