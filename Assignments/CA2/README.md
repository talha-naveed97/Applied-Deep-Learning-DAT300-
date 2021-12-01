# Background
We have been tasked by scientists to assist them in doing an analysis of the spread of birch trees in a local forest.

The scientists have given us flyover photos of a local forest and corresponding image masks showing where in the image birch trees are. The image masks consist of binary values (0=not birch, 1=birch) and the goal is to use the dataset to train a model to perform semantic segmentation.

https://github.com/talha-naveed97/Applied-Deep-Learning-DAT300-/blob/main/Assignments/CA2/Birch.jpg

![Alt text](./Applied-Deep-Learning-DAT300/Assignments/CA2/Birch.jpg?raw=true "Title")

You will participate in an InClass Kaggle competition. Only students enrolled in the DAT300 course are allowed to participate.

Link to our InClass competition on Kaggle:
Tree segmentation in images (Links to an external site.)

Link to participate
https://www.kaggle.com/t/fbe6ffeb6102400ab1e1f1cc6b1671d9 (Links to an external site.)


# Context of the compulsory
The data is stored in HDF5 format. You can access images (X) and masks (y) directly and use these in your models with the h5py package (Links to an external site.) or through the TensorFlow I/O package (Links to an external site.). It is recommended to develop your code in a Kaggle notebook. In addition, you are expected to run at least one model on the Orion cluster.

Familiarising: Before any modelling, visualise examples of the raw data and masks in your Jupyter notebook.
Basic U-NET: Create a U-Net with optional dropout. Use a proportion of the images for validation when training. The minimum requirement is to tune the following parameters: number of convolutional filters, dropout and learning rate.  Report strategies and scores leading up to the final choice. If time permits, we recommend adding augmentation (both images and masks) and changing the loss function, e.g. implementing F1 loss. Create a plot showing your model's predicted mask on some images in the training set and compare to the correct mask.
Transfer learning: Create a U-Net where the encoder part of the U-Net uses a pre-trained VGG16 (Links to an external site.). This can be achieved by loading a pre-trained model, dropping the final layer and freezing the weights. Add skip connections from the Conv2D layers of the VGG16-based encoder to the expansion layers of the decoder. If time allows, experiment with changing the same hyperparameters as in the basic U-Net and un-freezing layers in the encoder. Report on the performance of the model and discuss why/why not this might be a suitable task for transfer learning.
Compute cluster: Details on Orion logon will be made available here. After creating your models, you should upload at least one of these to Orion for testing and possibly tuning. The minimum requirement is to run one model one time, reporting your slurm-script, username, code to access data on Orion and time usage for your modelling, and uploading the predictions to Kaggle (in addition you may submit many solutions directly from Kaggle notebooks). Make sure your first run is limited in epochs and parameter choices so you can estimate resource use before running larger jobs. Due to limited resources (12 GPUs), try to limit single jobs to run for less than 2 hours. Send multiple jobs to the slurm queue if you need more time for more tuning and testing.

# Deliverables / submissions
To have the compulsory assignment approved you need to deliver the following:

Your group must appear on the leaderboard of our Kaggle competition, which means that you must submit at least one prediction. Your submission can be made with either the model in task 1 or 2. At least one submission must originate from a job on Orion, and you can submit up to 20 submissions per day.
Try to beat the Benchmark F1-score: 0.96177.
Submit a Jupyter notebook + PDF of Jupyter notebook on Canvas with the code for training of your best model in addition to the requirements described above. Please make short comments throughout your notebook/code on what you are doing and how you choose the parameters of your final best regression model. A Jupyter notebook template is provided here. (Links to an external site.)
Provide your Kaggle group name AND your real names at the beginning of your Jupyter notebook.
Co-operation across groups is valuable, but do not copy code or text. If your solution has been strongly inspired by another group, give them credit in your hand-in, just like you would cite articles, blogs or other sources if you base part of your solution on someone else's work.
