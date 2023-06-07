# Stack Hourglass Pose Estimation

## Task 1: Clone Stacked Hourglass repository

Step No | Description | Example/Code |
--- | --- | --- |
Step 1 | Open Ubuntu Terminal | - |
Step 2 | Change current directory and make GitHub directory | <code> cd Documents </code> <br> <code> mkdir <GitHub> <code> cd GitHub </code> |
Step 3 | Clone Stacked Hourglass keypoint detection repo | <code> git clone https://github.com/david8862/tf-keras-stacked-hourglass-keypoint-detection.git </code> |
Step 4 | Move "copy requirements_new.txt", "multi_person_demo_stu.py" and "models" folder into the Stacked Hourglass folder| -|
Step 5 | Create "output" folder | - |

## Task 2 : Create and Set-up Environment
Step No | Description | Example/Code |
--- | --- | --- |
Step 1 | Open Ubuntu Terminal | - |
Step 2 | Create Environment | <code> conda create -n test python=3.8 </code> |
  Step 3 | Activate Environtment | <code> conda activate test </code> |
Step 4 | Install requirements | <code> pip install -r requirements_new.txt </code> |

## Task 3: Have Fun!
Step No | Description | Example/Code |
--- | --- | --- |
Step 1 | Open Ubuntu Terminal | - |
Step 2 | Experiment with it | <code>python3 multi_person_demo_stu.py --num_stacks=2 --weights_path=./models/hg_s2_256_256_coco.h5 --classes_path=configs/coco_classes.txt --skeleton_path=configs/coco_skeleton.txt --input_folder=_example_ --output=output </code> |
