# UnityScriptTemplates
Script Templates to accelerate game dev within the Unity Engine

We can create custom script templates that are generated from .txt files. First create a new folder in your Assets folder called ScriptTemplates.
The naming convention of the script templates following a very specific order; `order-context menu group name__context menu name-file name.cs`

* `order` like an array, the position of the button in the context menu.
* `context menu group name` the label of the button that contains the button that is used to create the script.
* `context menu name` the label of the button that is used to create a new script.
* `file name` the standard name given to the script when it is created in the project.

Lets take an example for a ScriptableObject: Lets create a .txt file on your desktop named: 0-Scripts__ScriptableObject-NewScriptableObject.cs

```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

    #ROOTNAMESPACEBEGIN#
[CreateAssetMenu("#SCRIPTNAME#")]
public class #SCRIPTNAME# : ScriptableObject
{

}
#ROOTNAMESPACEEND#
```

What we write in this file is automatically added everytime in the script we create from this template. Lets discuss a few new things;

* `#ROOTNAMESPACEBEGIN#` : This is the starting line of your global namespace of your project or the namespace of your assembly.
* `#ROOTNAMESPACEEND#` : This closes the namespace with a curly bracket.
* `#SCRIPTNAME#` : As the name suggests, this names your script correctly to the name of the file in your project.

This allows for endless customization with templates, especially significantly more convenient for ScriptableObjects and editor scripts that requires standard implementation you wouldn't need to rewrite anymore.
When you are done writing the templates and imported them to the correct folder, `Assets/ScriptTemplates`, you have to restart the editor in order to initialize them.

Good luck!
