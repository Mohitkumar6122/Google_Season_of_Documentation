# GCBM Module

The GCBM (Generic Carbon Budget Model) is a combination of the FLINT platform with the science modules developed by the Canadian Forest Service (CFS).

These are the same science modules used in the first generation tool ([CBM-CFS3](https://www.nrcan.gc.ca/climate-change/impacts-adaptations/climate-change-impacts-forests/carbon-accounting/carbon-budget-model/cbm-cfs3/13089)). Since the science and processes behind both tools are very similar, it is relatively easy to transition from CBM-CFS3 to GCBM.

The CBM-CFS3 is widely used throughout Canada and globally and its use is supported by the Canadian Forest Service of Natural Resources Canada.

The next generation GCBM is currently used by the CFS with a number of partner organizations to advance the science of forest carbon estimation and to support policy analyses such as the assessment of mitigation options in the forest sector.

In GCBM, forest inventory and disturbance events are spatially explicit. The location of disturbances are explicit in spatial layers instead of rule based. The GCBM Module is able to simulate large landscapes easily.

![image](assets/gcbm.png)

It is one of the Country specific modules designed for Canada.

It works at the **Annual Time step**.

There is a special repository for the GCBM Module [Here](https://github.com/moja-global/moja.canada/tree/develop).

***PREREQUISITE MODULES FOR GCBM:*** 

There are numerous prerequisites for the GCBM and we have only included a short summary of these modules.


1. **The Canadian Model for Peatlands (CaMP)** 
    
    The Canadian Model for Peatlands (CaMP) is a module for Greenhouse Gas Emissions.

    The CaMP was designed as a module for the spatially-explicit Generic Carbon Budget Model (GCBM) that is intended for future reporting of Greenhouse gas (GHG) emissions and removal estimates from Canada's managed forest area. 

    The Canadian Model for Peatlands (CaMP) is a site- to national-level peatland carbon model developed to better estimate greenhouse gas (GHG) emissions across a range of peatland types within Canada.

    Different events are fired on the basis of different land type found during simulation.
    like If peatland land type is encountered then fires peatland disturbance event else it fires a regular CBM disturbance event.

    For More information regarding CaMP check out this [Document](https://www.sciencedirect.com/science/article/pii/S0304380020302350).

2. **[Turnover Module](https://github.com/moja-global/Google.Season.of.Documentation/blob/master/modules-development/turnover-module.md)**
