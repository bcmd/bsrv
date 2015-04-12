# BrainSignals Revisited
This repository contains model definitions, scripts and input data used for simplification and testing in the PLoS ONE paper [BrainSignals Revisited: simplifying a computational model of cerebral physiology][bsrv].

## Models
The `models` directory contains defintions for all model variants in [BCMD][bcmd] format. At the top level of the directory directory are self-contained `.modeldef` files for each variant. Because there is a great deal of overlap between the models, actual model development was performed using definitions decomposed into multiple files, with the shared details referenced from various master files. For completeness, all these files included in the `decomposed` subdirectory. These files are not required to build the models and their structure is somewhat opaque, so for most purposes it is probably simpler to just use the self-contained versions.

## Data
Both experimental data and synthetic model inputs are provided in the `data` directory. The `hypercapnia` subdirectory contains NIRS and systemic data from adult volunteers undergoing a hypercapnia challenge, in CSV format. BCMD input files corresponding to these data are in the `inputs` subdirectory, which also includes the input files for steady state simulations for blood pressure, oxygen saturation and partial pressure of CO<sub>2</sub>. The [R][r] script `synth.R` contains the functions used to generate a large number of synthetic input data sets. The actual files so generated are included in the `synthetic` subdirectory.

[bcmd]: https://github.com/bcmd/BCMD
[bsrv]: http://www.plosone.org "(NB: final URL will be added after publication)"
[r]: http://www.r-project.org
