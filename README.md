## Surface Morphology Edge Detection and Roughness Estimation

Atomic force microscopy (AFM) is an effective tool to study morphology and texture of diverse surfaces. Atomic force microscopic analysis is ideal for quantitatively measuring the nanometric dimensional surface roughness and for visualizing the surface nano-texture of the deposited film. One is often interested in the visualization of the discontinuities present in the AFM image which contain information such as grain size, grain shape, and roughness of the film. The goal of this research is to set up a notebook to facilitate the analysis of the shape and structure representative of nanoscale objects with the Canny Edge Detector (Canny). A brief overview of how Canny works will be provided. Details on how to display, process and analyze these images can be found the GitHub folder.

Canny detector is one of the most commonly used and most effective methods in edge detection which can be used to extract the image of sharp value discontinuities in the data as thin single-pixel lines. Steps in the Canny detector are briefly summarized below: 

1.  Smooth the image with a Gaussian filter to reduce noise.
2.  Compute the gradient of using any of the gradient operators Sobel or Prewitt.
3.  Extract edge points: Non-maximum suppression.
4.  Linking and thresholding: Hysteresis

First, two steps are straight forward, note that in the second step we compute the amplitude as well as the orientation of gradients. Non-maximum suppression: At each pixel location we have four possible directions. We check all directions if the gradient is maximum at this point. After this step one will get discontinuous thin edges that need to be fixed in the next step. Hysteresis is a way of linking the discontinuous lines produced in the previous step. 

A quick test on face images with Canny detector: 

![enter image description here](https://raw.githubusercontent.com/FengyuZ1994/Canny_Edge_Detector/master/test_face.png)


Test on real AFM images with Canny detector: 

![enter image description here](https://raw.githubusercontent.com/FengyuZ1994/Canny_Edge_Detector/master/test_afm.png)

To be continued
