## Separate data [![](../../images/icons/Separate_data.png)]

![](../../images/components/Separate_data.png)

Use this component to separate the text strings from the numbers in the climate data streams output from the Import EPW component.

#### Inputs
* ##### _inputList [Required]
A list of data that contains both text srtings and numbers.  For example, a data stream output from the Import EPW component.

#### Outputs
* ##### numbers
The numbers from in the _inputList data.  Note that the order of numbers in this list is the same as the _inputList.
* ##### strings
The text strings from in the _inputList data.  Note that the order of text strings in this list is the same as the _inputList.


[Check Hydra Example Files for Separate data](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Separate data)