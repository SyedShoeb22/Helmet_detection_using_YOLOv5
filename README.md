# Helmet_detection_using_YOLOv5
Building a Helmet Detection model using YOlOv5
    • I firstly needed to clone YOLOv5 repository from git and upload the images and annotations into the ‘data’ folder of repository.

Training:
    • After the above step, trained the model for 40 epochs, batch 40.
![image](https://user-images.githubusercontent.com/99830705/201469567-84d87387-ac7f-45db-a38b-6e021799334a.png)

									
    • In dataset.yml file we have to define the path of images, labels, path, classes name and how many classes are there in the training dataset.
    • After training for 40 epochs got precision of 0.92, recall 0.90 and mAP_0.5 as 0.95.
    • After training downloaded the ‘last.pt’ file in this files the trained weights gets saved then using this files made predictions on the provided test images.

Loading model:
    • model = torch.hub.load('ultralytics/yolov5', 'custom', path=r'D:\CV intern\last.pt', force_reload=True)

Prediction:
    • Predicting on images the model is able to easily detect the helmets as can be seen in below image.


![image](https://user-images.githubusercontent.com/99830705/201469606-1c3aed8d-c026-4d3c-a965-2eb366991448.png)









https://user-images.githubusercontent.com/99830705/201469929-0f5be335-2e32-445b-b50a-b4f86f32eda7.mp4









    • Following code is used to process the YouTube video with the detections.

![image](https://user-images.githubusercontent.com/99830705/201469625-ea412cd9-e7ef-4e8a-b2ce-de08cb7818ac.png)

