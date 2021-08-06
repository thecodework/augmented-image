# Augmented Image
## Using [ARcore Sceneform Library](https://developers.google.com/sceneform/develop)

## what this project about?
- The [Augmented Images](https://developers.google.com/ar/develop/java/augmented-images) APIs in [ARCore](https://developers.google.com/ar) lets you build AR apps that can detect and augment 2D images in the user's environment,such as posters or product packaging. In this Project, we will see how to detect and augmented image and show information using a ViewRenderable or show a 3-D model. We had a requirement to show the pressure flowing through a pipe using the mobileapplication. The AR implementation was: A person should be able to see the pressure levels at certain points in a pipe.
We implemented the [ARCore](https://developers.google.com/ar) with a ViewRenderable to show the information on a card. And it looks pretty cool.

## Installation steps

There are some following steps 
- In build.gradle of App, add a [Sceneform UX library](https://developers.google.com/sceneform/reference/com/google/ar/sceneform/ux/package-summary), [Firebase ML kit](https://firebase.google.com/docs/ml-kit) and [Sceneform Assets library](https://developers.google.com/sceneform/develop/import-assets).
- Compile Option to support Java which is needed for Sceneform library.
- In Android Manifets.xml file add permission for AR features in app, Camera permission, Internet permission add meta data to make it available for "Google Play Services for AR".
- Add the ArSceneView as shown which is provided by [Sceneform ux library](https://developers.google.com/sceneform/reference/com/google/ar/sceneform/ux/package-summary).
- Install Google [Sceneform tools (beta) plugin](https://plugins.jetbrains.com/plugin/10698-google-sceneform-tools-beta-) from android studio only.
- Create an augmented image
- Add image in drawable folder in app.
- ![image](https://user-images.githubusercontent.com/78479435/128372282-3a933bc6-adbb-4d95-8e50-7aafa7ae43a3.png)
- ![rabbit](https://user-images.githubusercontent.com/78479435/128371921-c3aef354-b43f-4f0e-8472-eab501bb82ab.png)

- Match the image in camera frame with the augmented image
- If matched, place an AR Object.
- Run the App.
 
## Libraries/Dependencies with their versions :
- [Sceneform](https://developers.google.com/sceneform/develop)- Sceneform is a 3D framework that makes it easy for you to build ARCore apps without OpenGL. We are using 1.15.0 version of google.ar.sceneform.ux:sceneform-ux.
	
## Permissions :
- We are using [Camera permission](https://developer.android.com/guide/topics/media/camera) and [hardware.camera.ar permission](https://developers.google.com/ar/develop/java/enable-arcore).
	
## Output will be
- After scanning the image/poster you will see the 3D model of respective image.
- ![Screenshot_20210804-185536_2](https://user-images.githubusercontent.com/78479435/128374757-a91e6947-dc91-4e5f-856b-4c0611a4d81e.png){:height="100px" width="100px"}

## What difficulties we faced while working on project?
- In the beginning scanning the image was quite difficult for us because we are scaning ramdom images.
- ![image](https://user-images.githubusercontent.com/78479435/126997287-70ee18f3-d05c-47a4-8384-895d0bf7d6ae.png)

## How we overcome the difficulties?
- After the reseach we find that we can only scan image that we stored in our projects assets folder.
- ![rabbit](https://user-images.githubusercontent.com/78479435/128372002-1adfe918-1e79-46ef-a74c-6cfb144433d1.png)


## What we tried to do but did not succeed?
- I our scenario, we had to identify the pressure sensor. Unfortunately the android ARCore SDK does not support the 3-D objects recognition. So we were not able to identify the sensor. Instead, we added an image on top of the sensors with the‘Sensor Id’. This is what we used as an augmented image as well.

## What are our future plan regarding the development of project?
- Our future planning  about this project is to move the 3d model when we touching the screen.
