# MALARIA-DETECTION-CNN
using CNN for classifying malaria skin images
## DISCRIPTION
>  we’ll discuss how deep learning and medical imaging can be applied to the malaria endemic.From there we’ll explore our malaria database which contains blood smear images that fall into one of two classes: positive for malaria or negative for malaria.After we’ve explored the database we’ll briefly review the directory structure for today’s project.We’ll then train a deep learning model on our medical images to predict if a given patient’s blood smear is positive for malaria or not.
>  
## DATASET
> The malaria dataset we will be using in today’s deep learning and medical image analysis tutorial is the exact same dataset that `Rajaraman et al.` used in their 2018 publication. The dataset consists of 27,588 images belonging to two separate classes:
>
> HINT:The dataset itself can be found on the [official NIH webpage](https://lhncbc.nlm.nih.gov/LHC-downloads/downloads.html#malaria-datasets)
> * Parasitized: Implying that the region contains malaria.
> * Uninfected: Meaning there is no evidence of malaria in the region.
> 
>  The number of images per class is equally distributed with 13,794 images per each respective class.the sample of dataset is similar as below:
>  
> ![dataset](https://user-images.githubusercontent.com/53394692/111433957-326c8300-8714-11eb-9c0b-9e23b8efc3d7.PNG)
## STRUCTURE of This Project
> * our dataset is assigned in `malaria` directory,as 3 seprate folderes `training`,`testing`and `validation`.each folder has two subdirectories as `Parasitized` and `Uninfected` that our images are assigned in them.
> * the architecture of autoencoder is in `pyimagesearch/resnet.py`.This file contains the exact ResNet model class included .
> * `save_model.py` is assigned to train procedure.
> * `load_modl.py` is assigned to test the algorithm.
> * `plot.png` is assinged to show train/validation loss or accuracy.
## Training Procedure
> for starting the train procedure ,you can run following command:
```
python save_model.py --dataset malaria --model saved_model.model
```
> after ending,the moodel weight is saved as `saved_model.model`,furthermore you can able to see the results,such as below:
>
![plot](https://user-images.githubusercontent.com/53394692/111466264-4d50ee80-8738-11eb-8cb4-131fa4dc68d1.png)

## Testing Procedure
> for testing model,run following command:
```
python load_model.py --images malaria/testing --model saved_model.model
```
> and see results as below:
> 
![test](https://user-images.githubusercontent.com/53394692/111469002-70c96880-873b-11eb-9683-7259482bd200.PNG)







































## License
> [Deep Learning and Medical Image Analysis with Keras](https://www.pyimagesearch.com/2018/12/03/deep-learning-and-medical-image-analysis-with-keras/) by Adrian Rosebrock



