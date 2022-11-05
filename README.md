# Fine-grained-localisation

## Task introduction

Geolocation is the problem of localising a person or device in the world using sensor data. Depending on the device, the environment, and the level of accuracy required, geolocation may rely on GPS coordinates, network routing addresses, or image data. Geolocation is an important problem in many AI and computing applications, from autonomous vehicle navigation to search engine queries based on the user’s current location (e.g., “restaurants near me”).

In this project, we investigated the problem of fine-grained geolocation in a small indoor/outdoor environment (an art museum) based on pure image information. Image information is particularly important for this type of problem, because other sources of information, like GPS, may not be accurate enough to provide fine-grained position data and may not be able to distinguish between different floors in indoor environments.

## Approach

To solve the image localisation problem, we estimate which images that have been taken near a test image and use them to inform the test image location. We define two measures of similarity between images: identified share features (e.g. SIFT features) and extracted feature maps using pretrained deep convolution neural network. We identify similar images based on a mix of these two metrics. Such approach leads to surprisingly good result in localising the position of cameras where test images are taken.
