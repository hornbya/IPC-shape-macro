# IPC-shape-macro
ImageJ macro to measure the size and shape parameters of particles and multiple components within particles

PURPOSE: This macro will measure the sizes and shapes of constituent components, or phases (e.g. crystals, glass) within each particle in an image containing multi-component particles. Components are linked to the host particle, which is described using the same parameters.

REQUIREMENTS: The Shape Filter ImageJ plugin (see above), an 'original' image containing multicomponent particles and a folder containing component image files, where each image is thresholded to show a single component present in the 'original' image.

INPUTS: this macro requires an "original" image showing particle shapes, and a set of images with the same dimensions as the original binary image that have been thresholded to only show a single component (or phase).
Single phase image files should have descriptive titles (e.g. "Plagioclase") and should be saved in a dedicated folder prior to running the macro.
If the original image and phase stack images are not binary when uploaded, the macro will convert them. This will not affect any images that are already binary. 

OUTPUTS: CSV text file containing following parameters for particles and one or multiple components:
Label(slice), Area, Perimeter, Convex hull (CH) area, Convex hull (CH) perimeter, Solidity, Convexity, Concavity Index, Form Factor, Circularity, Roundness, Axial ratio (Feret), Feret diameter, Minimum Feret diameter, Maximum inscribed circle diameter, orientation and ROI Index.

ACKNOWLEDGEMENTS: The macro calls on the Shape Filter ImageJ plugin (https://doi.org/10.5281/zenodo.57880) based on IJBlob, which is described in Wagner, T and Lipinski, H 2013. IJBlob: An ImageJ Library for Connected Component Analysis and Shape Analysis. Journal of Open Research Software 1(1):e6, 
The plugin description is available from https://imagej.net/Shape_Filter and is freely and openly available by subscribing to the Biomedgroup update site in ImageJ (see https://imagej.net/Update_Sites)

This macro also incorporates shape parameters described in Liu, E.J., et al (2015). Optimising Shape Analysis to quantify volcanic ash morphology. GeoResJ, https://doi.org/10.1016/j.grj.2015.09.001 and code from shape macro, with kind permission from Emma Liu.
The macro is freely and openly available in the Supplementary Materials and here: https://data.bris.ac.uk/datasets/wgxxhae8ptdc1he0g2cqq0q1i/Appendix_ShapeAnalysisMACRO.txt
