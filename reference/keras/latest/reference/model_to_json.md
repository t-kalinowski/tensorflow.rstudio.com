# model_to_json


Model configuration as JSON




## Description

Save and re-load models configurations as JSON. Note that the representation
does not include the weights, only the architecture.





## Usage
```r
model_to_json(object)

model_from_json(json, custom_objects = NULL)
```




## Arguments


Argument      |Description
------------- |----------------
object | Model object to save
json | JSON with model configuration
custom_objects | Optional named list mapping names to custom classes or functions to be considered during deserialization.







## See Also

Other model persistence: 
`get_weights()`,
`model_to_yaml()`,
`save_model_hdf5()`,
`save_model_tf()`,
`save_model_weights_hdf5()`,
`serialize_model()`


