# <p>  <b>StarPose - Cellpose Applied to Elongated Data </b> </p>
## <p>  <b>CSCI 3317 Final Project - Steven Roche, Daniel Kim, Julian Castro </b> </p>

This repo was cloned from Cellpose. For Cellpose documentation and installation instructions, follow the fork link. 
The main part of this repository is the Cellpose code and library. Our work is under the `CSCSI3317_final_project` folder.
The data used for finetuning is located at [cv_data](https://github.com/juliancstrocodes/cv_data). There are also scripts there that were used for data augmentation. 

Our fine-tuned models are located in `iteratedcellpose/CSCSI3317_final_project/models/model_links.md`. Relevant notebooks (described below) are found in `iteratedcellpose/CSCI3317_final_project/notebooks/`.

The contribution is as follows:
1. Data sourcing (finding the source data in the `cv_data` repo) was performed by Julian Castro.
2. Manual segmentation of the data from (1) was completed by all team members. After some cleaning, this was put in the `cv_data/segmented_for_finetuning` folder.
3. The data augmentation was performed by Steven Roche. The augmentation script is located at `cv_data/data_augmentation_biomed.py`.
4. The first finetuned model, found in `iteratedcellpose/CSCSI3317_final_project/models/model_links.md` and called `cellpose_...` was completed by Steven Roche.
5. The model finetuned on the augmented data, found in `iteratedcellpose/CSCSI3317_final_project/models/model_links.md` and called `model_elegans` was completed by Daniel Kim.
6. The files `cv_data/convert_files.py` and `cv_data/train_cellpose.ipynb` were created by Daniel Kim. Those files, respectively, 1): transformed the binary mask segmentations from `cv_data/data_augmentation_biomed.py` into instance segmentations (which resulted in the `cv_data/cleaned_augmentation_data` and 2) implemented code to finetune the Cellpose model.
7. The notebook `iteratedcellpose/CSCI3317_final_project/notebooks/stardist_prediction.ipynb` was created by Steven Roche. This notebook shows how we corrected the fine-tuned models' tendencies to segment a worm into two instances.
