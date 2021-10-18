1. **Pools**
  
    A pool is a reservoir within which something can be stored and released. 
   
    For example, a carbon pool is a reservoir from which carbon can be stored (sequestered and/or maintained) or emitted, such as debris. Within FLINT, each pool has attributed a value such as tonnes carbon, and at each time step, the FLINT can move stores from one pool to another using operation.

    Here are the different pools present in the FLINT. 

    ![Pools](assets/pools.png)

2. **Operations**
  
    An operation is a process within the FLINT that moves carbon stock between pools.         
    Operations can reflect ongoing natural processes, such as growth, or specific events, natural or human-induced.

    Operations allow the FLINT to track changes in carbon stock through time, including fluxes into and out of pools.

    For example, a harvest moves plant material to products and debris pools, wildfire moves plant material to debris and atmosphere pools.


3. **Events**
    
    Events are operations that occur intermittently (rather than for every time step in a simulation) resulting in the movement of carbon from one pool to another. 
    
    Events include natural and anthropogenic events including fire, harvesting, ploughing, and fertiliser application. These are coded for the FLINT as a module.

    Here is the relationship between Pools and Operations/ Events.

    ![Operations](assets/operations.png)

4. **Modules**

    Modules are the building block of FLINT. These contain the operations, describing the ecological processes and driving the carbon changes in the landscape.

    This document provides the infromation regarding major modules present in FLINT.


5. [**Tiers of Module**](https://community.foundationfootprint.com/FoundationFootprintHelpCentre/Miscellaneous/IPCCTiers.aspx#:~:text=Tiers%20of%20Emission%20Factors%20and%20Activity%20Data&text=A%20tier%20represents%20a%20level%20of%20methodological%20complexity.&text=Tier%201%20is%20the%20basic,of%20complexity%20and%20data%20requirements.)

    All the modules are divided into three different Tiers, according to the quantity of information required, and the degree of analytical complexity.

    Three tier's are described for categorizing both emissions factors and activity data.
    
    Tier 1 is the basic method, frequently utilizing IPCC-recommended country-level defaults, while Tier's 2 and 3 are each more demanding in terms of complexity and data requirements.

6. [**Temporal Distribution**](https://github.com/moja-global/FLINT/wiki/1.7-Temporal-Distribution)

    The temporal scale in FLINT is referred to as time-steps. Time-steps are lengths of time over which operations are reported. It is only at the end of a time-step that carbon can be moved from one pool to another.

    The standard time-step in the FLINT is one month. However it can be varied by the user. One month is the recommended time-step for modelling carbon.

7. **Simulation Units**

    A Simulation Unit is a unit for which a module is applied. A Simulation Unit can represent a spatial area, such as a pixel or forest stand, or it can represent an emissions source, such as livestock.    
    Where the Simulation Unit refers to a geographically referenced area, it is known as a Land Unit.

    The overall framework of FLINT manages the processing of Simulation Units over time. While Simulation Units are the basis of all simulations run in FLINT.

8. **Synchronized Events**

    In some circumstances, modules that are simulated for a particular Simulation Unit are dependent on other Simulation Units. That is, there is an interdependency across the Simulation Units.   
    In these situations, it is necessary for there to be a process that synchronises across the related Simulation Units and is known as synchronized events. 
    
    Synchronized Server in FLINT manages the Synchronized events.

9. **Mass Balance**

    The carbon cycle is based on the transfer of carbon molecules from one pool to another, where the molecules are not created, nor are they destroyed.  
    As such, all outputs must be equal to the inputs, that is, that the system is in balance. This is referred to as mass balance.

Overall this is the high level design of the FLINT.  

![design](assets/design.png)