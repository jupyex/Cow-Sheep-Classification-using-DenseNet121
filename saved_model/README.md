# Cow Sheep Classification using DenseNet121
## Performing Forward Inference
Let's say if you want to use the model to classify an image as a cow or sheep. You may type the following code to perform forward inference:
```python
import tensorflow as tf
loaded_model = tf.saved_model.load(saved_model_path) #specify the location where you saved the model
test_img = imread("test.jpg") #specify file name
test_img = resize(test_img, (160,160,3))
test_img = np.expand_dims(test_img, axis=0)
predictions = loaded_model(test_img)
```
