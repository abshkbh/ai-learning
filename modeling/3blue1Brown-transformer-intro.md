# Large Language Models explained briefly

- [3Blue1Brown - Large Language Models explained briefly](https://www.youtube.com/watch?v=LPZh9BOjkQs)

- Like a magical machine, takes in "words" -> predicts net word over and over again.
- LLM 
    - Large because lots of "parameters"
    - Also trained on entire internet scale of documents
- Words are represented as vectors
- Two stages of training
    - Pretraining - Backprop i.e. loss minimization based on prediction of model vs actual word
    - RLHF - Human rate answers and goes back into training pipeline. This converts it from a predicting machine to assistant. 
- Two key mechanisms
    - Attention - gives context to words "money in bank" vs "river bank" , bank is different.
    - Feedforward - a specific part of the neural network architecture, typically within a Transformer model, where information flows in one direction only, from the input layer through hidden layers to the output layer, without any looping back or feedback mechanisms
