# map-gen
Procedural map generation with AnsProlog and answer set programming.

## NOTE: SOME ASSETS WILL NOT LOAD PROPERLY WHEN VIEWED ON GitHub, PLEASE OPEN IT IN GOOGLE COLAB WITH CLINGO IMPORTED.
* https://colab.research.google.com/drive/1T9DikhvhDm2Hv9MH4wIyTceEgj3KiFWk?usp=sharing

## Summary
The program infers facts and state of the world given constraints. Thus it makes choices about how and where to place assets to eventually form a full map. 

* For example, a house will have rules where no two doors should be constructed and placed right next to one another. 
* This program is using Answer Set programming which is a declarative programming paradigm in contrast to the more widely used imperative programming paradigm. Whereas the latter is clearly coded and defined to tell the program what to do, in declarative programming the computer generates a desired result given a prescribed solution or constraints - similar to how SQL works..


## Layer Information
Model: "sequential_20"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
zero_padding2d_63 (ZeroPaddi (None, 50, 50, 1)         0         
_________________________________________________________________
conv2d_63 (Conv2D)           (None, 48, 48, 64)        640       
_________________________________________________________________
max_pooling2d_59 (MaxPooling (None, 24, 24, 64)        0         
_________________________________________________________________
dropout_37 (Dropout)         (None, 24, 24, 64)        0         
_________________________________________________________________
zero_padding2d_64 (ZeroPaddi (None, 26, 26, 64)        0         
_________________________________________________________________
conv2d_64 (Conv2D)           (None, 22, 22, 128)       204928    
_________________________________________________________________
max_pooling2d_60 (MaxPooling (None, 11, 11, 128)       0         
_________________________________________________________________
dropout_38 (Dropout)         (None, 11, 11, 128)       0         
_________________________________________________________________
zero_padding2d_65 (ZeroPaddi (None, 13, 13, 128)       0         
_________________________________________________________________
conv2d_65 (Conv2D)           (None, 11, 11, 512)       590336    
_________________________________________________________________
max_pooling2d_61 (MaxPooling (None, 5, 5, 512)         0         
_________________________________________________________________
dropout_39 (Dropout)         (None, 5, 5, 512)         0         
_________________________________________________________________
zero_padding2d_66 (ZeroPaddi (None, 7, 7, 512)         0         
_________________________________________________________________
conv2d_66 (Conv2D)           (None, 5, 5, 512)         2359808   
_________________________________________________________________
max_pooling2d_62 (MaxPooling (None, 2, 2, 512)         0         
_________________________________________________________________
dropout_40 (Dropout)         (None, 2, 2, 512)         0         
_________________________________________________________________
flatten_22 (Flatten)         (None, 2048)              0         
_________________________________________________________________
dense_44 (Dense)             (None, 256)               524544    
_________________________________________________________________
dropout_41 (Dropout)         (None, 256)               0         
_________________________________________________________________
flatten_23 (Flatten)         (None, 256)               0         
_________________________________________________________________
dense_45 (Dense)             (None, 512)               131584    
_________________________________________________________________
dropout_42 (Dropout)         (None, 512)               0         
_________________________________________________________________
dense_46 (Dense)             (None, 3)                 1539      
=================================================================
Total params: 3,813,379
Trainable params: 3,813,379
Non-trainable params: 0

## Training and Validation History
![datahistory](https://i.imgur.com/yXg84Yp.png?raw=true)
