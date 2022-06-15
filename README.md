# Head-Pose-Estimation

Simply, head pose estimation means detecting the position of a human head in the image. Particularly, it means detecting the head’s Euler angles – yaw, pitch and roll. They define the object’s rotation in a 3D environment.\
"http://personal.maths.surrey.ac.uk/T.Bridges/SLOSH/3-2-1-Eulerangles.pdf"\

<table>
  <tr>
    <td><img src=![Yaw-Pitch-Roll](https://user-images.githubusercontent.com/31386584/173800393-a53aecb3-8bc5-4fde-b8e9-638f19dc7b54.png) width=370 height=300></td>
    <td><img src=![Output(GIF)](https://user-images.githubusercontent.com/31386584/173801669-4e6c0525-da70-4139-a69b-08886990a234.gif) width=370 height=300></td>
  </tr>
 </table>

Process to detect the head pose: (Using MediaPipe & OpenCV)\
1- Download the data "http://www.cbsr.ia.ac.cn/users/xiangyuzhu/projects/3DDFA/Database/AFLW2000-3D.zip".\
2- Reading the images and using mediapipe library ("https://google.github.io/mediapipe/#:~:text=MediaPipe%20offers%20cross%2Dplatform%2C%20customizable,desktop%2Fcloud%2C%20web%20and%20IoT") to detect landmarks on faces then loading these landmarks to Pandas DataFrame.\
3- Reading the mat files for every image and extracting Pose parameters (Yaw, Pitch and Roll) then loading them to the DataFrame.\
4- Training a MultiOutput Support Vector Regressor (SVR) model.\
5- Testing the model on a live camera (Photos & Videos).\
\
\
Resources:\
1- https://indatalabs.com/blog/head-pose-estimation-with-cv#:~:text=Simply%20put%2C%20head%20pose%20estimation,rotation%20in%20a%203D%20environment.\
2- https://www.researchgate.net/figure/Orientation-of-the-head-in-terms-of-pitch-roll-and-yaw-movements-describing-the-three_fig1_279291928\
3- https://grauonline.de/wordpress/?page_id=3432\
4- https://sefiks.com/2022/01/14/deep-face-detection-with-mediapipe/
