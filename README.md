# README
This is an extension for Visual Studio Code. 

Presently it has only two features.

* Go to previous edit location by using Ctrl+j followed by Ctrl-l
* Show additional configurable symbols when you press Ctrl+Shift+o

## Configurable symbols

* Rules may be created in a file '.symbol-rules' in the root folder of the project.
* File specific rule may be added to the file itself.

### Rules format

* One rule per line.
* Rules begin with '#rule:' (without the quotes). Any line that does not contain this is ignored.
* The text following '#rule:' is composed of fields separated by double vertical bars ||


#### Rule Fields

* Regular Expression. May have parenthesized submatches. The submatches can be used to construct a label. Required.
* Label. Optional. Must contain at least one pair of the % character followed by a numeric digit. This is replaced by the corresponding submatch from the regular expression match. If not specified, submatch 1 or the entire match is used.
* Kind. Optional. One of : Array, Boolean, Class, Constant, Constructor, Enum, Field, File, Function, Interface, Method, Module, Namespace, Number, Package, Property, String, Variable. Defaults to Namespace.
* File Extensions. Limits the rules to files that match the given list of extensions. Must be of the form ext=.ext1,.ext2 
  
