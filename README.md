# tf-gesture-estimation
Gesture esimation /w binary network interaction. Pose Estimation is done via https://github.com/ildoonet/tf-pose-estimation . Then MobileNet /w retrained final layer to estimate gesture

Early stage Development.

Installation dependencies:

Python3 

tf-gpu 1.13.0rc2

opencv3

slim

slidingwindows

post-processing for Part-Affinity Fields Map implemented in C++ & Swig
```
$ cd tf_pose/pafprocess/
$ swig -python -c++ pafprocess.i 
$ python setup.py build_ext --inplace
```

# Usage:

```
$ python run_image.py --image=/tf-gesture-estimation/2.jpeg
```

# Retrain:

```
$ python scripts/retrain.py --model_dir=tf_files/retrained_graph.pb --output_label=tf_files/retrained_labels.txt --image_dir=Custom_Gesture_Dataset --output_graph=tf_files/output_graph.pb
```


ToDo:

Update to tf-gpu 2.1.0

Reevaluate Dataset (Stop Gesture)
