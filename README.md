# computer_vision

# camera intrinsics: Matrix K

|-------| Col 1 | Col 2 | Col 3 |
|-------|-------|-------|-------|
| Row 1 |  fx   |   0   |  x0   |
| Row 2 |  0    |  fy   |  y0   |
| Row 3 |  0    |   0   |   1   | 

<small>x0, y0 are image center shifts. Image center shifts are just that the image center may not align with the center of the camera. <br> </small>
<small> fx, fy, are focal length of x and y coordinates.</small> <br> <br>
<small> I believe this translates from the pixels in the cameras sensor, to the digital field of view, then the camera intrinsics ,K, multiplied by the camera extrinsics (Rw Tw) translates to the cameras world view.

# camera extrinsics: (cRw cTw) 

|-------| Col 1 | Col 2 | Col 3| Col 4 |
|-------|-------|-------|------|-------|
| Row 1 |  r11  |  r12  | r13  |  t1   |
| Row 2 |  r21  |  r22  | r23  |  t2   |
| Row 3 |  r31  |  r32  | r33  |  t3   |

<small> These matrices should be separated (the r's and the t's) and multiplied together </small>


#From camera frame to cars frame.
|-------|    Col 1     |    Col 2     |     Col 3     |
|-------|--------------|--------------|---------------|
|-------|    Xcam      |    equals    |     Ycar      |
|-------|    Ycam      |    equals    | Zcar + Hmount |
|-------|    Zcam      |    equals    |     Xcar      |  

<small> Camera frame to car frame. The optical axis Z is the cars X axis for the f1tenth. </small>
 
