# Arrays

Certain properties can be declared as an array, allowing the input to be
multi-select. Doing so returns all selected values within an array.

Property Type| Supported As Array  
---|---  
boolean| No  
string| Yes  
number| Yes  
Color| No  
Complex Object| Yes  
Select| Yes  
Typed List| No  
  
* * *

Simple types can be put into multi-value arrays by simply making them arrays.

![006aec21-7736-449d-8b30-68032dec0629]

String literal types can also be used as multi-value to provide the end user
with a set of options of which multiple can be selected.

![0828b528-74d4-4e46-ab1c-79c0d6965f06]

* * *

Configurations can also be arrays of complex objects. You can use these arrays
to permit the user to create a list of configured objects. When used in
combination with the `@tabular` decorator, it is possible to create table
structured inputs.

![4d90e19d-abf3-48a1-b878-4674625de765]

