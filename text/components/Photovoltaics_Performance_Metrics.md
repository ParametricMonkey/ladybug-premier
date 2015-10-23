## Photovoltaics Performance Metrics [![](../../images/icons/Photovoltaics_Performance_Metrics.png)]

![](../../images/components/Photovoltaics_Performance_Metrics.png)

Use this component to calculate various Photovoltaics performance metrics

#### Inputs
* ##### _PVsurface [Required]
- Input planar Surface (not polysurface) on which the PV modules will be applied. If you have a polysurface, explode it (using "Deconstruct Brep" component) and then feed its Faces(F) output to _PVsurface. Surface normal should be faced towards the sun.
* ##### PVsurfacePercent_ [Optional]
The percentage of surface which will be used for PV modules (range 0-100).
* ##### moduleActiveAreaPercent_ [Optional]
Percentage of the module's area excluding module framing and gaps between cells. 
* ##### moduleEfficiency_ [Optional]
The ratio of energy output from the PV module to input energy from the sun. It ranges from 0 to 100 (%).
* ##### lifetime_ [Optional]
Life expectancy of a PV module. In years.
* ##### _____________________ [Default]
Script variable PhotovoltaicsPerformanceMetrics
* ##### _ACenergyPerHour [Required]
Import "ACenergyPerYear" output data from "Photovoltaics surface" component.
* ##### _totalRadiationPerHour [Required]
Import "totalRadiationPerHour" output data from "Photovoltaics surface" component.
* ##### _cellTemperaturePerHour [Required]
Import "cellTemperaturePerHour" output data from "Photovoltaics surface" component.
* ##### _____________________ [Default]
Script variable PhotovoltaicsPerformanceMetrics
* ##### energyCostPerKWh_ [Optional]
The cost of one kilowatt hour in any currency unit (dollar, euro, yuan...)
* ##### embodiedEnergyPerM2_ [Optional]
Energy necessary for an entire product life-cycle of PV module per square meter.
* ##### embodiedCO2PerM2_ [Optional]
Carbon emissions produced during PV module's life-cycle per square meter..
* ##### gridEfficiency_ [Optional]
An average primary energy to electricity conversion efficiency.
* ##### _____________________ [Default]
Script variable PhotovoltaicsPerformanceMetrics
* ##### _runIt [Required]
...

#### Outputs
* ##### readMe!
...
* ##### __________________________
Script variable PhotovoltaicsPerformanceMetrics
* ##### Yield
Ratio of annual AC power output and nameplate DC power rating.
* ##### CUFperMonth
Capacity Utilization Factor - ratio of the annual AC power output and maximum possible output under ideal conditions if the sun shone throughout the day for the each month.
* ##### CUFperYear
Capacity Utilization Factor (sometimes called Plant Load Factor (PLF)) - ratio of the annual AC power output and maximum possible output under ideal conditions if the sun shone throughout the day and throughout the year.
* ##### basicPRperMonth
Basic Performance Ratio - ratio of the actual and theoretically possible energy output per month.
* ##### basicPRperYear
Basic Performance Ratio - ratio of the actual and theoretically possible annual energy output.
* ##### temperatureCorrectedPRperMonth
Temperature corrected Performance Ratio - ratio of the actual and theoretically possible energy output per month, corrected for PV module's Cell temperature. Mid-day hours (solarRadiation > 0.6 kWh/m2) only taken into account.
* ##### temperatureCorrectedPRperYear
Temperature corrected Performance Ratio - ratio of the actual and theoretically possible annual energy output, corrected for PV module's Cell temperature. Mid-day hours (solarRadiation > 0.6 kWh/m2) only taken into account.
* ##### __________________________
Script variable PhotovoltaicsPerformanceMetrics
* ##### energyValuePerMonth
Total Energy value for each month in currency unit (dollars, euros, yuans...)
* ##### energyValuePerYear
Total Energy value for whole year in currency unit (dollars, euros, yuans...)
* ##### embodiedEnergy
Total energy necessary for an entire product life-cycle of PV modules.
* ##### embodiedCO2
Total carbon emissions produced during PV module's life-cycle.
* ##### CO2emissionRate
An index which shows how effective a PV system is in terms of global warming.
* ##### EPBT
Energy PayBack Time - time it takes for PV modules to produce all the energy used through-out its product life-cycle.
* ##### EROI
Energy Return On Investment - a comparison of the generated electricity to the amount of primary energy used throughout the PV module's product life-cycle.


[Check Hydra Example Files for Photovoltaics Performance Metrics](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Photovoltaics Performance Metrics)