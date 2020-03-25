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
│  ├─ train.py
│  ├─ utilities
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