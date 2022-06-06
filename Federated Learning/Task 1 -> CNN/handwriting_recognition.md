Handwriting Recognition:

Source : https://www.youtube.com/watch?v=XF0q-uLxM7s

  Pattern recognition is awesome
  
  Softwares Used
  1. Tensorflow
  2. Keras
  3. Numpy
  4. Matplotlib
  5. Jupyter Notebook
  
  MNIST Data set
  -> training set of 60,000 examples
  -> test-set of 10,000 examples
  -> 784 features per image
  -> each image is labelled with respective digits
  
  data = training(builds the system) + test set(check the correctness of the system)
  
  Training set
  -> used to build a model
  -> consists of a set of images used to train the system
  -> training rules and algos used give relevant info on how to associate input data with output decision
  -> system is trained by applying these algos on the dataset
  -> usually comprises 80% of the data
  
  Test set
  -> used to check whether system is producing correct output after training or not.
  -> usually comprises 20% of the data
  
  Jupyter Notebook
  -> powerful tool to present data-science projects

import tensorflow as tf
import matplotlib.pyplot as plt
import numpy as np

mnist = tf.keras.datasets.mnist
(x_train,y_train),(x_test,y_test) = mnist.load_data()
print(y_train[5])

------------------------------------------------------

plt.imshow(x_train[5])
plt.show()

--------------------------------------------------------

model = tf.keras.models.Sequential()
model.add(tf.keras.layers.Flatten())
model.add(tf.keras.layers.Dense(128,activation = tf.nn.relu))
model.add(tf.keras.layers.Dense(128,activation = tf.nn.relu))
model.add(tf.keras.layers.Dense(10,activation = tf.nn.softmax))

model.compile(optimizer='adam',loss='sparse_categorical_crossentropy',metrics=['accuracy'])

model.fit(x_train,y_train,epochs=3)

-------------------------------------------------------

predictions = model.predict(x_test)
(predictions[3])

----------------------------------------

print(np.argmax(predictions[3]))

-----------------------------------------

plt.imshow(x_test[3])
plt.show()
