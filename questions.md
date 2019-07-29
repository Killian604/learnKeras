# Food for thought:
- We should consider a method by which to classify what day of the week 
trade is occuring. I say this because there is a BIG difference between 
comparing Monday trade to Tuesday trade and comparing Friday trade to 
the following Monday trade (news over the weekend can make a stock very 
hot/cold). On the other hand, we could assume this problem washes out 
because we're looking at daily ticks and not hourly. Thoughts?

# LTSM VIDEO:
- https://www.youtube.com/watch?v=8HyCNIVRbSU


# Questions:
- Aaron: do you think there is any way can improve our current format?
  - K: Format in terms of?

# Some general exploratory questions for ourselves:
- Why use vanilla RNNs if they suffer from the vanishing gradient problem?
  - Are there instances where the vanishing gradient is useful?
- Are there things that GRUs can do that LTSMs can't do?
- At what point do performance b/w LTSMs and GRUs diverge?


- What is the optimal dropout per layer? is there a best amountt?
- Does dropout benefit a RNN system w/ time series data because it could 
be dropping important time frames?
- What are the effects of shuffling NN input during training for time series data (model.fit(..,shuffle=True))?
Does the data trained need to be done in order?
- What are the effects of increasing epochs at the same time as increasing batch size? 
- What are the effects of decreasing epochs at the same time as decreasing batch size?
- How exactly can you input multiple features into an RNN at a single time? what's the input array shape?
  - (AFAIK, the first dimension is the input sets themselves...so are the features added in the 2nd or 3rd dim?)
- Is there a "best" optimizer for RNNs?

- Look into docs for keras.utils.plot_model(). After that: are there any guides on how to interpret it?
- Is there a way to incorporate multiple RNN types on the same level? Are there benefits to mixing RNN cells? In what way?
- Q: In Siddarth's notebook, he imports a Bidirectional TF layer but never 
uses it (only mentions it) -- how is it employed? What's the output? ffDoes it provide extra power?
  - A: https://www.quora.com/When-should-one-use-bidirectional-LSTM-as-opposed-to-normal-LSTM
  - A: It appears as though bidirectional LTSMs don't just use past data but also utilize future data to produce outcomes.
Think of a fill-in-the-blank: "I am __ student" -- a bidirectional LTSM would have access to the word 'student', and so 
could fill in the blank with the word 'a'. Appears to be very useful for NLP, not so much for stock prediction.

# Potential interview questions
- What are the effects of decreasing batch_size? Why wouldn't you want 
to have a batch size of 1?
- Explain what happens between epochs in a NN.
