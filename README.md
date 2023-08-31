# Bubble recognition and size measure algorithm

## The code structure 

File folds "assert",  “dataset”, "logs", "mrcn", 

and files "store_data.py" "store_data_test.py" "train.py" "forcast.py" "test.py" "d32.ipynb" "setup.py" "requirments.txt"

The "mrcn" is the network. The "dataset" is the dataset to train or test. "logs" is to store the models in training.  "store_data.py" and "store_data_test.py" are to transform the dataset format(more details are below). "train.py" is to train the model. "forcast.py" is to detection. "test.py" is to output the AP value and PR curve. "d32.ipynb" is to output the Sauter meter diameter， the size distribution of two models and the real values of the test dataset.

## User instructions

### 📖install libaries, and download datasets and models

Fitst download the code package, and install the keras and tensorflow.

The following versions can work.
keras 2.2.4 and its  intastall commmand:
```
pip install keras=2.2.4
```

tensorflow 1.13.1 and its install commmand:
```
pip install tensorflow = 1.13.1
```

The datasets and models download from . The file folder "dataset" is of datasets I have used, and "models" of models which have been trained.

Be care, after download, the files should be put into the package, i.e the file folder "code"

### 📖 Usage Details

### Train

1. When use the dataset I have used, put the data in the "datafile\train" to the file folder "dataset"

   Next, run the command
   ```
   python train.py
   ```
2. When want to use the data prepare by yourself. You need to prepare the data as the format in the files folder "dataset_pic". (More details in Essay)

   Then delete all the data in the filefold dataset" and run the command
   ```
   python store_data.py
   ```
   After the dataset has been prepared, run the command to train the model.
   ```
   python train.py
   ```
After training, the file folder "logs" would store the trained models.

### Test (AP and PR curve)

1. When use the test dataset I have used, put the data in the "datafile\test" to the file folder "dataset"

   Next, run the command
   ```
   python test.py
   ```
2. When want to use the data prepare by yourself. You need to prepare the data as the format in the files folder "dataset_pic_test". (More details in Essay)

   Then delete all the data in the filefold dataset" and run the command
   ```
   python store_data_test.py
   ```
   After the dataset has been prepared, run the command to train the model.
   ```
   python test.py
   ```
After the running, the result of AP values and the PR curve would be outputted.

### Forecast

   In the code, you can set the parameters of the models path and the test image path. Then run the command
   ```
   python forcast.py
   ```
   Then the foracst result would be outputted.


### Sauter meter diameter & size distribution

   In the "d32.ipynb", you can set the parameters of the models path and the test image folder path. Then run the file, it would show the results. (More details in code)

 
 

 
 
