## Intruduction

This report present the whole processes of Creating Ensemble Fusion of Case-based Distilled Student Models for Enhanced Real-time Video Summarization.

## Get Logits from Teacher Model
- Download [GenerativeImage2Text] (https://github.com/microsoft/GenerativeImage2Text)
- Replace the **decoder.py** with the provied one
- Execute **get_teacher_logits.ipynb**, located in the same directory as GenerativeImage2Text

## Clustering
- Ad short cut of [dataset] (https://drive.google.com/drive/u/0/folders/17MWu0h-yH4YA29dcOURYvg56VdNdQBrA) of MSRTVV at gdreive
- Create directions: "outputs"
- Create 4 direction: "val_checkpoint/studentModel_best", "train_checkpoint/studentModel_current", "studentModel", "Epoch_checkpoints"
- Execute **training_lets_go_distill.ipynb**

## Distillation

AA

## Ensemble & Testing

AA
