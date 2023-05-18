<p align="left">
  <img src="https://user-images.githubusercontent.com/125717930/225975240-24b9a8ad-8cc6-4d5f-9a91-1435951b0bd7.png" width="120" alt="Nest Logo" />
</p>

# FaceLivenessDetection-Docker

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


> - [Face Liveness Detection - Android(Basic SDK)](https://github.com/kby-ai/FaceLivenessDetection-Android)
> - [Face Liveness Detection - iOS(Basic SDK)](https://github.com/kby-ai/FaceLivenessDetection-iOS)
> - [Face Recognition - Android(Stdndard SDK)](https://github.com/kby-ai/FaceRecognition-Android)
> - [Face Recognition - iOS(Stdndard SDK)](https://github.com/kby-ai/FaceRecognition-iOS)
> - [Face Attribute - Android(Premium SDK)](https://github.com/kby-ai/FaceAttribute-Android)
> - [Face Attribute - iOS(Premium SDK)](https://github.com/kby-ai/FaceAttribute-iOS)

## Try the API

### Postman
  To test the API, you can use Postman. Here are the endpoints for testing:
  - Test with an image file: Send a POST request to http://18.222.214.79:8080/check_liveness.
  - Test with a base64-encoded image: Send a POST request to http://18.222.214.79:8080/check_liveness_base64.

    You can download the Postman collection to easily access and use these endpoints. [click here](https://github.com/kby-ai/FaceLivenessDetection-Docker/blob/main/postman/kby-ai-live.postman_collection.json)
    
    ![image](https://github.com/kby-ai/FaceLivenessDetection-Docker/assets/125717930/f0f91ad7-220c-4453-a6c5-77eec26d446f)

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
  
## How to run

### 1. System Requirements
  - CPU: 4 cores or more (Recommended: 8 cores)
  - RAM: 4 GB or more (Recommended: 8 GB)
  - HDD: 4 GB or more (Recommended: 8 GB)
  - OS: Ubuntu 20.04 or later
  - Dependency: OpenVINO™ Runtime (Version: 2022.3)

### 2. Setup and test
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
  - Run docker
    ```
    sudo docker run -v ./license.txt:/home/openvino/kby-ai-live/license.txt -p 8080:8080 kby-ai-live
    ```
  - Send us the machine code and replace the license.txt file you received. Then, run the Docker container again.
    
    ![image](https://github.com/kby-ai/FaceLivenessDetection-Docker/assets/125717930/216f1306-a758-4e47-a8fe-159f3c84f53b)
    
    ![image](https://github.com/kby-ai/FaceLivenessDetection-Docker/assets/125717930/2eff3496-abc2-4e70-bee1-4195375f42e6)


  - To test the API, you can use Postman. Here are the endpoints for testing:

    Test with an image file: Send a POST request to http://{xx.xx.xx.xx}:8080/check_liveness.
    
    Test with a base64-encoded image: Send a POST request to http://{xx.xx.xx.xx}:8080/check_liveness_base64.
    
    You can download the Postman collection to easily access and use these endpoints. [click here](https://github.com/kby-ai/FaceLivenessDetection-Docker/blob/main/postman/kby-ai-live.postman_collection.json)
    

    
    



