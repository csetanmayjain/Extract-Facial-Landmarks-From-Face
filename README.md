# Extract Landmarks From Face

 Detect Facial landmarks in a face.
 
Facial landmarks are used to localize and represent salient regions of the face, such as:
1. Mouth
2. Eyebrow
3. Eye
4. Nose
5. Jaw

In this program we try to detect the following facial landmarks using dlib, OpenCV, Python and then print and store those landmarks in a file.
1. Mouth
2. Inner Mouth
3. Right Eyebrow
4. Left Eyebrow
5. Right Eye
6. Left Eye
7. Nose
8. Jaw

# Understanding dlib’s facial landmark detector
The pre-trained facial landmark detector inside the dlib library is used to estimate the location of 68 (x, y)-coordinates that map to facial structures on the face.

These annotations are part of the 68 points iBUG 300-W dataset which the dlib facial landmark predictor was trained on.
![](images/facial_landmarks_68markup.jpg)


# Installation
Packages Required
1. imutils
2. numpy
3. argparsedlib
4. cv2

# How to run
Python program and dlib should be in the same directory or give the path manually

Argument

python program_namepath_of_trained_model source_image_path

Example

python detect_face_parts.py --shape-predictor shape_predictor_68_face_landmarks.dat --image images/example_01.jpg

# Input

Input Image
![](images/picture.jpg)


# Output

Left Eye
![](Screenshots/left_eye.png)

Right Eye
![](Screenshots/right_eye.png)

Left Eyebrow
![](Screenshots/left_eyebrow.png)

Right Eyebrow
![](Screenshots/right_eyebrow.png)

Node
![](Screenshots/nose.png)

Mouth
![](Screenshots/mouth.png)

Inner Mouth
![](Screenshots/inner_mouth.png)

Curve

![](Screenshots/curve.png)


# Details Regarding Content of Folders and Files

1. Extracted Features :- Contains the extracted landmarks from face in numpy.
2. Screenshots :- Contains the screenshots of output images
3. images :- Contains the sample input image and example of facial landmark features in an image
4. detect_face_parts.py :- Source program in Python
5. shape_predictor_68_face_landmarks.dat :- Model for extracting landmark
6. helpers.py :- Replace it with your current helpers.py present in "imutils/face_utils/helpers.py". 

# Troubleshoot

Quite possible, after you will run it, you will face following error
"imutils/face_utils/helpers.py", line 83, in visualize_facial_landmarks color[i] index out or range"

Solution
FACIAL_LANDMARKS_68_IDXS provides 8 landmarks but only seven colors are present in imutils, helper file(imutils/face_utils/helpers.py) in line 65 which leads to index out of range.
To resolve this add one more color to it or you can replace your existing helper file, with the file present in this repository.

