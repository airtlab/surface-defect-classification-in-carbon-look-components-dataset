# A Dataset for the Classification of Surface Defect in “Carbon Look” Components

This repository contains the data used for the experiments presented in the paper

>Silenzi, A.; Castorani, V.; Tomassini, S.; Falcionelli, N.; Contardo, P.; Bonci, A.; Dragoni, A.F.; Sernani, P. Quality Control of Carbon Look Components via Surface Defect Classification with Deep Neural Networks. *Sensors*. 2023; 23(17):7607. <https://doi.org/10.3390/s23177607> 

The paper is published in the special issue [Artificial Intelligence in Imaging Sensing and Processing](https://www.mdpi.com/journal/sensors/special_issues/JS98B8S2W8) of the [Sensors MDPI journal](https://www.mdpi.com/journal/sensors). The paper is open access and available here: https://www.mdpi.com/1424-8220/23/17/7607

The repository is composed of plain images of carbon look components sued to compare end-to-end models based on Convolutional Neural Networks for the classification of surface defects. The images included in this data repository are taken from real production of [Hp Composites Spa](https://www.hpcomposites.it/), a company located in Ascoli Piceno, Italy, and specialized in the production of composite materials components.

## Data Description

The images were manually labeled according to the recommendations of the domain experts, i.e. the Hp Composite staff, in particular to distinguish between recoverable and non-recoverable defects. The images are taken from different angles and distances, without standard lighting. In this way,
we emulate the conditions that an operator, in charge of controlling the appearance of the components, would face using an handheld device for the quality control, without dedicated settings as in NDT. Thus, we investigate the capability of the proposed models of working under varying conditions, in order to assess the viability of our approach based on plain images.

The available images are split into two separate dataset, included in the “[carbon-binary](carbon-binary/)” and “[carbon-multiclass](carbon-multiclass/)” directories. 

	 surface-defect-classification-in-carbon-look-components-dataset
	  ├─ carbon-binary
	  │   ├─ negative (200 .jpg images)
	  │   └─ positive (200 .jpg images)
	  └─ carbon-multiclass 
	      ├─ negative (500 .jpg images)
	      ├─ non_recoverable_defects (500 .jpg images)
	      └─ recoverable_defects (500 .jpg images)

The carbon-binary directory includes a dataset usable for binary classification. It has two subdirectories “negative” and “positive”, labeling the included images:
-  “[negative](carbon-binary/negative/)” includes 200 images with no defects or limited recoverable porosities;
-  “[positive](carbon-binary/positive/)” includes 200 images with weft discontinuites.

The carbon-binary directory includes a dataset usable for multiclass classification. It has three subdirectories “negative” and “non_recoverable_defects”, and, “recoverable_defects”, labeling the included images:
-  “[negative](carbon-multiclass/negative/)” includes 500 images with no defects;
-  “[non_recoverable_defects](carbon-multiclass/non_recoverable_defects/)” includes 500 images with weft discontinuites or severe porosities. Components presenting such defects need to be discarded;
-  “[recoverable_defects](carbon-multiclass/recoverable_defects/)” includes 500 images with defects that can be treated and corrected, such as limited porosities and the infiltration of external materials (such as aluminum).

The images are 224 x 224 pixels (96 ppi) in JPEG format. The images were originally taken at 3968 x 2976 pixels, then cropped at the center and resized at 224 x 224.The images were manually labeled according to the recommendations of the domain experts, i.e. the Hp Composite staff, in particular to distinguish between recoverable and non-recoverable defects. The images are taken from different angles and distances, without standard lighting.

## Dataset Release Agreement

The dataset is freely released for research and educational purposes.

Please cite as
- Silenzi, A.; Castorani, V.; Tomassini, S.; Falcionelli, N.; Contardo, P.; Bonci, A.; Dragoni, A.F.; Sernani, P. Quality Control of Carbon Look Components via Surface Defect Classification with Deep Neural Networks. *Sensors*. 2023; 23(17):7607. <https://doi.org/10.3390/s23177607>
 
Bibtex entry:

	 @article{Silenzi2023,
	   author = {Silenzi, Andrea and Castorani, Vincenzo and Tomassini, Selene and Falcionelli, Nicola and Contardo, Paolo and Bonci, Andrea and Dragoni, Aldo Franco and Sernani, Paolo},
	   title = {Quality Control of Carbon Look Components via Surface Defect Classification with Deep Neural Networks},
	   journal = {Sensors},
	   volume = {23},
	   year = {2023},
	   number = {17},
	   article-number = {7607},
	   doi = {10.3390/s23177607}
	 }

The paper is open access and available here: <https://www.mdpi.com/1424-8220/23/17/7607>