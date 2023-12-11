<p align="center">
  <a href="https://play.google.com/store/apps/dev?id=7086930298279250852" target="_blank">
    <img alt="" src="https://github-production-user-asset-6210df.s3.amazonaws.com/125717930/246971879-8ce757c3-90dc-438d-807f-3f3d29ddc064.png" width=500/>
  </a>  
</p>

👏 Product List

https://github.com/kby-ai/Product

👏  We have published the Face Liveness Detection, Face Recognition SDK and ID Card Recognition SDK for the server.

  - [FaceLivenessDetection-Docker](https://github.com/kby-ai/FaceLivenessDetection-Docker)

  - [FaceRecognition-Docker](https://github.com/kby-ai/FaceRecognition-Docker)

  - [IDCardRecognition-Docker](https://github.com/kby-ai/IDCardRecognition-Docker)

# FaceLivenessDetection-Docker
## Overview

This project demonstrates an advanced face liveness detection technology implemented via a Dockerized Flask API.

It includes features that allow for testing face liveness detection using both image files and base64-encoded images.

> The demo is integrated with KBY-AI's Face Liveness Detection Server SDK.

> We can customize the SDK to align with your specific requirements.

  | Face Liveness Detection      | Face Recognition |
  |------------------|------------------|
  | Face Detection        | Face Detection    |
  | Face Liveness Detection        | Face Recognition    |
  | Pose Estimation        | Pose Estimation    |
  | 68 points Face Landmark Detection        | 68 points Face Landmark Detection    |
  | Face Quality Calculation        | Face Occlusion Detection        |
  | Face Occlusion Detection        | Face Occlusion Detection        |
  | Eye Closure Detection        | Eye Closure Detection       |
  | Mouth Opening Check        | Mouth Opening Check        |

> For other solutions, please explore the following:
>
> [Face Liveness Detection - Android(Basic SDK)](https://github.com/kby-ai/FaceLivenessDetection-Android)
> 
> [Face Liveness Detection - iOS(Basic SDK)](https://github.com/kby-ai/FaceLivenessDetection-iOS)
> 
> [Face Recognition - Android(Standard SDK)](https://github.com/kby-ai/FaceRecognition-Android)
> 
> [Face Recognition - iOS(Standard SDK)](https://github.com/kby-ai/FaceRecognition-iOS)
> 
> [Face Recognition - Flutter(Standard SDK)](https://github.com/kby-ai/FaceRecognition-Flutter)
> 
> [Face Recognition - React-Native(Standard SDK)](https://github.com/kby-ai/FaceRecognition-React-Native)
>
> [Face Attribute - Android(Premium SDK)](https://github.com/kby-ai/FaceAttribute-Android)
> 
> [Face Attribute - iOS(Premium SDK)](https://github.com/kby-ai/FaceAttribute-iOS)

## Try the API
### Online Demo
  You can test the SDK using images from the following URL:
  https://web.kby-ai.com
  
  ![image](https://github.com/kby-ai/FaceLivenessDetection-Docker/assets/125717930/4fd2c1ca-3552-4c6e-b8c2-4a12d7c92ca6)

### Postman
  To test the API, you can use Postman. Here are the endpoints for testing:
  - Test with an image file: Send a POST request to http://18.221.33.238:8080/check_liveness.
  - Test with a base64-encoded image: Send a POST request to http://18.221.33.238:8080/check_liveness_base64.

    You can download the Postman collection to easily access and use these endpoints. [click here](https://github.com/kby-ai/FaceLivenessDetection-Docker/blob/main/postman/kby-ai-live.postman_collection.json)
    
    ![image](https://github.com/kby-ai/FaceLivenessDetection-Docker/assets/125717930/b24b1145-08af-46ca-8ffa-65aa020749b4)


## SDK License

This project uses KBY-AI's Face Liveness Detection Server SDK, which requires a license per machine.

- The code below shows how to use the license: https://github.com/kby-ai/FaceLivenessDetection-Docker/blob/6aafd08dba5093600008ec66df39f362e53f9bb8/app.py#L36-L48

- In order to request the license, please provide us with the machine code obtained from the "getMachineCode" function.

  Please contact us:
  ```
  Email: contact@kby-ai.com

  Telegram: @kbyai

  WhatsApp: +19092802609

  Skype: live:.cid.66e2522354b1049b

  Facebook: https://www.facebook.com/KBYAI
  
## How to run

### 1. System Requirements
  - CPU: 2 cores or more (Recommended: 8 cores)
  - RAM: 4 GB or more (Recommended: 8 GB)
  - HDD: 4 GB or more (Recommended: 8 GB)
  - OS: Ubuntu 20.04 or later
  - Dependency: OpenVINO™ Runtime (Version: 2022.3)

### 2. Setup and Test
  - Clone the project:
    ```
    git clone https://github.com/kby-ai/FaceLivenessDetection-Docker.git
    ```
  - Download the model from Google Drive: [click here](https://drive.google.com/file/d/1bYl0p5uHXuTQoETdbRwYLpd3huOqA3wY/view?usp=share_link)
    ```
    cd FaceLivenessDetection-Docker
    
    wget --load-cookies /tmp/cookies.txt "https://docs.google.com/uc?export=download&confirm=$(wget --quiet --save-cookies /tmp/cookies.txt --keep-session-cookies --no-check-certificate 'https://docs.google.com/uc?export=download&id=1bYl0p5uHXuTQoETdbRwYLpd3huOqA3wY' -O- | sed -rn 's/.*confirm=([0-9A-Za-z_]+).*/\1\n/p')&id=1bYl0p5uHXuTQoETdbRwYLpd3huOqA3wY" -O data.zip && rm -rf /tmp/cookies.txt
    
    unzip data.zip
    ```
  - Build the Docker image:
    ```
    sudo docker build --pull --rm -f Dockerfile -t kby-ai-live:latest .
    ```
  - Run the Docker container:
    ```
    sudo docker run -v ./license.txt:/home/openvino/kby-ai-live/license.txt -p 8080:8080 kby-ai-live
    ```
  - Send us the machine code and then we will give you a license key.
    
    After that, update the license.txt file by overwriting the license key that you received. Then, run the Docker container again.
    
    ![image](https://github.com/kby-ai/FaceLivenessDetection-Docker/assets/125717930/216f1306-a758-4e47-a8fe-159f3c84f53b)
    
    ![image](https://github.com/kby-ai/FaceLivenessDetection-Docker/assets/125717930/2eff3496-abc2-4e70-bee1-4195375f42e6)


  - To test the API, you can use Postman. Here are the endpoints for testing:

    Test with an image file: Send a POST request to http://{xx.xx.xx.xx}:8080/check_liveness.
    
    Test with a base64-encoded image: Send a POST request to http://{xx.xx.xx.xx}:8080/check_liveness_base64.
    
    You can download the Postman collection to easily access and use these endpoints. [click here](https://github.com/kby-ai/FaceLivenessDetection-Docker/blob/main/postman/kby-ai-live.postman_collection.json)   

### 3. Execute the Gradio demo
  - Setup Gradio
    Ensure that you have the necessary dependencies installed. 
    
    Gradio requires Python 3.6 or above. 
    
    You can install Gradio using pip by running the following command:
    ```
    pip install gradio
    ```
  - Run the demo
    Run it using the following command:
    ```
    cd gradio
    python demo.py
    ```
  - You can test within the following URL:    
    http://127.0.0.1:9000    
## About SDK

### 1. Initializing the SDK

- Step One

  First, obtain the machine code for activation and request a license based on the machine code.
  ```
  machineCode = getMachineCode()
  print("machineCode: ", machineCode.decode('utf-8'))
  ```
  
- Step Two

  Next, activate the SDK using the received license.
  ```
  setActivation(license.encode('utf-8'))
  ```  
  If activation is successful, the return value will be SDK_SUCCESS. Otherwise, an error value will be returned.

- Step Three

  After activation, call the initialization function of the SDK.
  ```
  initSDK("data".encode('utf-8'))
  ```
  The first parameter is the path to the model.

  If initialization is successful, the return value will be SDK_SUCCESS. Otherwise, an error value will be returned.

### 2. Enum and Structure
  - SDK_ERROR
  
    This enumeration represents the return value of the 'initSDK' and 'setActivation' functions.

    | Feature| Value | Name |
    |------------------|------------------|------------------|
    | Successful activation or initialization        | 0    | SDK_SUCCESS |
    | License key error        | -1    | SDK_LICENSE_KEY_ERROR |
    | AppID error (Not used in Server SDK)       | -2    | SDK_LICENSE_APPID_ERROR |
    | License expiration        | -3    | SDK_LICENSE_EXPIRED |
    | Not activated      | -4    | SDK_NO_ACTIVATED |
    | Failed to initialize SDK       | -5    | SDK_INIT_ERROR |

- FaceBox
  
    This structure represents the output of the face detection function.

    | Feature| Type | Name |
    |------------------|------------------|------------------|
    | Face rectangle        | int    | x1, y1, x2, y2 |
    | Liveness score (0 ~ 1)        | float    | liveness |
    | Face angles (-45 ~ 45)        | float    | yaw, roll, pitch |
    | Face quality (0 ~ 1)        | float    | face_quality |
    | Face luminance (0 ~ 255)       | float    | face_luminance |
    | Eye distance (pixels)       | float    | eye_dist |
    | Eye closure (0 ~ 1)       | float    | left_eye_closed, right_eye_closed |
    | Face occlusion (0 ~ 1)       | float    | face_occlusion |
    | Mouth opening (0 ~ 1)       | float    | mouth_opened |
    | 68 points facial landmark        | float[]    | landmarks_68 |
  
    > 68 points facial landmark
    
    <img src="https://user-images.githubusercontent.com/125717930/235560305-ee1b6a39-5dab-4832-a214-732c379cabfd.png" width=500/>

### 3. APIs
  - Face Detection
  
    The Face SDK provides a single API for detecting faces, performing liveness detection, determining face orientation (yaw, roll, pitch), assessing face quality, detecting facial occlusion, eye closure, mouth opening, and identifying facial landmarks.
    
    The function can be used as follows:

    ```
    faceBoxes = (FaceBox * maxFaceCount)()
    faceCount = faceDetection(image_np, image_np.shape[1], image_np.shape[0], faceBoxes, maxFaceCount)
    ```
    
    This function requires 5 parameters.
    * The first parameter: the byte array of the RGB image buffer.
    * The second parameter: the width of the image.
    * The third parameter: the height of the image.
    * The fourth parameter: the 'FaceBox' array allocated with 'maxFaceCount' for storing the detected faces.
    * The fifth parameter: the count allocated for the maximum 'FaceBox' objects.

    The function returns the count of the detected face.

### 4. Thresholds
  The default thresholds are as the following below:
  https://github.com/kby-ai/FaceLivenessDetection-Docker/blob/1e89ec05f49d55807164a92d19abc5149054ce2a/app.py#L17-L29
