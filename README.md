In this Notebook, we try and see how accurately different models fit on the training and testing datasets.
We use ECG signals, and try to predict whether the signal is Abnormal or Normal.

_The dataset can be downloaded from the following link: https://www.kaggle.com/datasets/shayanfazeli/heartbeat_


# Models
## LSTM (Long Short-Term Memory):
LSTMs are a type of recurrent neural network (RNN) designed to address the vanishing gradient problem of traditional RNNs by incorporating memory cells that can maintain information in memory for long periods. They are particularly useful for tasks involving sequences, such as time series prediction, natural language processing, and speech recognition, where the dependencies between elements can be extended over many time steps.

## BiLSTM (Bidirectional Long Short-Term Memory)
BiLSTMs extend the traditional LSTM architecture by processing data in both forward and backward directions with two separate hidden layers, which are then fed forwards to the same output layer. This approach allows them to capture context from both past and future data points, making them particularly effective for complex sequence prediction tasks where understanding context from both directions is beneficial. BiLSTMs are widely used in natural language processing tasks like sentiment analysis and named entity recognition.

## Transformer
Transformers represent a significant shift away from recurrent models to architectures that rely entirely on self-attention mechanisms to compute representations of their input and output without using sequence-aligned RNNs or convolution. Introduced in the paper "Attention is All You Need" by Vaswani et al., transformers allow for much more parallelization than RNNs and have led to breakthroughs in a variety of NLP tasks. Their architecture enables them to learn contextual relationships between words in a text, irrespective of their positions in the sequence, making them particularly powerful for machine translation, text summarization, and as the backbone of models like GPT and BERT.

## CNN (Convolutional Neural Network):
CNNs are primarily used in image processing but have also found use in other data-rich environments (e.g., audio, video). They are characterized by their hierarchical structure that helps in detecting patterns with varying degrees of abstraction, which are learned through convolutions—operations that can capture spatial hierarchies in data. CNNs excel at tasks like image classification, object detection, and image generation.


#### NOTE:
Before drawing any conclusions try to increase the number of epochs for training. Other models like RNN or GRN are also good for time-series predictions.



# ECG SIGNALS 
 
### 1. CLASS 'N' (NORMAL): 
**Characteristics:** The ECG of a normal heartbeat typically shows a regular rhythm with 
consistent intervals. The P wave, QRS complex, and T wave follow a regular pattern.  
**Comparison Basis:** This will be our baseline for comparison.

 
### 2. CLASS 'S' (SUPRAVENTRICULAR ECTOPIC BEATS): 
**Characteristics:** These beats originate from the atria, above the ventricles. The P wave 
might be altered or not visible. The QRS complex is usually narrow as the ventricles are 
depolarized normally. 
**Comparison Basis:** Compared to 'N', the main difference is often seen in the P wave's 
appearance or timing.


 
### 3. CLASS 'V' (VENTRICULAR ECTOPIC BEATS): 
**Characteristics:** Ventricular ectopic beats are characterized by a premature and wide 
QRS complex, as the ventricles are not depolarized through the normal pathway. 
**Comparison Basis:** The QRS complex in 'V' is noticeably wider and earlier than in 'N'. There's 
often an absence of a preceding P wave.

 
### 4. CLASS 'F' (FUSION BEATS): 
**Characteristics:** Fusion beats are a combination of normal and ectopic beats. The 
waveform is a fusion of a normal QRS complex and an ectopic ventricular complex. 
**Comparison Basis:** The QRS complex in 'F' appears to be a blend of normal and abnormal 
depolarization, making it different in shape from the 'N' class but not as wide as in pure 
ventricular ectopic beats. 

### 5. CLASS 'Q' (UNKNOWN BEAT): 
**Characteristics:** These are beats that do not fit into the typical categories. They may 
have various irregularities. 
**Comparison Basis:** The waveform can vary significantly, showing atypical patterns that do not 
conform to the typical 'N' morphology. 
The 'Q' class in an ECG dataset, labeled as "Unknown Beat," represents beats that do 
not clearly fit into the standard categories of cardiac rhythms or patterns. 






















