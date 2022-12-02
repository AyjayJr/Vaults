# What to do

- Finish presentation PART 1 within the next 2 or 3 days
	- first part is an overview of the paper in about 1 minute
	- second part is that we will walk through each of the figures, equation, and table in the paper and from me reading the paper twice i will know if i understand those figures or not
- Second presentation is anywhere from 2 - 3 weeks after the first one
	- explanation of the entire paper that exhibits a deep understanding
	- be able explain to a highschool student

---
# Read and comprehend the following article

[RM-Depth: Unsupervised Learning of Recurrent Monocular Depth in Dynamic Scenes](https://openaccess.thecvf.com/content/CVPR2022/papers/Hui_RM-Depth_Unsupervised_Learning_of_Recurrent_Monocular_Depth_in_Dynamic_Scenes_CVPR_2022_paper.pdf)

---
# Article outline

## Abstract

**Monocular Depth Estimation** is the task of estimating the depth value (distance relative to the camera) of each pixel given a single (monocular) RGB image. This has shown promising results with undupervised training methods, but it requires images without motion. This paper proposes a learning framework that can jointly predict depth and 3D motion in a single image.

## Introduction

Scene geometry generally involves estimating depth, camera motino, and optical flow from a single image. Unlike depth from triangulation, single-image depth estimation is inherently ill-posed. Convolutional neural networks and usupervised methods have acheieved appealing performance in estimation as of lately but their successes primarily rely on there being two images both without motion. In this paper, an unsupervised learning framework of recurrent monocular depth, dubbed RM-Depth, is proposed to jointly predict depth, camera motion, and motion field of moving objects without requiring static scenes. The contributions of this work are as follows:

1. Recurrent modulation unit
	- iteratively refine the fusion by adaptive modulating of the encoder features using the hidden state of the decoder
2. Residual upsampling
	- usually a single set of filters is used, this paper proposes the use of multiple sets of filters
3. Motion field of moving objects
	- This breaks down the scene rigidity assumption and allows to use general videos for the unsupervised learning

## Related work

**Figure 1**
- Overview of unsupervised learning framework
- in the motion network images are warped towards the target image using the novel view synthesis equation
- the depth network uses RMUs to fuse encoder and decoder features.

## Depth from a single image

Usupervised learning of single-image depth estimation is achieved byu training two networks together. The depth network takes an image as input and gradually predicts the scene depth.
The pose network estimates camera motion for each image pair. Points on the initial image are warped towards the target image. This is the driving force behind the unsupervised training. The proposed framework, RM-Depth, utilizes Recurrent Modulation Units (RMU) to adaptively combine encoder and decoder features.

### Perspective projection

**Equation 1**
- D is the depth map
- a point, x, on I is the image projection from a 3D point, p 
- Once D(x) is given, p can be recovered by back-projection as follows
- Basically it seems like this figure is showing how to project a 2d image into 3D space.

### Novel view synthesis

**Equation 2**
- this figure seems to show how we can synthesize another image at a different viewpoint in the scene as if it was taken by the same camera
- this is used to warp the source images to the points in the target image 

## Recurrent depth network

**Equation 3**
- showing how the RMU takes the upsampled decoder feature and fuses it with the corresponding encoder feature through a concatenation followed by a convolution layer.

**Figure 2**
- an example of the difference between a convetional depth network and one involving RMUs
- here we can see how the RMUs fuse the decoder features with the encoder features

## Recurrent Modulation Unit (RMU)

There are two componenet inside and RMU, modulation and update.

**Equation 4a/4b**
- these equations denote how the encoder features are iteratively modulated by weights and biases.
- this is the modulation component

**Figure 3**
- detail of the RMU
- the encoder feature is modulated by weight and bias
- the output is a weighted averaged between the encoder feature and the previous hidden state

**Equation 5a/5b**
- these equation shows how the hidden state of the decoder is then combined with the encoder feature.
- this is the update phase

**Equation 6**
- hidden state initialization
- this equation shows how the inital hidden state h0 is not initialized as 0 and instead results from the top level encoder

**Equation 7a/7b**
- depth inference
- the depthe map is inferred from the hidden state.

## Residual upsampling

**Equation 9**
- the general equation that shows how we can use different upsampling filters on different regions
- this enables different filters that have better accuracy on whichever region it's acting on

**Equation 10**
- this equation represents what actually happens in RM-Depth
- RM-Depth only uses low-frequency and high-frequency filters to compromise between accuracy and speed

## Object motion

**Figure 4**
- The architecture of the motion network

**Equation 11**
- shows how the object motion decoder refines the previous estimate by augmenting it with the encoder feature
- the feature warping towards the target image helps make the generation of the motion field easier

**Equation 12**
- This equation is used to surpress outliers when position x is affected by non-rigid motion

**Equation 13**
- This equation works to properly surpress undesired object motion in rigid regions

**Figure 5 - 9**
- just showing examples of how it works and comparing it against other frameworks