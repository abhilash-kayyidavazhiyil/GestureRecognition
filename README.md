# GestureRecognition
GestureRecognition using deep learning techniques

**Problem Statement**

Imagine you are working as a data scientist at a home electronics company which manufactures state of the art smart televisions. You want to develop a cool feature in the smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote

The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:

Thumbs up:  Increase the volume

Thumbs down: Decrease the volume

Left swipe: 'Jump' backwards 10 seconds

Right swipe: 'Jump' forward 10 seconds

Stop: Pause the movie


Data:
https://drive.google.com/uc?id=1ehyrYBQ5rbQQe6yL4XbLWe3FMvuVUGiL

Results:

Experiment Number	Model	Result 	Decision + Explanation
1	Conv3D	Throws Generator error	Crop the images correctly, try to overfit on less amount of data
2	Conv3D	Model not trainable as a lot of parameters	Reduce the size of the image/Reduce the number of layers
3	Conv3D	Accuracy: 0.21	Increase the amount of trainable data/ reduce the filter size 
			
			
2	Conv3D	Accuracy: 0.32	Reduce Cropping
3	Conv3D	Accuracy : 0.57	crop the images and resize them

			
l-1th	Conv3D	Accuracy: 0.45	Try ConvLSTM as Conv3D not giving desired accuracy
lth	ConvLSTM	Accuracy: 0.8047


	Apply rnn after conv3D
			
Final Model	Conv - Gru	Accuracy: 0.82
	Apply conv2d with Gru Rnn is the best model 
![image](https://user-images.githubusercontent.com/16000838/111916423-4c032700-8a94-11eb-8ba8-9f955d14109e.png)


