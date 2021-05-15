# license-plate
Link of data: https://drive.google.com/uc?export=download&id=0B9GEvXOuYdpldG5HRV9qRUJVMFU


- 31 classes: ['0','1','2','3','4','5','6','7','8','9',
       'A','B','C','D','E','F','G','H','K','L','M','N','P','R','S','T','U','V','X','Y','Z']

- Total: 1076 pictures 
- Shape: 28,12,3

Note:
- My code is true when it reachs model.compile the code after that is quite not good and not percise
- I'm using image retraining: [ImageDataGenerator](https://www.tensorflow.org/hub/tutorials/tf2_image_retraining) and transfer learning: [mobilev2net](https://www.tensorflow.org/tutorials/images/transfer_learning), if you are not understand click the link 
- Please becareful that the image is converted to rgb and becareful the shape of the image
- When you want to predict an image use this: 
```
prediction_scores = model.predict(np.expand_dims(image, axis=0))
predicted_index = np.argmax(prediction_scores)
predicted_letter = label[predicted_index]
