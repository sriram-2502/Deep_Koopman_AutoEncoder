# Deep Koopman AutoEncoder
DNN based Koopman autoencoder model (Project report [https://github.com/sriram-2502/Deep_Koopman_AutoEncoder/blob/main/AuE8930_Koopman_Autoencoder_Project%20(1).pdf])


Future work will extend this architecture to approximate the principle eigenfunction coordinate transformation as the encoder network.

Knowledge of the local linear eigenvalues can be exploited and impose a soft constraint on the learned basis function. 
Its easy to see how this framework makes it possible to impose combinations of constraints through the loss function. 


The tanh activation function is an example of an analytical function which satisfies the necessary gradient constraints at the origin.


![alt text](./images/NetworkArch.png)


# Setup 
Theses setups were ran in anaconda with VS code with jupyter notebook. Note, this should also be able to run in a typical jupyter notebook or google colab environment but has not been verified.
<br>
Clone the repository
Note: Repository may be quite large as results/ directory has results that contains the deep learning model and the images and graphs of the results

```
git clone https://github.com/sriram-2502/Deep_Koopman_AutoEncoder.git
```
# Folder Structure
This section gives general overview of the folder structures and each file purpose in the main repo
### Champ and Doggo Directory 
This contains files to train, load model, and save model for specific dataset relating to Champ or Doggo. Most of the files stated below should be within this directory. This let's you train, load and save the model.
### Images
Files containing images for visual purposes for github repo
### Files 
- Custom_Koopman_AE_{name} 
  - Jupyter notebook files to preprocess, train model, and save model
- load_model_{name} 
  - Jupyter notebook model to specifically load the saved models in checkpoints/
# Standard Workflow (Not verified to work) 
- If running new simulation data, create a new subdirectory to do your training. (Ex: If running Doggo dataset, create a directory named Doggo as seen in main repo)
- Copy files Custom_Koopman_AE_Doggo.ipynb (if wish to have HP tuning, copy HP file) and load_model.ipynb (load_model_animation most up to date) into your newly created directory.
  - Optional - Copy NetworkArch.txt from either /Champ or /Doggo to record architecture structure
- Start running code
```
cd <github repo>
mkdir <new_name_for_dataset_dir>
cp Custom_Koopman_AE_Doggo.ipynb load_model.ipynb <new_name_for_dataset_dir>/
```
# Stanford Doggo Workflow 
Stanford doggo consist of running mulch, rigid ground, and pebbles experiment. (Note, I believe this data has already been preprocessed as it looks too smooth to note be preprocessed, but Dakota has stated that it should not be preprocessed). Currently Doggo/ directory may contain corrupted .ipynb files. Instead copy directory of one of the Doggo experiments in the /Results directory and start training dataset. Currently, for Doggo, dataset is compiled into a csv file... One csv file should contain multiple trajectories of the experiment. Preprocessing data should have multiple trajectories with the same length...
# Champ
