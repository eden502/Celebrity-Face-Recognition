# Celebrity-Face-Recognition

For this exercise we were tasked with the following:
1. Implement a CNN using VGG16 architechture on our own - without using pytorch.
2. Train our model to predict face recognition from a custom dataset which we created in a previous task - 13 classes of celebrity faces - 20 images each.
3. Re-train 5 torchvision models that were already trained on ImageNet datasets for facial recognition.
4. Ensamble those models to create a better prediction.

    
###### VGG16 Architecture
![Screenshot](images/vgg16.png)
For our task, we altered the final FC layers to an output of 13 to fit our 13 classes.

### Results:
- After training our network for 30 epochs:</br>
![image](https://user-images.githubusercontent.com/62388816/175392604-bcdc1a1b-4b19-4f7b-a443-bc6162eb4728.png)
![image](https://user-images.githubusercontent.com/62388816/175392645-1b42a3c1-f8a8-49c7-b037-76dfafbf140c.png)

### Ensambled Models
- The pretrained models we selected are: ResNet18, AlexNet, EfficientNet-b7, GoogleNet, VGG16Net
- Individual results after re-training the networks with our data:</br>
![image](https://user-images.githubusercontent.com/62388816/175393120-8bcad3ac-66f8-47b5-8b05-7f4c8d38185b.png)
![image](https://user-images.githubusercontent.com/62388816/175393153-36995fe4-e07d-459f-ad06-1871795aa258.png)
- Each model recieved a weight based on its performance in training.
- To ensamble the results we used a weighed average algorithm.
- Average model predictions were 67.28%
- Ensambles model predicion was 88.4%
- Detailed results are described in Intro to CV - Ex3.ipynb


