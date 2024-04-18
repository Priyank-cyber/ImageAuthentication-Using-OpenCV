# ImageAuthentication-Using-OpenCV

There are several steps included in the authentication of an image and these are:

(1) Image Loading:
The image is loaded into the system using the OpenCV library, which is a powerful tool for image processing. Once loaded, the image is displayed to verify that it has been correctly loaded.

(2) Preprocessing:
The image is converted from color to grayscale which simplifies the data, and a Gaussian blur is applied to the grayscale image to reduce noise and details. The grayscale image and the blurred image are displayed to understand the effects of preprocessing.

(3) Noise Pattern Analysis:
The system calculates the noise pattern by comparing the blurred image to the original image. The identified noise pattern is displayed, which might reveal traces of tampering.

(4) Error Level Analysis (ELA):
The image is saved with a known level of JPEG compression to prepare for error level analysis. The system calculates the ELA image by re-loading the compressed image and comparing it with the original. The ELA image is then enhanced to exaggerate the differences and displayed, potentially revealing areas of the image that have been altered.

(5) Feature Extraction:
The Canny edge detector is used on the grayscale image to identify edges. The result of the edge detection is displayed to visualize the structural information within the image.

(6) Feature Analysis:
The mean and standard deviation of the image's pixel intensities are calculated to get statistical information about the image's brightness and contrast. The variance of the Laplacian filter's output is calculated, providing a measure of the image's sharpness. The results from previous analyses are combined into a weighted score, which gives an overall assessment of the image's authenticity.

(7) Simulated Machine Learning Model:
A dataset is created, including features extracted from multiple images, to train a machine learning model. The dataset is split into training and validation sets, and a Support Vector Machine (SVM) model is trained on the dataset to learn to differentiate between authentic and tampered images. The trained model's performance is evaluated, providing metrics such as accuracy, precision, and recall. Finally, the model's prediction is used to authenticate the image, concluding the process.
