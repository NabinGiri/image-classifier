# image-classifier
Python Jupyter notebook with Convolutional Neural Network image classifier implemented in keras with Google Colab. 

#Usage:
Data should be in below structure:
data/
	training/
		class_a/
			class_a01.jpg
			class_a02.jpg
			...
		class_b/
			class_b01.jpg
			class_b02.jpg
			...
	validation/
		class_a/
			class_a01.jpg
			class_a02.jpg
			...
		class_b/
			class_b01.jpg
			class_b02.jpg
			...
      
Data Preview:
Found 24585 images belonging to 2 classes. # training data
Found 496 images belonging to 2 classes. # validation data
Found 12531 images belonging to 1 classes. # testing data


Training Result: 


Log-loss (cost function):
training   (min:    0.158, max:    0.630, cur:    0.161)
validation (min:    0.066, max:    0.578, cur:    0.075)

accuracy:
training   (min:    0.624, max:    0.941, cur:    0.941)
validation (min:    0.758, max:    0.944, cur:    0.922)

Model: "sequential_1"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_1 (Conv2D)            (None, 200, 200, 32)      896       
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 200, 200, 32)      9248      
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 100, 100, 32)      0         
_________________________________________________________________
conv2d_3 (Conv2D)            (None, 100, 100, 64)      18496     
_________________________________________________________________
conv2d_4 (Conv2D)            (None, 100, 100, 64)      36928     
_________________________________________________________________
max_pooling2d_2 (MaxPooling2 (None, 50, 50, 64)        0         
_________________________________________________________________
conv2d_5 (Conv2D)            (None, 50, 50, 128)       73856     
_________________________________________________________________
conv2d_6 (Conv2D)            (None, 50, 50, 128)       147584    
_________________________________________________________________
max_pooling2d_3 (MaxPooling2 (None, 25, 25, 128)       0         
_________________________________________________________________
conv2d_7 (Conv2D)            (None, 25, 25, 256)       295168    
_________________________________________________________________
conv2d_8 (Conv2D)            (None, 25, 25, 256)       590080    
_________________________________________________________________
max_pooling2d_4 (MaxPooling2 (None, 12, 12, 256)       0         
_________________________________________________________________
flatten_1 (Flatten)          (None, 36864)             0         
_________________________________________________________________
dense_1 (Dense)              (None, 256)               9437440   
_________________________________________________________________
dropout_1 (Dropout)          (None, 256)               0         
_________________________________________________________________
dense_2 (Dense)              (None, 256)               65792     
_________________________________________________________________
dropout_2 (Dropout)          (None, 256)               0         
_________________________________________________________________
dense_3 (Dense)              (None, 1)                 257       
_________________________________________________________________
activation_1 (Activation)    (None, 1)                 0         
=================================================================
Total params: 10,675,745
Trainable params: 10,675,745
Non-trainable params: 0
_________________________________________________________________
