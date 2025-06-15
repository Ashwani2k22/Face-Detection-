🔹 What is OpenCV?

OpenCV (Open Source Computer Vision Library) is a powerful open-source computer vision and machine learning library. Licensed under BSD, it is free for both academic and commercial use.

It provides over 2500 optimized algorithms for:

Image processing

Object detection and tracking

3D model extraction

Motion analysis

Camera calibration

Machine learning (classification, clustering)

OpenCV supports C++, Python, Java, and runs on Windows, Linux, macOS, Android, and iOS. It is written in optimized C/C++ for real-time applications and supports multi-core processing.

🔹 What is Face Detection?

Face detection is the process of identifying and locating human faces in images or videos. It is a fundamental step in many real-time applications such as:

Face unlock

Surveillance systems

Attendance systems

Emotion or age detection

However, it is a challenging task due to variations in lighting, facial expressions, poses, and occlusions.

🔹 Pre-trained Classifiers in OpenCV

OpenCV provides several pre-trained XML classifiers for face, eyes, and smile detection stored in the opencv/data/haarcascades/ folder. The two most widely used face classifiers are:

Haar Cascade Classifier

LBP (Local Binary Pattern) Cascade Classifier

✅ Haar Cascade Classifier

Proposed by Viola and Jones, this method uses a cascade of classifiers trained with thousands of positive and negative images.

Working Steps:

Haar Feature Selection:

Computes features by comparing the intensity between rectangular regions.

Integral Image:

Speeds up the computation using only four values per region.

Adaboost:

Selects the most relevant features.

Cascade Classifiers:

Applies a series of classifiers on image regions. If a region fails in any stage, it's rejected as a face.

✅ LBP Cascade Classifier

LBP is a texture-based method that is faster but slightly less accurate.

Working Steps:

LBP Labeling:

Each pixel is labeled with a binary number based on its neighbors.

Feature Vector:

Image is divided into regions; each region's histogram is concatenated to form a feature vector.

AdaBoost Learning:

Removes unnecessary features.

Cascade of Classifiers:

Applies stages from simple to complex to detect faces efficiently.

📊 Implementation Steps:

# 1. Load Haar Cascade face detection model
# 2. Initialize webcam using cv2.VideoCapture()
# 3. Read video frames
# 4. Convert frame to grayscale
# 5. Detect faces using detectMultiScale()
# 6. Draw rectangles around detected faces
# 7. Display the result using cv2.imshow()

🎥 Output:

A real-time video window appears, showing the camera feed with rectangles drawn around detected faces. The output video can be saved using OpenCV's VideoWriter class.
