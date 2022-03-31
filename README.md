# Face-Mask-Detection using Faster-RCNN


![with_mask](https://user-images.githubusercontent.com/56887206/161077468-b9ef9a15-0919-4f2c-a217-3167606a3540.jpg)



![without_mask](https://user-images.githubusercontent.com/56887206/161077514-a97c11e1-7d92-4af3-b1a8-05ccd393117d.jpg)



This project is an example of transfer learning where we train our own model over the existing COCO model. 
This makes our model more accurate since the model has already learned vertical and horizontal features over the COCO dataset. 
It will be able to generalize in a much better manner.


In the project faster-RCNN has been used since it provides accurate results and is better than RCNN and fast-RCNN. 
Faster-RCNN uses the concept of region proposal networks instead of the selective search algorithm which was previously seen in RCNN and fast-rcnn. 
Rather than having a predefined number of bounding boxes, our RPN is a neural network that is able to learn the position of bounding boxes and identify objects within the box. 
It consists of a classifier using the softmax algorithm to predict the class and a regressor to determine the co-ordinates of the bounding boxes. 
RCNN used selective search and was hard coded to make 2000 bounding boxes while looking for classes. 
Faster RCNN used learning algorithms to get precise co-ordinates for bounding boxes. Since they were hard coded, and used more number of bounding boxes they were slower and took longer.


While faster-RCNN performs better but provides a very low FPS. The You Only Look Once (YOLO) algorithm improves on the FPS while maintaining Faster-RCNN level accuracy


![image](https://user-images.githubusercontent.com/56887206/161067010-c3ab014e-12e2-46d6-9e35-09d94aea634b.png)


Steps performed:
1.	Annotate images for the respective classes using a tool like labelimg. 
2.	We must first perform all the steps like creating tfrecords, creating a labelmap.pbtxt with our class names, move around some files before we can send start the training process.
3.	Post training and getting the inference graph (which contains the frozen weights) from training in the cloud we add it to our local folder to make our predictions.
4.	It is an application which will perform predictions on live video , just do a git pull and install requirements.txt and run application mask_detection_app.py



