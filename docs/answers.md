# import tesnorflow as tf

# from tensorflow import keras

# from tensorflow.keras import layers, optimizers

# import numpy as np

# mnist_data = keras.datasets.mnist

# (images_train, _),(_, _) = mnist_data.load_data()

# View Data type, dimensions, and value range of the loaded data `images_train`
print("Datatype:", images_train.dtype)
print("Shape:", images_train.shape)
print("Dimensions:", images_train.ndim)
print("Minimum value:", images_train.min())
print("Maximum value:", images_train.max())

# loaded_image_samples = images_train[:6] 

# images = images.reshape(-1, 28, 28, 1).astype('float32')       

# images_preprocessed = images_preprocess(images_train) 

# BUFFER_SIZE = images_train.shape[0]   

# NOISE_SIZE = 100

# generator = keras.Sequential ([        

# layers.Dense(7*7*128, input_shape=(NOISE_SIZE,), use_bias=True),   

# layers.Conv2DTranspose(64, (5, 5), strides=(2, 2), padding='same', use_bias=False),

# the dimension of the 2D latent image after upsampling by the transposed convolution layer is 14X14, since the stride step is 2 for all of its spatial dimensions.


# layers.LeakyReLU(alpha=0.2), 

# layers.Conv2DTranspose(32, (3, 3), strides=(2, 2), padding='same', use_bias=False),

# layers.BatchNormalization(),

# layers.LeakyReLU(alpha=0.2),

# layers.Conv2DTranspose(1, (3, 3), strides=(1, 1), padding='same', use_bias=False, activation='tanh'),

# image_dim =(28, 28, 1)

# discriminator = keras.Sequential([      

# layers.Conv2D(64, (5, 5), strides=(2, 2), input_shape=image_dim, padding='same'),

# layers.LeakyReLU(alpha=0.2), 

# layers.Dropout(0.3),    

# layers.Conv2D(128, (3, 3), strides=(2, 2), padding='same'), 

# layers.LeakyReLU(alpha=0.2), 

# layers.Dropout(0.3),    

# layers.Conv2D(256, (3, 3), strides=(2, 2), padding='same'),      
# layers.LeakyReLU(alpha=0.2),     
# layers.Dropout(0.3),  

# layers.Flatten(),    

#     layers.Dense(units=1, activation='sigmoid')    

# my_optimizer = optimizers.Adam(learning_rate=0.0002, beta_1=0.5)

#
discriminator.compile(
        optimizer=my_optimizer,
        loss=keras.losses.BinaryCrossentropy()
       )    
#

# The total number of parameters in the whole DCGAN model is 1,232,161.

# dcgan.compile(optimizer=my_optimizer,
              loss=keras.losses.BinaryCrossentropy()
             )

#         discriminator.trainable = True     

#         discriminator.trainable = False  

#         dcg_loss = dcgan.train_on_batch(noise_inputs, labels_real) 
