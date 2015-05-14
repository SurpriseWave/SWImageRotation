# SWImageRotation
iOS project to rotate and flip image.

## Features:
- Rotate Left
- Rotate Right
- Rotate at angle
- Flip verticaly
- Flip Horizontally
- Save final image

## How to use it
1. Add **_UIRotateImageView.h_** and **UIRotateImageView.m** file in your project
2. import **UIRotateImageView.h** file in View Controller.
3. Place your image view inside view. use **UIRotateImageView** insted of **UIImageView** This super view will define boundery of image.
4. Set image in code.
5. Call require method depand on your need:
	- **(void)rotateWithAngle:(CGFloat)angle;** Rotate at angle
	- **(void)rotateAtPosition:(CGFloat)radians;** Rotate Left Or Right. pass kRotateRight or kRotateLeft
	- **(void)flipHorizontally;**
    - **(void)flipVertically;**

6. Add **adjustPossition** method in view controller : After every operation we have to perform some adjustment for UI. see adjustPossition method in sample project.
7. **Grid And Other view** : This are not included in **UIRotateImageView.h** and **UIRotateImageView.m** but if you need that you can see how to implement it is sample project.
	- **Grid** : You will find a view name "Grid View" in storyboard with 6 sub view for grid. Size of grid view must be same as image view and both should be in same parent view.
	- **Other View** : There are two other view to hide unwanted image area while we rotate it at arbitrary angle.
8. Call method **finalImage** on image view to get resulted image.

### Rotate at angle : 
This is different from other operation. All other operation are performed on UIImage on-the-fly. But this rotation is performed on UIImageView first. Actual rotation performed on UIImage at the time of making final image. Reason of doing so is Animation. This create smooth animation of rotation and zoom.

### Licence : MIT






