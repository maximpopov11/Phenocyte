# Phenocyte
An automatic Arabidopsis plant phenotyping tool using machine learning.

Plants are vital to human civilization for their agricultural yields as well as other uses such as those in energy. As such, phenotyping plants to maximize yields is a busy field of research. Manual phenotyping is an incredibly slow, tedious, and error-prone process. Arabidopsis is a model plant in the field due to the ease of genetically modifying it and it's quick rate of growth. This work develops Phenocyte to automatically segment Aribidopsis plant images into its four plant segments to trivialize phenotyping thereof.

This work achieves a state of the art 99.25% IoU for the segmentation of the entire plant versus the background. The individual plant part IoUs are less exemplary, and require further training to improve, but real-value phenotyping achieves much stronger success rates than the full mask segmentation at current training state. Measured averaged values include:
* 99.25% overall plant vs background segmentation IoU
* 92.96% accurate root lengths
* 80.55% leaf segmentation IoU
* 53.25% stem segmentation IoU
* 67.39% seed segmentation IoU
* 73.37% root segmentation IoU

Further model training is expected to improve results. For maximal performance, more accurate training data is required.

UNet Model.ipynb contains the model with the results described above.

Raw SAM contains an initial strategy seeking to search the SAM hyperparameter space without model training which achieved poor results.

SAM Prompt contains an initial strategy seeking to automatically find prompt points for SAM without model training which achieved suboptimal results.
