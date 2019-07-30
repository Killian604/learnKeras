# Questions:
- Aaron: do you think there is any way can improve our current format?
  - K: Format in terms of?

# Some exploratory questions for ourselves:
- Why use vanilla RNNs if they suffer from the vanishing gradient problem?
  - Are there instances where the vanishing gradient is useful?
- Are there things that GRUs can do that LTSMs can't do?
- At what point do performance b/w LTSMs and GRUs diverge?
- In Siddarth's notebook, he imports a Bidirectional TF layer but never 
uses it (only mentions it) -- how is it employed? What's the output? ffDoes it provide extra power?
- What is the optimal dropout per layer? is there a best amt?
- Does dropout benefit a RNN system w/ time series data because it could 
be dropping important time frames?
- What are the effects of shuffling NN input during training for time series data? Does the data trained need to be done in order?
- What are the effects of increasing epochs at the same time as 
increasing batch size?
- How to get multi-dim inputs into an RNN? what's the shape?
- Look into docs for keras.utils.plot_model(). After, are there any guides on how to interpret it?
- Is there a way to incorporate multiple RNN types on the same level? Are there benefits to mixing RNN cells? In what way?

# Potential interview questions
- What are the effects of decreasing batch_size? Why wouldn't you want 
to have a batch size of 1?
- explain what happens b/w epochs in a NN
