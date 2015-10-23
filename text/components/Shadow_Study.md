## Shadow Study [![](../../images/icons/Shadow_Study.png)]

![](../../images/components/Shadow_Study.png)

Use this component to generate outline curves representing shadows cast by input _geometry for a given _sunVector.

#### Inputs
* ##### _geometry [Required]
Breps representig test geometries that will cast shadows on each other.
* ##### _sunVector [Required]
A sun vector from the Ladybug sunPath component.

#### Outputs
* ##### readMe!
...
* ##### shadow
Outline curves representing the shadows cast by the individual input Breps on other input Breps.  Note that, if all input _geometry is planar, this output can be hooked up to a Grasshopper "Brep" component to give Breps representing shadows cast.
* ##### shade
Outline curves representing the the parts of individual input Breps that are not in the sun.  In other words, this is the self-shaded part of the Breps. Note that, if all input _geometry is planar, this output can be hooked up to a Grasshopper "Brep" component to give Breps representing self-shaded areas.


[Check Hydra Example Files for Shadow Study](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Shadow Study)