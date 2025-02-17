# Mussel 3D Imager

We leverage advanced 3D reconstruction techniques to enhance the accuracy of AI-based mussel analysis. Specifically, we utilize Neural Radiance Fields (NeRF), a cutting-edge 3D reconstruction tool, to generate detailed 3D models of mussel valve configurations and behavioral patterns. NeRF reconstructs 3D scenes and objects from a sparse set of 2D images.

To facilitate image capture, we developed a custom data collection system capable of imaging mussels from multiple angles. This system includes a turntable constructed from foam board, marked along the edges for reference, with a central mounting area for the mussels. A servo motor, controlled by an ESP32 microcontroller, rotates the turntable in small increments, while an ESP32 camera captures images at each step. The captured images, along with rotation degree data and timestamps, are stored on a Secure Digital (SD) card.

Additionally, several key components, such as the camera holder and turntable base, are 3D-printed. The collected images are then used to train a NeRF model using the Python-based Nerfstudio framework, and the generated 3D models can be visualized through the Nerfstudio API.

Mussel 3D reconstruction:
<img src="mussel_3D_recontruction.png" alt="Alt Text" width="600" height="400">

ESP32 based imaging system:
<img src="ESP32_Imaging_System.png" alt="Alt Text" width="600" height="400">
