# Auto-Assistance-System-for-visually-impaired

The World Health Organization (WHO) reported that there are 285 million visually-impaired people worldwide. Among these individuals,   there are 39 million who are totally blind. There have been several systems designed to support visually-impaired people and to improve the quality of their lives. One of the most difficult activities that must be conducted by visually impaired is indoor navigation. Inindoor environment, visually impaired should be aware of obstacles in front of them and be able to avoid it. The use of powered wheelchairs with high transportability and obstacle avoidance intelligence is one of the great steps towards the integration of physically disabled and mentally handicapped people. The disable person will not be able to visualize the object so this Auto-assistance system may suffice the requirement. Auto-Assistance System operating in dynamic environments need to sense its surrounding environment and adapt the control signal in real time to avoid collisions and protect the users. Auto-Assistance System that assist or replace user control could be developed to serve for these users, utilizing systems and algorithms from Auto-Assistance robots. This systemcould be used to assist disable in their mobility by warning of obstacles. The system could be used in indoor environment like hospital, public garden area. So, we are designing an Auto-assistance system which will help the visually impaired person to work independently. In this system we would be detecting the obstruction in the path of visually impaired person using USB Camera & help them to avoid the collisions.

# Dependencies (Windows 10 Opearting System)
## _Hardware Requirements_ ##
NVIDIA GPU card with compute capability 3.5 or higher. Check your NVIDIA GPU card is CUDA enabled or not **[CUDA Enabled GPU](https://developer.nvidia.com/cuda-gpus)**

## _Software Requirements_ ##
* #### Anaconda Python 3.6/3.7 - [https://www.anaconda.com](https://www.anaconda.com/distribution/)
* #### Opencv Library version - [https://opencv.org](https://opencv.org/releases/) 
* #### Tensorflow Library version - [https://www.tensorflow.org](https://www.tensorflow.org/install) [Recommended version 1.10.0] 
* #### NVIDIA GPU Driver - [nvidia.com](https://www.nvidia.com/Download/index.aspx?lang=en-us)  CUDA 10.0 requires 410.x or higher.
* #### CUDA Toolkit - [NVIDIA CUDA](https://developer.nvidia.com/cuda-toolkit-archive) TensorFlow supports CUDA 10.0 (TensorFlow >= 1.13.0) [Recommended Tensorflow version 1.10.0 & CUDA toolkit version 10.1]
* #### cuDNN SDK - [CUDA Deep Neural Network Library](https://developer.nvidia.com/rdp/cudnn-archive) CUDA 10.0 requires >= 7.4.1 [Recommended cuDNN version 7.5.0 for CUDA 10.1]
* #### Visual Studio 2019 - [https://visualstudio.microsoft.com](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=Community&rel=16) [Recommended visual studio version - 2019 community]
* #### Raspbian OS - [Raspbian Stretch with desktop and recommended software](https://www.raspberrypi.org/downloads/raspbian/)

## **Installation Process Sequence**
1. Install Visual Studio 2019 community **_(Packages: .NET, Data Science, python development, c++, Node.js)_**
2. Install CUDA **(Computer Unified Device Architeure)** Toolkit **_(version: 10.1)_**
3. Install cuDNN Library **_(version: 7.5.0 for CUDA 10.1)_**
4. Install Anaconda python interpreter **_(version: 3.6/3.7)_**
5. Install opencv Library
6. Install tensorflow-gpu library **_(version: 1.10.0)_**

## **How to install Opencv library through Anaconda Prompt**
Just open the Anaconda Prompt and use this command `(Windows OS)`
~~~~
pip install opencv-python
pip install opencv-python==_version_
~~~~
Just open the terminal and use this command `(Raspbian OS for Raspberry Pi)`
~~~~
sudo apt-get update
pip install python-opencv / sudo apt-get install python-opencv  (for Python 2)
pip3 install python-opencv  (for Python 3)
~~~~

## **How to install Tensorflow-GPU library through Anaconda Prompt**
Just open the Anaconda Prompt and use this command `(Windows OS)`
~~~~
pip install tensorflow-gpu
pip install tensorflow-gpu==_version_  (Example: 1.10.0, 1.12.0, 1.13.0)
~~~~
Just open the terminal and use this command `(Raspbian OS for Raspberry Pi)` [These commands are only for Raspberry pi module 3, 3B or 3B+]  _(**Reference:** [HOW TO INSTALL TENSORFLOW ON RASPBERRY PI](https://www.raspberrypi.org/magpi/tensorflow-ai-raspberry-pi/))_
~~~~
sudo apt-get update
sudo apt install libatlas-base-dev
pip install tensorflow==_version_  (for Python 2)
pip3 install tensorflow / pip3 install tensorfow==_version_  (for Python 3)
~~~~

## **How to install Visuall studio, CUDA Toolkit, cuDNN library and Anaconda**
[1] [TensorFlow GPU Full & Latest Installation Tutorial + (DLL Error Solution & Installation on Anaconda)](https://youtu.be/7QLvYL22KkM)

[2] [How to install Tensorflow-GPU on Windows 10](https://youtu.be/HExRhnO5Mqs)

[3] [How to install Tensorflow GPU | 2019 | LATEST | Windows | From Scratch Installation](https://youtu.be/D1Cx2pil4jI)

## **HAAR-CASCADE Algorithm for object detection**
A Haar Cascade is basically a classifier which is used to detect the object for which it has been trained for. The Haar Cascade is trained by superimposing the positive image over a set of negative images. The training is generally done on a server and on various stages. Better results are obtained by using high quality images and increasing the amount of stages for which the classifier is trained. One can also used predefined Haar Cascades which are available on [Haar-Cascade Pretrained Files](https://github.com/opencv/opencv/tree/master/data/haarcascades)

**_Object Detection_**

| Person  | Mug | Tennis-Ball |
| ------------- | ------------- | ------------- |
| ![Human](https://user-images.githubusercontent.com/43854300/57829642-3e602480-77cd-11e9-8215-8a24ef983a18.png)  | ![Mug](https://user-images.githubusercontent.com/43854300/57829353-4ec3cf80-77cc-11e9-9a43-67de0d30ee97.png)  | ![Tennis Ball](https://user-images.githubusercontent.com/43854300/57829268-0a383400-77cc-11e9-95bd-89aa255470b7.png) |

**_References_**

[1] [Haar Cascade Object Detection](https://pythonprogramming.net/haar-cascade-face-eye-detection-python-opencv-tutorial/)

[2] [Make your own Haar Cascade on Windows | Quick & Simple](https://youtu.be/Dg-4MoABv4I)

[3] [Bulk Image Converter](https://sourceforge.net/projects/bulkimageconver/)

[4] [Ant-Renamer](https://filehippo.com/download_ant_renamer/)

[5] [Rapid object detection using a boosted cascade of simple features](https://ieeexplore.ieee.org/document/990517)

## **YOLO (You Only Look Once) Algorithm for object detection**
YOLO is an extremely fast real time multi object detection algorithm. YOLO stands for “You Only Look Once”. The algorithm applies a neural network to an entire image. The network divides the image into an S x S grid and comes up with bounding boxes, which are boxes drawn around images and predicted probabilities for each of these regions. The method used to come up with these probabilities is logistic regression. The bounding boxes are weighted by the associated probabilities. For class prediction, independent logistic classifiers are used.

**_Object Detection_**

| Person  | Mug | Tennis-Ball |
| ------------- | ------------- | ------------- |
| ![Human](https://user-images.githubusercontent.com/43854300/57830252-28536380-77cf-11e9-8cd4-4d8ae430e882.png) | ![Mug](https://user-images.githubusercontent.com/43854300/57830681-7c127c80-77d0-11e9-8f5f-b18d61b54ac9.png) | ![Tennis Ball](https://user-images.githubusercontent.com/43854300/57830571-23db7a80-77d0-11e9-9bf5-9dc09c7d3357.png) |

**_References_**

[1] [yoloV3](https://pjreddie.com/darknet/yolo/)

[2] [yoloV2](https://pjreddie.com/darknet/yolov2/)

[3] [Image Detection with YOLO v2 Real Time YOLO with Webcam](https://youtu.be/-_RLK6RFqSc)

[4] [You Only Look Once: Unified, Real-Time Object Detection](https://pjreddie.com/media/files/papers/yolo.pdf)

[5] [Pascal VOC 2007 + 2012 dataset (Images + Annotations)](https://pjreddie.com/projects/pascal-voc-dataset-mirror/)

[6] [MS COCO dataset 2017](http://cocodataset.org/#download)
