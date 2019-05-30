# Car-parking Spaces detection by using MRCNN on Google Colab

This is an implementation of detecting empty car parking spaces and sending the user a notification once it finds it. This project uses the 
Google Colab platform, Since I DONT HAVE A GPU 😛 . Both the input and output are read and written to Google drive. 

This project mainly has three parts :-
1. Detecting the object i.e car in this case
2. Detecting the empty car parking spaces
3. Sending a notification message

## 1. Detecting the car

The car detection part uses the Mask R-CNN model to identify the objects. We filter out and draw bounding boxes on only Car, Truck and 
Bus since these spaces can be used for car parking.

## 2. Detecting the empty car parking spaces

For this, we first need to understand that the Valid car parking spaces are the spaces occupied by the stationary cars. This is an easy way to 
detect the parking spaces. So when on these valid parking spaces becomes empty, we can imply that we have found an empty parking space.

## 3. Sending a notification

Once we detect an empty parking space, its time to send a notification message to the user. For messaging service, we use Twilio.


## References

1. https://medium.com/@ageitgey/snagging-parking-spaces-with-mask-r-cnn-and-python-955f2231c400 - This is a wonderful post by Adam
   Geitgey which motivated me to build this project.
2. https://github.com/matterport/Mask_RCNN - Mask RCNN implementation.
