# cs6910_assignment2
# DL
## Final code file is named as # final_dl_assignment1
'''3k & sonagara'''
## report link : https://wandb.ai/sonagara/dl_a2eeeee/reports/Copy-of-sonagara-s-Assignment-2--Vmlldzo2MDgyNTE/edit

## set variables
- img_size = single dimension of image
- n_class = no of classes
- path = path for the data
- sweep_config = sweep configuration for create_model
- sweep_config = sweep configuration for train_pretrain_model

## create_model(n_filters,dropout,batchnormalize)
- n_filters = list containing filters for each layer
- dropout = dropout parameter
- batchnormalize = True/False
- also the activation,regularization parameter,maxpool size, kernal size,dense neurons can be changed by changing the parameters inside the create_model 

## train() - to train the sweep

## best_model() returns model,labels (dictonary for class labels)
for trainig the best model which we obtained by running sweep
all the parametrs in this are predefined

## load_data() - to load the three test images form each class
returns x (numpy array of scaled images), y (containg class for images in x)

## plot_test(model,labels,x,y) - for plotting the three test images form each class , the title for each images are predicted/True class lables
- model - trained model
- lables - dictonary for class labels ex {"Insecta" : 2,"fungi" : 3,etc}
x , y - load_data()

## plot_filters(img,model,layer_no = 1) - for plotting all filters of any conv layers
- img = any single img with shape(img_shape,img_shape,3)
- model = trained model
layer_no = default 1 , any conv layer no of model whose filter you need to visulaize

## plot_guided_backprop() - for doing guided back propagation on any 10 neurons for the conv5 layer and plotting the images which excite them
- all the parametrs are hancoded it can be changed inside the plot_guided_backprop() for doing guided back prop on any other layes

## load_pretrained_model(name,k = False,default_shape = False) - to load pretrianed model
- name = 'vgg16' , 'resnet50' , 'inception_v3' 
- if need to add any new pretrined model update the last_conv, i_shape and import the required modules 

## train_pretrain_model() - for training sweep on pretrained model

## train_pretrain_model(name,ds = True) - wihout sweep training pretrained model
- name = nam eof the model ex 'vgg16','resnet50' ,etc.
- ds = default_shape True/False - to train the model on its default image shape or our defined image shape
- all the parametrs in this are predefined

