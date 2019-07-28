# Regarding .iloc (delete after conversation done):
- It's an indexer
- I believe he's using .iloc to select column index of 1 (hence the column range of 1:2) which is the "High" columns
- He MIGHT have been able to use the indexer '.loc' which grabs columns BY NAME instead of by index (alot cleaner IMO, but im not 100% sure, ill have to test it)
- standard format/use => DataFrame.iloc[ <rows go here> , <columns go here> ]
  - Select all rows and all columns goes like this: DataFrame.iloc[:,:]
-


# Questions:
- Aaron: do you think there is any way can improve our current format?

# Some exploratory questions for ourselves:
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


- Look into docs for keras.utils.plot_model(). After that: are there any guides on how to interpret it?
- Is there a way to incorporate multiple RNN types on the same level? Are there benefits to mixing RNN cells? In what way?
- In Siddarth's notebook, he imports a Bidirectional TF layer but never 
uses it (only mentions it) -- how is it employed? What's the output? ffDoes it provide extra power?

# Potential interview questions
- What are the effects of decreasing batch_size? Why wouldn't you want 
to have a batch size of 1?
- Explain what happens between epochs in a NN.
