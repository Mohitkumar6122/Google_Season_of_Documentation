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

2. **Decay Module**

    This Module performs the annual decay and turnover on a set of dead organic matter pools present in the GCBM.
    Data Requirements for the Decay Module are as :
    
    - A table named "decay_parameters" with one set of decay parameters for each of the enumerated dom pools in the DomPool.

    - Scalar "mean_annual_temperature" is the mean annual temperature of the environment.

    - Scalar "SlowMixingRate" the amount turned over from slow aboveground to slow belowground annually.

3. **Moss Decay Module**

    This module is used for moss related computing, that is whether the moss pool is decaying or not.
    
    It uses various mathematical equations to apply decay rates to the different moss pools.

4.  **Moss Disturbance Module**

    This module responds to the fire disturbance events in CBM.
    
    This module is responsible for transferring carbon content from Moss pools to the Greenhouse gases pools.
    
    It gets the input data from the variable ```moss_fire_parameters```.

5. **Moss Growth Module**

    This module is responsible for the growth of moss pools that is it increments the moss growth with the help of mathematical equations, various parameters and moss pools.

6. **Moss Turnover Module**

    This module is responsible for the turnover of moss pools that is from the moss live pool to the moss past pool.
    
    It accurately calculates the amount of turnover moss by taking moss live amount and transfer rates into consideration and by applying transfer events. 

7. **Peatland after CBM Module**

    This module is triggered after CBM simulation on a land unit, and prepares the land unit to simulate the peatland simulation.

    It transfers carbon from some CBM pools to  the peatland pools. 
    
    It is called after finishing the regular CBM simulation.

8. **Peatland Decay Module**

    This module is responsible for Peatland decay.
    
    It gets the data by variable ```peatland_decay_parameters```, ```peatland_turnover_parameters``` and also accounts in various parameters like mean annual temperature, annual water table depth, total initial carbon and transfers the pool's content accordingly.

    It also uses a special turnover rate for various pools like carotelm pool.

    It sets the turnover rate for diffrent pools by taking into acoount of values of varoius greenhouse gases.

9. **Peatland Disturbance Module**

    This module responds to the historical and last disturbance events in the CBM spinup.
    
    It alters the water table depth according to the disturbance type and Peatland Id. 

10. **Peatland Growth Module**

    This module gets the data from the ```peatland_growth_parameters```, ```peatland_turnover_parameters``` and ```peatland_growth_curve```.
    
    It simulates the various growth cycles, growth curves and also sets the component value for the pools like woody layer, moss layer and many more. 

14. **[Turnover Module](https://github.com/moja-global/Google.Season.of.Documentation/blob/master/modules-development/turnover-module.md)**

