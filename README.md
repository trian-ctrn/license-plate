# Abstract
-  Module used in this project:
Tensorflow, Gradio
- This project stimulates the process of license plates number recognition system in a majority parking lots located in Ho Chi Minh city.
# License-plate
Link of data: https://drive.google.com/uc?export=download&id=0B9GEvXOuYdpldG5HRV9qRUJVMFU


- 31 classes: ['0','1','2','3','4','5','6','7','8','9',
       'A','B','C','D','E','F','G','H','K','L','M','N','P','R','S','T','U','V','X','Y','Z']

- Total: 1076 pictures 
- Shape: (28,12,3)

|classes|number of pictures|
|-|-|
|0|63|
|1|54|
|2|64|
|3|13|
|4|54|
|5|62|
|6|45|
|7|20|
|8|36|
|9|37|
|A|5|
|B|54|
|C|36|
|D|52|
|E|84|
|F|12|
|G|21|
|H|60|
|K|14|
|L|18|
|M|15|
|N|25|
|P|60|
|R|30|
|S|14|
|T|5|
|U|34|
|V|11|
|X|32|
|Y|22|
|Z|24|

Note:
- My code is true when it reachs model.compile the code after that is quite not good and not percise
- I'm using image retraining: [ImageDataGenerator](https://www.tensorflow.org/hub/tutorials/tf2_image_retraining) and transfer learning: [mobilev2net](https://www.tensorflow.org/tutorials/images/transfer_learning), if you are not understand click the link 
- Please becareful that the image is converted to rgb and becareful the shape of the image
- When you want to predict an image use this: 
```
prediction_scores = model.predict(np.expand_dims(image, axis=0))
predicted_index = np.argmax(prediction_scores)
predicted_letter = label[predicted_index]
```
This is my slide about the project: [click here](https://hackmd.io/@P7mWzip8QO2j3VXVk3etyw/rkR4sQLdO#/)


- Here is my graph: 

![download (2)](https://user-images.githubusercontent.com/83942057/118450020-f35fab80-b71d-11eb-84a7-5b5c1134457e.png) 
![download (3)](https://user-images.githubusercontent.com/83942057/118450033-f8245f80-b71d-11eb-9866-ab9a41d75723.png)

# How to use
- This is like the system in the parking lot
1. Open the gradio
2. Input your name, your type of license plate and your url of that license plate
3. Submit it 
4. Then input your name,  your type of license plate and your url of that license plate again, you will see the total money you have to pay. Remember to use an unique name.
