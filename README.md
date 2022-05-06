# Instability-of-Convolutional-Neural-Networks-

In this project I will be explaing how supervised machine learning algorithms of image classification are instable. 
I will use the face mask detector as an example to illustrate instability
I have a generator G that generates images X (masked & unmasked faces) from an unknown probability distribution, 
then the images are labeled by a supervisor S (human) and the pair (X,y) is fed to the learning machine LM. After feeding the machine with enough data, 
the machine constructs a prediction model 𝑦 ̃ = 𝐹_𝑤 (X)  which predicts the label 𝑦 ̃ (masked/unmasked) for any input image X.
Then, I will perturbe the input to show that the prediction model will give a wrong prediction


First of all, what is stability? Stability of a learning algorithm refers to the changes in the output of the system when we change the training dataset. 
A learning algorithm is said to be stable if the learned model doesn’t change much when the training dataset is modified. 
It’s important to notice the word “much” in this definition. 
That’s the part about putting an upper bound. A model changes when you change the training set. 
That’s just how it is! But it shouldn’t change more than a certain threshold regardless of what subset you choose for training. 
If it satisfies this condition, it’s said to be “stable”.

In my project I will be using "DeepFool" a simple and accurate method to fool deep neural networks. I will also provide the option of perturbing the image manually
