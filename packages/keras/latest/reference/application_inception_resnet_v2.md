# application_inception_resnet_v2


Inception-ResNet v2 model, with weights trained on ImageNet




## Description

Inception-ResNet v2 model, with weights trained on ImageNet





## Usage
```r
application_inception_resnet_v2(
  include_top = TRUE,
  weights = "imagenet",
  input_tensor = NULL,
  input_shape = NULL,
  pooling = NULL,
  classes = 1000,
  classifier_activation = "softmax",
  ...
)

inception_resnet_v2_preprocess_input(x)
```




## Arguments


Argument      |Description
------------- |----------------
include_top | Whether to include the fully-connected layer at the top of the network. Defaults to ``TRUE``.
weights | One of ``NULL`` (random initialization), ``'imagenet'`` (pre-training on ImageNet), or the path to the weights file to be loaded. Defaults to ``'imagenet'``.
input_tensor | Optional Keras tensor (i.e. output of ``layer_input()``) to use as image input for the model.
input_shape | optional shape list, only to be specified if ``include_top`` is FALSE (otherwise the input shape has to be (299, 299, 3). It should have exactly 3 inputs channels, and width and height should be no smaller than 71. E.g. (150, 150, 3) would be one valid value.
pooling | Optional pooling mode for feature extraction when ``include_top`` is ``FALSE``. Defaults to ``NULL``.   *  `NULL` means that the output of the model will be the 4D tensor output of the last convolutional layer.  *  `'avg'` means that global average pooling will be applied to the output of the last convolutional layer, and thus the output of the model will be a 2D tensor.  *  `'max'` means that global max pooling will be applied.
classes | Optional number of classes to classify images into, only to be specified if ``include_top`` is TRUE, and if no ``weights`` argument is specified. Defaults to 1000 (number of ImageNet classes).
classifier_activation | A string or callable. The activation function to use on the "top" layer. Ignored unless ``include_top = TRUE``. Set ``classifier_activation = NULL`` to return the logits of the "top" layer. Defaults to ``'softmax'``. When loading pretrained weights, ``classifier_activation`` can only be ``NULL`` or ``"softmax"``.
... | For backwards and forwards compatibility
x | ``preprocess_input()`` takes an array or floating point tensor, 3D or 4D with 3 color channels, with values in the range [0, 255].




## Details

Do note that the input image format for this model is different than for
the VGG16 and ResNet models (299x299 instead of 224x224).

The ``inception_resnet_v2_preprocess_input()`` function should be used for image
preprocessing.





## Value

A Keras model instance.




