# Hands-On Session 1

## Data Preparation
Data preparation (also referred to as “data preprocessing”) is the process of transforming raw data collected so that the data can be fed through to algorithms for training and testing. Often, we do not have the relevant data and are required to perform our own data collection. You can find the respective video collected by the Team in your computer. 

### Task 1: Data Cleaning
Aim: To use FFmpeg to segment videos into 5s clips of people falling
Step | Description | Example/Code |
--- | --- | ---|
Step 1 | Create the output directory based on the video name  | pg_day_front_redteam or pg_day_intercom_redteam |
Step 2 | Open Ubuntu Terminal | - |
Step 3 | Check if your computer have FFmpeg installed <br> Proceed to step 4 if FFmpeg is installed, else go to Step 3.5| ffmpeg -version |
Step 3.5 <br> (Optional)| Update repository <br> Install FFmpeg <br> Confirm installation| sudo apt update && sudo apt upgrade <br> sudo apt install ffmpeg <br> ffmpeg -version |
Step 4 | Segment videos into 5s clips <br><br> See table below for start times for the fall of different subject. | ffmpeg -i _'input directory'_ - ss _start time (hh:mm:ss)_ -t _duration (hh:mm:ss)_ -c:v copy -c:a copy _'output directory with new file name'_ -y|

<u>Starting Time<u>
Video Name | Subject 1 | Subject 2 | Subject 3 | Subject 4 | 
--- | --- | --- | --- | --- |
pg_day_front_redteam | 00:00:12 <br> 00:00:57 <br> 00:01:55 <br> 00:03:00 |  00:00:21 <br> 00:01:05 <br> 00:02:10 <br> 00:03:13 | 00:00:35 <br> 00:01:18 <br> 00:02:25 <br> 00:03:23 | 00:00:45 <br> 00:01:31 <br> 00:02:39 <br> 00:03:43 |
pg_day_intercom_redteam | 00:00:13 <br> 00:00:58 <br> 00:01:56 <br> 00:03:00.25 |  00:00:21 <br> 00:01:05 <br> 00:02:10 <br> 00:03:13 | 00:00:35 <br> 00:01:18 <br> 00:02:25 <br> 00:03:23 | 00:00:45 <br> 00:01:31 <br> 00:02:39 <br> 00:03:43 |

### Task 2: Data Preprocessing
Aim: To use FFmpeg to convert 5s clips into frames
Step | Description | Example/Code |
--- | --- | ---|
Step 1 | Open Ubuntu Terminal | - |
Step 2 | Convert 5s clip into frames | ffmpeg -i _input path_ -vf fps=1 _output%d.png_ |
  
Feel free to play around with the FPS value to see how the images turn out! For the next exercise, we will do 5 frames per second.  

If you prefer a UI to do such editing, you can look up kdenlive 😊 
