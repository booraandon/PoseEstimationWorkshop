# Data Annotation

Next step after cleaning up the raw data is to annotate it. Data annotation is the process of labeling individual elements of training data to help algorithms understand what is in the image. As we are doing pose estimation, we will be following COCO format and annotation the keypoints on the images. 
<code> </code>
## Task 1: Install and Set-up COCO-Annotator
Step No.| Description | Example/Code |
--- | --- | ---|
Step 1 | Open Ubuntu Terminal | - |
Step 2 | Change current directory to “Documents” | <code> cd Documents </code> |
Step 3 | Clone the repo COCO-Annotator by jsbroks | <code> git clone https://github.com/jsbroks/coco-annotator </code> |
Step 4 | heck if your computer has Docker and Docker-compose installed | <code> sudo docker -v </code> and <code> sudo docker-compose -v</code> |
Step 5 | Change current directory to cloned directory | <code> cd coco-annotator </code> |
Step 6 | Start the application to pull and download all images | <code> sudo docker-compose up </code>

## Task 2: Creation of Labels
Step No.| Description |
--- | --- |
Step 1 | Access the annotator by going to “localhost:5000”  |
Step 2 | Create an account and login to the annotator |
Step 3 | Select “Create” in the “Categories” page | 
Step 4 | Fill up the Name and Supercategory accordingly. <br><br> <br>Name: person <br>Supercategory: person  |
Step 5 | Add Labels as per the table in the next page |

Labels | Connects to |
--- | --- |
Nose | Eye_right <br> Eye_left |
Eye_left | Nose <br> Ear_left <br> Eye_right |
Eye_Right | Nose <br> Ear_right <br> Eye_left |
Ear_left | Eye_left <br> Shoulder_left | 
Ear_right | Eye_Right <br> Shoulder_right | 
Shoulder_left | Ear_left <br> Shoulder_right <br> Elbow_left <br> Hip_left | 
Shoulder_right | Ear_right <br> Shoulder_left <br> Elbow_right <br> Hip_right |
Elbow_left | Shoulder_left <br> Wrist_left | 
Elbow_right | Shoulder_right <br> Wrist_right | 
Wrist_left | Elbow_left |
Wrist_right | Elbow_right | 
Hip_left | Shoulder_left <br> Hip_right <br> Knee_left | 
Hip_right | Shoulder_right <br> Hip_left <br> Knee_right | 
Knee_left | Hip_left <br> Ankle_left | 
Knee_right | Hip_right <br> Ankle_right | 
Ankle_left | Knee_left | 
Ankle_right | Knee_right |

## Task 3: Creating and Uploading of Dataset
Step No.| Description |
--- | --- |
Step 1 | Access the annotator by going to “localhost:5000”  |
Step 2 | Create an account and login to the annotator |
Step 3 | Select “Create” in the “Datasets” page | 
Step 4 | Fill up the Name (keypoint_demo) and select person for the category |
Step 5 | Navigate to the dataset folder in the file explorer. <br><br> (./coco-annotator/datasets/keypoint_demo) |
Step 6 | Copy and paste all the images extracted from the previous exercise into the keypoint_demo folder. <br> <br> <br> If not allowed, please right click the datasets folder and select open in terminal. Enter <code> sudo chmod -rwx keypoint_demo </code> and enter the account password.  to the dataset folder in the file explorer. (./coco-annotator/datasets/keypoint_demo) |
Step 7 | Refresh the browser and you should see the images uploaded |

## Task 4: Annotating Dataset
Step No.| Description |
--- | --- |
Step 1 | Access the annotator by going to “localhost:5000”  |
Step 2 | Create an account and login to the annotator |
Step 3 | Select “keypoint_demo” in the “Datasets” page  | 
Step 4 | Select the first image  |
Step 5 | Click the “+” icon on the right side of the page and you will realize that a new set of tools will be enabled on the left side of the page.  |
Step 6 | Select keypoint tool and annotate accordingly |
Step 7 | Click “Save” on the left side and proceed to the next image |
