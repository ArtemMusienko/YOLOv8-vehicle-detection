![Google Colab](https://img.shields.io/badge/Google%20Colab-%23F9A825.svg?style=for-the-badge&logo=googlecolab&logoColor=white)![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)![OpenCV](https://img.shields.io/badge/opencv-%23white.svg?style=for-the-badge&logo=opencv&logoColor=white)![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)![Kaggle](https://img.shields.io/badge/Kaggle-035a7d?style=for-the-badge&logo=kaggle&logoColor=white)![Google Drive](https://img.shields.io/badge/Google%20Drive-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)![YOLO](https://img.shields.io/badge/YOLO-111F68?style=for-the-badge&logo=yolo&logoColor=white)

<img  width="2048"  height="681"  alt="image"  src="https://github.com/user-attachments/assets/692b58fe-7261-42d4-9a75-6dda7ed02c5c"  />

## YOLOv8-vehicle-detection

[![ru](https://img.shields.io/badge/README_на_русском-2A2C39?style=for-the-badge&logo=github&logoColor=white)](README.ru.md)  

It is already difficult to imagine the modern world without video surveillance cameras. Such cameras are already equipped with detection of cars, license plates, and so on. It is not always possible to obtain high-quality images of vehicles, which leads to difficulties in detection due to limited illumination. To solve such problems, you can use the **YOLO** models from **Ultralytics**. The **8** version was chosen from the family of these models. Why? It combines the maturity of the Ultralytics ecosystem with a modern architecture, providing advanced capabilities compared to its predecessors, including instance segmentation, pose/keypoint estimation, and classification.

> I strongly recommend using a **T4 graphics accelerator** or
> something more powerful!

The dataset will be used [Cars Detection](https://www.google.com/url?q=https%3A%2F%2Fwww.kaggle.com%2Fdatasets%2Fabdallahwagih%2Fcars-detection%2Fdata). In order to download it, we will need to register on **Kaggle** and get your _API key_ through the profile settings. To complete the process, you need to enter the key and nickname in the two fields provided in the interface, and then submit this information to the Kaggle server for verification.

To achieve the task of detecting vehicles in low-light conditions, we will use image augmentation. The code allows you to add only augmented images to the final dataset, as well as original and augmented images.

 We will use the medium-sized model `yolo8m.pt`, which is pre-trained for object detection. Since I am limited in computational resources, I have chosen the medium-sized model, but you can choose a more complex model that will produce better results but will require more resources.

To improve the quality of the code, you can use graphics accelerators that are more powerful than **T4**. You can also implement garbage collection, which will lead to a slight optimization of the code. Then, you can use an extended dataset, which includes both augmented and original data. I have implemented this feature at the code level using buttons. Finally, you can choose a more advanced model version, such as `yolov8l.pt` or `yolov8x.pt`, which may produce better results but require more powerful computing resources. It is possible to add more epochs to train the model, as there is clearly no overfitting. Finally, it is recommended to add a prediction function to the video.

> For more information on writing code, as well as theoretical
> part and conclusions, please refer to the paper itself!