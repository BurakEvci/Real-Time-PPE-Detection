# Real-Time PPE Detection and Safety Compliance System
This project is a real-time computer vision application that detects and tracks personal protective equipment (PPE) compliance using a camera feed or a video file. It identifies various PPE items such as hardhats, masks, and safety vests, and highlights any missing equipment for enhanced safety monitoring.


![1](https://github.com/user-attachments/assets/e672f2b8-9189-4420-a819-bb62c8fcc2f6)
![2](https://github.com/user-attachments/assets/fee34aec-fb19-472f-95ea-2607719188d9)
![3](https://github.com/user-attachments/assets/7c6d8b48-ce60-4945-b424-d61c92024da2)



## 1. Real-Time Video Processing with OpenCV
The application works with both a live camera feed (cv2.VideoCapture(0)) and pre-recorded video files (e.g., ppe-1.mp4).

The frames are captured and processed in real-time, making it suitable for immediate safety checks on job sites.
## 2. Custom PPE Detection Model (ppe.pt)
The model used in this application (ppe.pt) was trained using a custom dataset specifically designed for PPE detection.

The dataset includes images annotated with various PPE items such as hardhats, masks, safety vests, and instances of non-compliance (e.g., NO-Hardhat, NO-Mask).

The YOLO architecture was used for training, allowing the model to quickly and accurately identify PPE compliance in diverse environments.
## 3. Object Detection and Classification
The YOLO model (ppe.pt) detects various PPE items and classifies them into categories such as compliant (e.g., Hardhat, Mask) and non-compliant (e.g., NO-Hardhat, NO-Mask).

Detected objects are labeled with their class names and confidence scores.
## 4. Classification and Color Coding
The detected PPE items are color-coded based on compliance:

Red ((0,0,255)): Indicates missing safety gear (NO-Hardhat, NO-Mask, NO-Safety Vest).

Green ((0,255,0)): Indicates compliant safety gear (Hardhat, Mask, Safety Vest).

Blue ((255,0,0)): Used for other detected objects such as machinery or vehicles.
## 5. Displaying Information on the Image
Bounding boxes and labels with confidence scores are drawn around detected items, providing clear visual feedback on PPE compliance status.

Real-time processing ensures that safety violations are immediately visible to supervisors or monitoring systems.
## Use Case
This project is designed for real-time safety compliance monitoring on construction sites, industrial facilities, or any environment where PPE is mandatory. 

It helps ensure that all personnel are following safety protocols, thereby reducing the risk of workplace accidents.

Note: I do not own the copyrights of this project.(youtube @murtazasworkshop) It is for learning purposes only.
