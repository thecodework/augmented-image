# Augmented Image
## Using [ARcore Sceneform Library](https://developers.google.com/sceneform/develop)

## what this project about?
- The [Augmented Images](https://developers.google.com/ar/develop/java/augmented-images) APIs in [ARCore](https://developers.google.com/ar) lets you build AR apps that can detect and augment 2D images in the user's environment,such as posters or product packaging. In this Project, we will see how to detect and augmented image and show information using a ViewRenderable or show a 3-D model. We provide a set of reference images. Once ARCore begins tracking an image, it provides estimates for image position and orientation each frame. All tracking happens on the device. No internet connection is required to detect and track images. [ARcore](https://developers.google.com/ar) scan the image that we store in the database once an image is detected. [ARcore](https://developers.google.com/ar) create 3D image of that image.

## Installation steps

There are some following steps 
- In build.gradle of App, add a [Sceneform UX library](https://developers.google.com/sceneform/reference/com/google/ar/sceneform/ux/package-summary), [Firebase ML kit](https://firebase.google.com/docs/ml-kit) and [Sceneform Assets library](https://developers.google.com/sceneform/develop/import-assets).
- Compile Option to support Java which is needed for Sceneform library.
- In Android Manifets.xml file add permission for AR features in app, Camera permission, Internet permission add meta data to make it available for "Google Play Services for AR".
- Add the ArSceneView as shown which is provided by [Sceneform ux library](https://developers.google.com/sceneform/reference/com/google/ar/sceneform/ux/package-summary).
- Install Google [Sceneform tools (beta) plugin](https://plugins.jetbrains.com/plugin/10698-google-sceneform-tools-beta-) from android studio only.
- Create an augmented image
- Add image in drawable folder in app.
- ![image](https://user-images.githubusercontent.com/78479435/128532532-b55e2fb2-5ed6-4c64-a05e-1a25e654230f.png)
- Add glb file in assets folder in app.
- ![image](https://user-images.githubusercontent.com/78479435/128532753-6b7768ec-e1b4-4437-8fc0-9219dc75dc01.png)
- ![snsr_image (1)](https://user-images.githubusercontent.com/78479435/128531749-0104eb39-f1cf-42c2-8cb6-c98dd16d09d7.jpg)

- Match the image in camera frame with the augmented image
- If matched, place an AR Object.
- Run the App.
 
## Libraries/Dependencies with their versions :
- [Sceneform](https://developers.google.com/sceneform/develop)- Sceneform is a 3D framework that makes it easy for you to build ARCore apps without OpenGL. We are using 1.15.0 version of google.ar.sceneform.ux:sceneform-ux.
	
## Permissions :
- We are using [Camera permission](https://developer.android.com/guide/topics/media/camera) and [hardware.camera.ar permission](https://developers.google.com/ar/develop/java/enable-arcore).
	
## Output will be
- After scanning the image/poster you will see the 3D model of respective image.
- ![snsr_image (1)](https://user-images.githubusercontent.com/78479435/128597281-4500960b-5e61-4e9d-a0e4-49b8b29a232b.jpg)

## What difficulties we faced while working on project?
- In the beginning scanning the image was quite difficult for us because we are scaning ramdom images.
- ![image](https://user-images.githubusercontent.com/78479435/126997287-70ee18f3-d05c-47a4-8384-895d0bf7d6ae.png)

## How we overcome the difficulties?
- After the reseach we find that we can only scan image that we stored in our projects assets folder.
- ![snsr_image (1)](https://user-images.githubusercontent.com/78479435/128531786-15747cfa-3c80-4e4e-bf6f-3eaa5bb03cb6.jpg)


## What we tried to do but did not succeed?
- I our scenario, we had to identify the pressure sensor. Unfortunately the android ARCore SDK does not support the 3-D objects recognition. So we were not able to identify the sensor. Instead, we added an image on top of the sensors with the‘Sensor Id’. This is what we used as an augmented image as well.

## What are our future plan regarding the development of project?
- Our future planning  about this project is to move the 3d model when we touching the screen.
