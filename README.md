# dynamic-network-architectures_translation [In Progress]
This repository adapts the dynamic-network-architectures for image-to-image translation tasks. It is based on the original repository found at [MIC-DKFZ/dynamic-network-architectures](https://github.com/MIC-DKFZ/dynamic-network-architectures).

## Changes Made
- **UNet Decoder Improvements**: Added upsampling + convolution in the UNet decoder instead of transposed convolution to help prevent checkerboard artifacts, especially when using perceptual loss. cf [this article](https://distill.pub/2016/deconv-checkerboard/).
  - `Upsample_Trilinear`
  - `Upsample_Nearest`
  - 
## TODO
- Add an argument to control the choice of UNet decoder (e.g., `upsample_trilinear`, `upsample_nearest`).
- Test if _tanh_ is necessary after the last convolution in decoder.
