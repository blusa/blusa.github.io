---
layout: post
title:  "Training a new model (thermix)"
date:   2016-05-11 10:37:24 -0300
categories: thermix
---
In this post we will explain with details the whole process for training a new model for the thermix platform.

### 1. Collect videos
__1.1 Data collection tool__

There's an app that makes data collection for thermix easier. Download and install [this thermix branch](https://github.com/gui2/verzus-social/tree/fede-dev-thermal-data-collection).

The app allows the user to record videos normally, and automatically generates and sends 3 videos (uses FLIR One lepton and VGA sensors):
- radiometric infrared
- lava palette infrared
- RGB

__1.2 Data structure__

The script that downloads and updates the database of videos to train in the backend responds to a certain pattern, so you must follow it in order to allow the script to work properly.

Send the videos to a group, where the group name follows this pattern: ```DD-MM-YY_<class_name>```, where ```DD-MM-YY``` stands for 2 digits for day, 2 for month and 2 for year, and ```<class_name>``` the corresponding class name in the backend and frontend.

__1.3 Current class names__

So far, we support this classes:

| ```<class_name>```| ```<link_id>```|
| -------------     |:-------------:|
| __sitting__       |1|
| __standing__      |2|
| __lying__         |3|
| __close up__      |4|
| __outdoor__       |5|
| __indoor__        |6|

If you want to record data for a new class, just create a group following the structure detailed in __1.2 Data Structure__.

### 2. Update backend database manually

### 3. Generate dataset manually

### 4. Train a new model

### 5. Deploy the model
