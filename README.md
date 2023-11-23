# Face Detecton In Python Using OpenCV

# OpenCV
# OpenCV Face Detection

OpenCV, an open-source computer vision and machine learning software library, is a versatile tool with over 2500 algorithms. It's freely available for both business and academic use, providing a range of functionalities like machine learning tools, image processing, and computer vision algorithms.

## Key Features

- **Algorithms:** OpenCV offers a comprehensive set of algorithms, including those for machine learning, image processing, and vision.
  
- **Applications:** The library finds applications in various domains such as face detection, object recognition, 3D model extraction, camera calibration, motion analysis, and more.

- **Compatibility:** OpenCV supports multiple programming languages, including C++, C, Python, and Java. It's compatible with Windows, Linux, Mac OS, iOS, and Android.

- **Optimized Performance:** Written in optimized C/C++, OpenCV is designed for computational efficiency, making it suitable for real-time applications.

## Face Detection

Face detection is a crucial task with real-time applications. OpenCV addresses the challenges of face detection, considering factors like pose variation, occlusion, image orientation, illumination changes, and facial expression.

### Pre-trained Classifiers

OpenCV includes pre-trained classifiers for various tasks, stored as XML files in `opencv/data/`. Specifically, for face detection, two pre-trained classifiers are available.

Explore the capabilities of OpenCV for accurate and efficient face detection in diverse scenarios.

1.Haar Cascade Classifier

2.LBP Cascade Classifier

We will explore both face detectors in this tutorial.

# Haar Cascade Classifier

It is a machine learning based approach where a cascade function is trained from a lot of positive (images with face) and negative images (images without face). The algorithm is proposed by Paul Viola and Michael Jones.

The algorithm has four stages:

# 1.Haar Feature Selection:
Haar features are calculated in the subsections of the input image. The difference between the sum of pixel intensities of adjacent rectangular regions is calculated to differentiate the subsections of the image. A large number of haar-like features are required for getting facial features.
# 2.Creating an Integral Image: 
Too much computation will be done when operations are performed on all pixels, so an integral image is used that reduce the computation to only four pixels. This makes the algorithm quite fast.
# 3.Adaboost: 
All the computed features are not relevant for the classification purpose. Adaboost is used to classify the relevant features.
# 4.Cascading Classifiers: 
Now we can use the relevant features to classify a face from a non-face but algorithm provides another improvement using the concept of cascades of classifiers. Every region of the image is not a facial region so it is not useful to apply all the features on all the regions of the image. Instead of using all the features at a time, group the features into different stages of the classifier.Apply each stage one-by-one to find a facial region. If on any stage the classifier fails, that region will be discarded from further iterations. Only the facial region will pass all the stages of the classifier.

# LBP Cascade Classifier 

LBP is a texture descriptor and face is composed of micro texture patterns. So LBP features are extracted to form a feature vector to classify a face from a non-face. Following are the basic steps of LBP Cascade classifier algorithm:

# 1.LBP Labelling:
A label as a string of binary numbers is assigned to each pixel of an image.
# 2.Feature Vector: 
Image is divided into sub-regions and for each sub-region, a histogram of labels is constructed. Then, a feature vector is formed by concatenating the sub-regions histograms into a large histogram.
# 3.AdaBoost Learning:
Strong classifier is constructed using gentle AdaBoost to remove redundant information from feature vector.
# 4.Cascade of Classifier:
The cascades of classifiers are formed from the features obtained by the gentle AdaBoost algorithm. Sub-regions of the image is evaluated starting from simpler classifier to strong classifier. If on any stage classifier fails, that region will be discarded from further iterations. Only the facial region will pass all the stages of the classifier.

# Steps :

       # 1.Loading HaarCascadeFace Algorithm
       
       # 2.Initializing Camera
       
       # 3.Reading Frame from Camera
       
       # 4.Converting Color image into Grayscale Image
       
       # 5.Obtaining Face coordinates by passing algorithm
       
       # 6.Drawing Rectangle on the Face Coordinates
       
       # 7.Display the output Frame

# Output :

To see the output video, go to the media file and check the output video
