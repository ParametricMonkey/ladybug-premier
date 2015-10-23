## PMV Comfort Calculator [![](../../images/icons/PMV_Comfort_Calculator.png)]

![](../../images/components/PMV_Comfort_Calculator.png)

Use this component to calculate comfort metrics of Predicted Mean Vote (PMV), the Percent of People Dissatisfied (PPD), and the Standard Effective Temperature (SET) for a set of climate conditions and occupant behavior/clothing.

#### Inputs
* ##### _dryBulbTemperature [Required]
A number representing the dry bulb temperature of the air in degrees Celcius.  This input can also accept a list of temperatures representing conditions at different times or the direct output of dryBulbTemperature from the Import EPW component.
* ##### meanRadiantTemperature_ [Optional]
A number representing the mean radiant temperature of the surrounding surfaces in degrees Celcius.  If no value is plugged in here, this component will assume that the mean radiant temperature is equal to air temperature value above.  This input can also accept a list of temperatures representing conditions at different times or the direct output of dryBulbTemperature from the Import EPW component.
* ##### windSpeed_ [Optional]
A number representing the wind speed of the air in meters per second.  If no value is plugged in here, this component will assume a very low wind speed of 0.05 m/s, characteristic of most indoor conditions.  This input can also accept a list of wind speeds representing conditions at different times or the direct output of windSpeed from of the Import EPW component.
* ##### _relativeHumidity [Required]
A number between 0 and 100 representing the relative humidity of the air in percentage.  This input can also accept a list of relative humidity values representing conditions at different times or the direct output of relativeHumidity from of the Import EPW component.
* ##### ------------------------------ []
...
* ##### metabolicRate_ [Optional]
A number representing the metabolic rate of the human subject in met.  This input can also accept text inputs for different activities.  Acceptable text inputs include Sleeping, Reclining, Sitting, Typing, Standing, Driving, Cooking, House Cleaning, Walking, Walking 2mph, Walking 3mph, Walking 4mph, Running 9mph, Lifting 10lbs, Lifting 100lbs, Shoveling, Dancing, and Basketball.  If no value is input here, the component will assume a metabolic rate of 1 met, which is the metabolic rate of a seated human being.  This input can also accept lists of metabolic rates.
* ##### clothingLevel_ [Optional]
A number representing the clothing level of the human subject in clo.  If no value is input here, the component will assume a clothing level of 1 clo, which is roughly the insulation provided by a 3-piece suit. A person dressed in shorts and a T-shirt has a clothing level of roughly 0.5 clo and a person in a thick winter jacket can have a clothing level as high as 2 to 4 clo.  This input can also accept lists of clothing levels.
* ##### ------------------------------ []
Script variable SETCalculator
* ##### comfortPar_ [Optional]
Optional comfort parameters from the "Ladybug_PMV Comfort Parameters" component.  Use this to adjust maximum and minimum acceptable humidity ratios.  These comfortPar can also change whether comfort is defined by eighty or ninety percent of people comfortable.  By default, comfort is defined as 90% of the occupants comfortable and there are no limits on humidity when there is no thermal stress.
* ##### analysisPeriod_ [Optional]
An optional analysis period from the Analysis Period component.  If no Analysis period is given and epw data from the ImportEPW component has been connected, the analysis will be run for the enitre year.
* ##### calcBalanceTemperature_ [Optional]
Set to "True" to have the component calculate the balance temperature for the input windSpeed_, _relativeHumidity, metabolicRate_, and clothingLevel_.  The balance temperature is essentially the temperature for these conditions at which the PMV is equal to 0 (or the energy flowing into the human body is equal to the energy flowing out).  Note that calculating the balance temperature for a whole year with epw windspeed can take as long as 10 minutes and so, by default, this option is set to "False".
* ##### _runIt [Required]
Set to "True" to run the component and calculate the PMV comfort metrics.

#### Outputs
* ##### readMe!
...
* ##### ------------------------------
...
* ##### --------------------
Because the PMV comfort model is derived from indoor comfort studies and you have hooked up outdoor data, the PMV values out of this component are not meaningful.
* ##### --------------------
Because the PMV comfort model is derived from indoor comfort studies and you have hooked up outdoor data, the PPD values out of this component are not meaninful.
* ##### OUT_SET
The Outdoor Standard Effective Temperature (OUT_SET) in degrees Celcius.  OUT_SET is an ajusted temperature scale meant to reflect the heat stress or cold felt by an individual and has passed peer review as an indicator of outdoor comfort.  HOWEVER, if you are interested in knowing whether outdoor conditions are actually comfortable, it is highly recommended that you use the Ladybug UTCI Comfort Calculator.  OUT-SET has been shown to be a poor indicator of outdoor comfort and is better used as a tool to help understand what clothing and metabolic rate a comfortable person might have in the outdoors AFTER running a UTCI study.
* ##### ------------------------------
------------------------------
* ##### restrictedComfOrNot
Because the PMV comfort model is derived from indoor comfort studies and you have hooked up outdoor data, the comfortableOrNot values out of this component should be taken with a grain of salt.  The comfort here represents a very narrow range because you are restricting the theoretical person's clothing and metabolic rate, which is normally unrestricted in the outdoors.
* ##### restrictedPercentComf
Because the PMV comfort model is derived from indoor comfort studies and you have hooked up outdoor data, the percentOfTimeComfortable values out of this component should be taken with a grain of salt.  The comfort here represents a very narrow range because you are restricting the theoretical person's clothing and metabolic rate, which is normally unrestricted in the outdoors.
* ##### ------------------------------
...
* ##### balanceTemperature
The balance temperature is the temperature for the input windSpeed_, _relativeHumidity, metabolicRate_, and clothingLevel_ at which the PMV is equal to 0 (or the energy flowing into the human body is equal to the energy flowing out).  Setting the dry bulb and radiant temperatures to this value will produce a PMV of 0 and will yield the lowest possible PPD.


[Check Hydra Example Files for PMV Comfort Calculator](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_PMV Comfort Calculator)