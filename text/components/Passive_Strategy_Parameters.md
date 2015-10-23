## Passive Strategy Parameters [![](../../images/icons/Passive_Strategy_Parameters.png)]

![](../../images/components/Passive_Strategy_Parameters.png)

Use this component to adjust the assumptions of the passive strategies that can be overalid on the Ladybug the Psychrometric Chart. The default assumptions of each of the strategies are as follows: 

#### Inputs
* ##### maxTempAboveComf_ [Optional]
An optional number in degrees C representing the maximum daily temperature above the comfort range which can still be counted in the Thermal Mass + Night Flush polygon.  The default is set to 16.7 C above the highest comfort temperature.
* ##### minNightDiffBelowComf_ [Optional]
An optional number in degrees C representing the minimum temperature below the maximum comfort temperature that the outdoor temperature must drop at night in order to count towards the Thermal Mass + Night Flush polygon. The default is set to 2.8 C.
* ##### maxComfortableAirSpeed_ [Optional]
An optional number in m/s that represents the maximum winds speed tolerable before it starts blowing papers and becomes annoying to occupants.  This is used to shape the "Occupant Use of Fans" Polygon and the default is set ot 1.5 m/s.
* ##### lowestBldgBalancePt_ [Optional]
An optional number representing the building balance point, which will be used to shape the "Internal Heat Gain" strategy polygon.  The default is set to 12.8 C and it is assumed that, above this outdoor temperature, the building is free-running and occupants are able to open windows as they wish.  Note that this default balance temperature of 12.8 is fairly low and assumes a large number of inside heat sources or people as well as in insulated envelope.

#### Outputs
* ##### strategyPar
Passive strategy parameters that can be plugged into the "Ladybug_Psychrometric Chart" to adjust the assumptions of the passive strategy polygons.


[Check Hydra Example Files for Passive Strategy Parameters](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Passive Strategy Parameters)