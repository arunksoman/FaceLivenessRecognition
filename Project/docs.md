1. Create folder named FaceLiveness Recognition any drive you want.
2. Open VSCode. Then go to File $\rarr$ Open folder $\rarr$ navigate to your folder $\rarr$ open folder
3. Create folder structure (The folder structure can be change time to time as per requirements.) as I given below except <span style="color: green">**venv**</span>

```
FaceLivenessRecognition
├─ Project
│  ├─ configurations.py
│  ├─ ConvNet
│  │  ├─ convnet.py
│  │  └─ __init__.py
│  ├─ Dataset
│  │  ├─ Fake
│  │  └─ Real
│  ├─ dataset_preparation.py
│  ├─ docs.md
│  ├─ readme.md
│  ├─ recognize.py
│  ├─ SSDModels
│  │  ├─ deploy.prototxt
│  │  └─ res10_300x300_ssd_iter_140000.caffemodel
│  ├─ train.py
│  ├─ utilities
│  │  ├─ convenience.py
│  │  ├─ paths.py
│  │  ├─ video_utilities
│  │  │  ├─ filestream.py
│  │  │  ├─ streamfromcam.py
│  │  │  ├─ videostream.py
│  │  │  └─ __init__.py
│  │  └─ __init__.py
│  ├─ Video
│  └─ Videos
├─ readme.md
├─ requirements.txt
└─ venv

```
4. Go to terminal $\rarr$ New terminal on your vs code. it will open up an integrated terminal on the bottom.
5. Install virtual environment using following command on integrated terminal. It will take upto 2 or 3 minutes  to execute so wait until that. After executing this command you can see a <span style="color: green">**venv**</span> folder:
 
```python -m venv venv```

6. Then activate your venv using following command:

```.\venv\Scripts\activate```

7. Install necessary python index packages using following command:

```pip install -r requirements.txt```

8. in order to check everything works perfectly. Type **python** on your integrated terminal. It will show python interpreter. Then type following lines and hit enter after each line to execute those lines.

```python
import tensorflow as tf
import keras
```

If these things not throwing any error our virtual environment is ready for doing this project. If this throws some error like <span style="color: red">**DLL file missing**</span> please contact me.

## Dataset Preparation

1. Run **capture_video.py** file. After running this file you can see your face on a window. You have to move your face back and forth as well as change your angle of face infront of camera. it will save your video on the folder named **Videos in avi format**.
2. Copy that video to your mobile phone. Play that video before your camera while running same program(**capture_video.py**). Do not forgot to <span style="color:red">**write/ notedown names of those files.**</span>
3. Now the video played from your phone is a kind of fake image since your live appearance is not before your camera. So Now we have to create our dataset using these steps.
4. For more accuracy you can use different camera sensors (say camera of your mobile phone) in order to capture video. Then you have to store those videos on your folder Videos(notedown this video as real). Then Play this video on phone and capture that video using **capture_video.py** script. 
5. Another ways to improve accuracy is you have to choose diffrent lighting conditions for taking those videos as well as people with diffrent skin tones. We are using a shallow convolutional neural network, so our each class(Real/ Fake) can have upto 8k-10k images.