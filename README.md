# DeepLabV3_Plus

Building the DeepLabV3+ model DeepLabv3+ extends DeepLabv3 by adding an encoder-decoder structure. 
The encoder module processes multiscale contextual information by applying dilated convolution at multiple scales, while the decoder module refines the segmentation results along object boundaries.

<img width="799" alt="deeplabv3_plus_diagram" src="https://user-images.githubusercontent.com/109419535/211144034-0e0b11d6-7182-4f5a-b9a5-d3da1c15a429.png">


Dilated convolution: With dilated convolution, as we go deeper in the network, we can keep the stride constant but with larger field-of-view without increasing the number of parameters or the amount of computation.
Besides, it enables larger output feature maps, which is useful for semantic segmentation.

The reason for using Dilated Spatial Pyramid Pooling is that it was shown that as the sampling rate becomes larger, the number of valid filter weights (i.e., weights that are applied to the valid feature region, instead of padded zeros) becomes smaller.
