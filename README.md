# SIIM-ISIC-Melanoma-Classification
Skin cancer is prevalent, with melanoma causing 75% of skin cancer deaths. The Society for Imaging Informatics in Medicine and the International Skin Imaging Collaboration aim to improve melanoma diagnosis accuracy by developing image analysis tools using patient-level contextual information. Early detection increases chances of cure.

## Dataset Description
What should I expect the data format to be?
The images are provided in DICOM format. This can be accessed using commonly-available libraries like pydicom, and contains both image and metadata. It is a commonly used medical imaging data format.

Images are also provided in JPEG and TFRecord format (in the jpeg and tfrecords directories, respectively). Images in TFRecord format have been resized to a uniform 1024x1024.

Metadata is also provided outside of the DICOM format, in CSV files. See the Columns section for a description.

## What am I predicting?
You are predicting a binary target for each image. Your model should predict the probability (floating point) between 0.0 and 1.0 that the lesion in the image is malignant (the target). In the training data, train.csv, the value 0 denotes benign, and 1 indicates malignant.

## Files
train.csv - the training set
test.csv - the test set
sample_submission.csv - a sample submission file in the correct format
Columns
image_name - unique identifier, points to filename of related DICOM image
patient_id - unique patient identifier
sex - the sex of the patient (when unknown, will be blank)
age_approx - approximate patient age at time of imaging
anatom_site_general_challenge - location of imaged site
diagnosis - detailed diagnosis information (train only)
benign_malignant - indicator of malignancy of imaged lesion
target - binarized version of the target variable
Please cite the dataset under CC BY-NC 4.0 with the following attribution:

## Credits
>The ISIC 2020 Challenge Dataset https://doi.org/10.34970/2020-ds01 (c) by ISDIS, 2020
>
>Creative Commons Attribution-Non Commercial 4.0 International License.
>
>The dataset was generated by the International Skin Imaging Collaboration (ISIC)
>and images are from the following sources: Hospital Cl??nic de Barcelona,
>Medical University of Vienna, Memorial Sloan Kettering Cancer Center,
>Melanoma Institute Australia, The University of Queensland, and the
>University of Athens Medical School.
>
>You should have received a copy of the license along with this work.
>
>If not, see https://creativecommons.org/licenses/by-nc/4.0/legalcode.txt or 
>https://www.kaggle.com/competitions/siim-isic-melanoma-classification/data.

  
## Import Data
```
kaggle competitions download -c siim-isic-melanoma-classification
```
