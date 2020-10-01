# GitHub101
**Major work**

Preprocessing Audio Dataset :- https://www.kaggle.com/shivam316/preprocessing-part-1 

Class Imbalance & MFCC'S :- https://www.kaggle.com/shivam316/handel-imbalance-creating-spectrogram-part-2

Feature Extraction & Modeling:- https://www.kaggle.com/shivam316/part-3-feature-extraction-modeling-95-acc

**Minor work**

MNIST via Covnets :- https://www.kaggle.com/shivam316/mnist-via-covnets-3-models-all-99-acc




Day 1 -> Processed Audio files.

Day 2 ->  Resolved class imbalance and tried to extract mfcc feature but no luck , there is some error in preprocessing.

Day 3 -> Studied about features in an audio and worked out the error in **Day 1 Preprocessing** , so had to do it all over again
          ( 3hrs of processing) , but in the end got the mfcc feature out, **rise and shine**
          
Day 4 -> Today i got on with dividing the data into **train and validation**, then i started **feature extraction**.
          First i thought that i will try to extract features **one-by-one** and see which one performs **best with 1D-covnet** but different
          features performed well on different audio files,
          So then i thought to use them all by **concatenation**, but the pitfall here was that covnets are designed to find **spatial patterns**
          and the features i had were having a **relation with the audio** but **not** with **each other** so i can not use them together
          finally, i thought of to use them **depth wise**, but i will have to pull out a few tricks to do that,
          So i am going to start with that tomorrow with a fresh mind, **Adios!**.
          
Day 5 -> So what i planned for today was to **concatenate features in depth dimention**, after a few np.mean in different axis i found the combination
          for depth-wise concatenation, made a **basic (not-pretrained) model** to test out the features and got **83% accuracy and 0.75 loss** , with very
          **less overfitting**.
          Thing with Audio feature extraction is that there are many **parameters** to tune for **feature extraction** as well, this was a basic approch
          hoping to improve on this, main take away was that i am in **right direction**.

Day 6 -> Not happy with yesterday's performance of **83%** , i thought that combining features in **dept-dimension** and using **1D-CNN**, is not paying
          respect to **spectral features and patterns** , so i decided to use **Functional API** and different **CNN-Models** for each main feature and then combining 
          them with a **Dense Network**, worked quite well  and gave **accuracy->100% + loss->0.0029** on train data and **accuracy->92% + loss->0.312**
          on validation set, model is clearly **overfitting** , but is much better than **Day 5**, can be improved by regularizaton, **Nyto!**

Day 7 -> Cheat day ;)

Day 8 -> **Regularized** the model and got **97%** acc on **train** data and **95%** on **validation** data, i believe this model can achieve upto **97%-98%** acc
          on **validation** data, if i **remove** the **classes with less samples**, but i want the model to predict **as many diseases as possible**,
          Now i am confused to work MORE on this or not, idk!! :( 
          
Day 9 :- As this spectacular 10 day journey ends tonight, thought of doing a final contribution, i already had a **97%** accuracy artificial
          **neural network** for Digit Recognition Dataset or popularly known as **MNIST** dataset but wanted to get a better score than this and wanted to end this 
          contest with a great feeling, so i made **Three Miniature Versions** of most popular winners of **ImageNet ILSVRC Challenge**, and tuned all 3 to produce
          **99%+** acuuracy
          
          
   **Upvote if you liked this series, comment if you Loved it**
