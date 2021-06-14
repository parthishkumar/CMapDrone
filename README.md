# CMapDrone
Building contour maps for non-flat areas using Drone

For identifying contours on geographical images captured from a camera on drone, a popular method is to develop an orthomosaic from overlapping aerial photographs. Thus, a 2D contour map is developed that is free of distortion. In recent developments, instead of stitching 2D images, the 3D video game like DEM is available. The NDVI imagery is used to identify images using infrared detection facility.
In this project, the color intensity of images is used to highlight the geographical identities on earth through the Open Computer Vision libraries of the cv2 module in Python. This module offers image capturing and manipulation functions through the gray scale image of a BGR/HSV image. The two images, viz. Image1 (The Ganges river near Patna, Bihar as recorded by NASA Earth Observatory) and Image2 (The peak of Mount Everest), are observed to plot the prominent geographies on pixel difference concept.

The Ganges river near Patna, Bihar – contour map of the river

To identify the river contour, thresholding of the gray image is done with inverted to zero simple thresholding method. The contours are obtained by calling the findContours function of cv2. All possible contour approximation algorithm and contour retrieval algorithm are tested for the best results. The drawContours method of cv2 draws contours on the specified image. A Red Gray color map is used to display the gray scaled image, the original image, and the contoured image. The code is executed in JUPYTER NOTEBOOK and attached for verification.

The peak of Mount Everest – contour map of the mountain

To identify the mountain peak, the bright and deep color intensities are identified separately. This is done using THRESHOLD_BINARY and THRESHOLD_BINARY_INV simple thresholding. The RETR_TREE for contour approximation  and CHAIN_APPROX_NONE for contour retrieval are used. The two contour plots are overlapped using two for loops to draw contours. Please refer to the attached “Contour Maps from Drone.ipynb” file for referencing the code and the steps. The information may be labeled on the contoured image by accurately ascertaining geographical locations.
