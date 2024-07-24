# <p>  <b>StarPose - Cellpose Applied to Elongated Data </b> </p>
## <p>  <b>CSCI 3317 Final Project - Steven Roche, Daniel Kim, Julian Castro </b> </p>

This repo was cloned from Cellpose. For Cellpose documentation and installation instructions, follow the fork link. 
The main part of this repository is the Cellpose code and library. Our work is under the `CSCSI3317_final_project` folder.
The data, augmentation, and image processing scripts used for finetuning is located at [cv_data](https://github.com/juliancstrocodes/cv_data).

Our fine-tuned models are located in `iteratedcellpose/CSCSI3317_final_project/models/model_links.md`. Relevant notebooks (described below) are found in `iteratedcellpose/CSCI3317_final_project/notebooks/`.


[The final paper for this project can be found here.](https://github.com/user-attachments/files/16365709/StarPoseFinalReport.pdf)
<p align="center">
  <img width="200" alt="Screenshot 2024-07-24 at 1 43 14 PM" src="https://github.com/user-attachments/assets/493acfbc-4c78-44fa-84fa-164df262d36c">
  <img width="200" alt="Screenshot 2024-07-24 at 1 43 49 PM" src="https://github.com/user-attachments/assets/a42c5234-e945-47e0-bb33-75b928d5a02b">
  <img width="202" alt="Screenshot 2024-07-24 at 1 46 59 PM" src="https://github.com/user-attachments/assets/cde7096d-2e50-46d1-8a4c-f49bf2643609">
</p>

[The slide deck for this project can be found here.](https://github.com/user-attachments/files/16365824/StarPoseSlideDeck.pdf)
<p align="center">
<img width="300" alt="Screenshot 2024-07-24 at 1 52 24 PM" src="https://github.com/user-attachments/assets/fb5e6895-b8c7-4937-86e6-9dd664c11546">
</p>




The contribution is as follows:
1. Data sourcing (finding the source data in the `cv_data` repo) was performed by Julian Castro.
2. Manual segmentation of the data from (1) was completed by all team members. After some cleaning, this was put in the `cv_data/segmented_for_finetuning` folder.
3. The data augmentation was performed by Steven Roche. The augmentation script is located at `cv_data/data_augmentation_biomed.py`.
4. The first finetuned model, found in `iteratedcellpose/CSCSI3317_final_project/models/model_links.md` and called `cellpose_...` was completed by Steven Roche.
5. The model finetuned on the augmented data, found in `iteratedcellpose/CSCSI3317_final_project/models/model_links.md` and called `model_elegans` was completed by Daniel Kim.
6. The files `cv_data/convert_files.py` and `cv_data/train_cellpose.ipynb` were created by Daniel Kim. Those files, respectively, 1): transformed the binary mask segmentations from `cv_data/data_augmentation_biomed.py` into instance segmentations (which resulted in the `cv_data/cleaned_augmentation_data` and 2) implemented code to finetune the Cellpose model.
7. The notebook `iteratedcellpose/CSCI3317_final_project/notebooks/stardist_prediction.ipynb` was created by Steven Roche. This notebook shows how we corrected the fine-tuned models' tendencies to segment a worm into two instances.
