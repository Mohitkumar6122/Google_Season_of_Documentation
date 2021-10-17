# RothC Module

RothC is a module used for simulating the turnover of soil carbon in non-waterlogged soils under different vegetation types. It is based on the decomposition of organic matter as it relates to mean temperature and moisture, and proportion of resistant and decomposable organic material. It runs on the monthly time step interval.

It is better than the other modules because its input data is readily available and there is considerable overlap with hybrid growth modules and WOFOST modules. For a detailed explanation and better understanding you can refer to this [PDF.](https://www.verdeterreprod.fr/wp-content/uploads/2020/05/RothC_guide_WIN.pdf)

## INPUTS :

-   Time Step (Monthly).
-   Pool 1: Input of plant residue.
-   Pool 2: Input of farmyard manure.
-   Pool 3: Total organic carbon.
-   Pool 4: Microbial biomass carbon.
-   Rainfall.
-   Open pan evaporation.
-   Mean air temperature.
-   Clay content of soil.
-   Decomposability of incoming plant material.
-   Soil Cover.
-   Depth of soil layer sampled.

## OUTPUT :

-   Total Organic Carbon.
-   Microbial Biomass Carbon.


Here is the pictorial representation of RothC module.

![rothc](assets/RothC.png)