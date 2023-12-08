## Intruduction

This report present the whole processes of Creating Ensemble Fusion of Case-based Distilled Student Models for Enhanced Real-time Video Summarization. For Inference the model without re-build the model, please go to the last section "**Inference with Completed Data **".

## Get Logits from Teacher Model
- Download [GenerativeImage2Text](https://github.com/microsoft/GenerativeImage2Text/)
- Replace the **decoder.py** with the provied one
- Execute **get_teacher_logits.ipynb**, located in the same directory as GenerativeImage2Text

## Clustering
- Download or add short cut of [dataset](https://drive.google.com/drive/u/0/folders/17MWu0h-yH4YA29dcOURYvg56VdNdQBrA/) of MSRTVV at gdreive
- Execute **clustering.ipynb**

## Distillation
- Create directions: "outputs"
- Create 4 direction: "val_checkpoint/studentModel_best", "train_checkpoint/studentModel_current", "studentModel", "Epoch_checkpoints"
- Execute **training_lets_go_distill.ipynb**
  To obtain 4 separate clusters and an additional student model as the control group, it is necessary to run the training_lets_go_distill.ipynb five times. Each run involves selecting one from the "for all videos training" and four "for cluster videos training" options for execution.

## Ensemble & Testing
- Create directions: "student_models/Cluster_0" ect.
- After complete the training of one cluster, copy the 3 files "**model.safetensors**", "**generation_config.json**", "**config.json**" at "outputs/val_checkpoint/studentModel_best" into corresponding folder.
- Run **Ensemble.ipynb**

## Inference with Completed Data 
- For Inference the model without re-build the model.
- Download [trained student models](https://drive.google.com/drive/folders/1nIZgixmE2lREckPZ8pRNIGxSHbp_4iNs?usp=sharing/).
- Run **Ensemble.ipynb**
