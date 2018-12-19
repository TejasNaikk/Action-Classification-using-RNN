# Action-Classification-using-RNN
Using different versions of Recurrent neural networks (RNNs) such as LSTM (Long Short Term Memory) to classify human actions.  

## Dataset details:

Skeleton data that encodes the 3D locations of 25 body joints. (Data is collected by Kinect v2). 
Number of classes : 10 different action classes. 
Training sequences: 4000 
Validation sequences: 800 
Test sequences : 1000 
Each sequence has 15 frames, each frame is a 75-dimension vector (the xyz positions of 25 joints).


## Different experiments to improve the accuracy

I tried different architectures and played with different parameters and tuned it to get the best accuracy. My best architecture is as:

1) Single LSTM layer with input size of 75, hidden size 120 and with dropout of 0.3 2) ReLU Activation Layer 3) Linear Layer 4) ReLU Activation Layer 5) Linear Layer

I tried various optimizers like Adam, SGD and found SGD to be the best. I experimented by increasing and decreasing the learning rate and found e-1 to be the best learning rate.

I experimented with 100, 200 ,300 , 400 and 500 epochs. 300 epochs gave me the best possible accuracy and after 300 the model starts overfitting.
