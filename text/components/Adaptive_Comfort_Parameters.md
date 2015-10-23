## Adaptive Comfort Parameters [![](../../images/icons/Adaptive_Comfort_Parameters.png)]

![](../../images/components/Adaptive_Comfort_Parameters.png)

Use this component to set Adaptive comfort parameters for the Adaptive Comfort Calculator or the Adaptive Comfort Chart.  

#### Inputs
* ##### ASHRAEorEN_ [Optional]
Set to 'True' to have the Adpative components use the US (ASHRAE 55 2013) adaptive standard and set to 'False' to have the Adaptive components use the European (EN-15251) standard.  The default is set to use the US (ASHRAE 55 2013) standard.  Note that changing the standard will also change some of the inputs below.  The ASHRAE standard will use the average monthly temperature by default and the European standard will use a running mean temperature by default.  Also, the European standard uses building classes instead of 80 / 90 percent acceptability.
* ##### eightyOrNinetyComf_ [Optional]
Set to 'True' to have the comfort standard be 80 percent of occupants comfortable and set to 'False' to have the comfort standard be 90 percent of all occupants comfortable.  The default is set to 'False' for 90 percent, which is what most members of the building industry seem to aim for in today's world.  However some projects will occasionally use 80% as this was originally the benchmark that engineers set around the dawn of air conditioning.
* ##### avgMonthOrRunMean_ [Optional]
Set to 'True' to have the Adpative components compute the prevailing outdoor temperature from the average monthly temperature (the official method used by the US's ASHRAE 55 2013) and set to 'False' compute the prevailing outdoor temperature from a weighted running mean of the last week (the official method used by Europe's EN-15251).  The default is set to align with the chosen comfort standard above (either ASHRAE 55 2013 or EN-15251) but this option is included to allow users to explore differences and variations between the two standards.
* ##### levelOfConditioning_ [Optional]
An optional number between 0 and 1 that represents how 'air conditioned' a space is. By default, this value is always set to 0 because both the ASHRAE 55 2013 and EN-15251 standards are strictly meant to be used for buildings without any installed air conditioning whatsoever.

#### Outputs
* ##### comfortPar
Comfort parameters that you can plug into either the "Ladybug_Adaptive Comfort Calculator" or the "Ladybug_Adaptive Comfort Chart."


[Check Hydra Example Files for Adaptive Comfort Parameters](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Adaptive Comfort Parameters)