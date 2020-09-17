# Udacity 课程狗的种类分类识别    
##项目概述：

    这是Udacity课程目标之一，从图像中检测出小狗或人，如果从图像中检测出小狗。
    该算法将大致识别出小狗品种。如果检测出人脸，该算法将大致识别出最相似的小狗品种。
##项目流程：
* [第 0 步](#step0)：导入数据集
* [第 1 步](#step1)：检测人脸
* [第 2 步](#step2)：检测小狗
* [第 3 步](#step3)：（从头开始）创建分类小狗品种的 CNN
* [第 4 步](#step4)：（使用迁移学习）使用分类小狗品种的 CNN     
* [第 5 步](#step5)：（使用迁移学习）创建分类小狗品种的 CNN
* [第 6 步](#step6)：编写算法
* [第 7 步](#step7): 测试算法
##项目CNN结构：

Layer (type)                 Output Shape              Param   
conv2d_1 (Conv2D)            (None, 223, 223, 16)      208       
max_pooling2d_2 (MaxPooling2 (None, 111, 111, 16)      0         
conv2d_2 (Conv2D)            (None, 110, 110, 32)      2080      
max_pooling2d_3 (MaxPooling2 (None, 55, 55, 32)        0         
conv2d_3 (Conv2D)            (None, 54, 54, 64)        8256      
max_pooling2d_4 (MaxPooling2 (None, 27, 27, 64)        0         
global_average_pooling2d_1 ( (None, 64)                0         
dense_1 (Dense)              (None, 133)               8645      
Total params: 19,189
Trainable params: 19,189
Non-trainable params: 0
_________________________________________________________________
##迁移学习
使用Xception，达到85.28%准确率
