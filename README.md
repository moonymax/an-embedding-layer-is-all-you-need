# An embedding layer is all you need

This model, with 100% of its parameters being embedding parameters, has an accuracy of 88% on the validation set after 200 - 300 epochs of training (I forgot how many exactly).

The idea behind the model is that every word has a certain probability of being represented in a business, sport or other article. The four embedding dimensions represent the classes in which those words appear. This obviously only works because sufficient semantic value is contained in each token (each token is approximately one word). After each word in the sample is embedded the dimensions of each token only have to be added up and compared to eachother.

An intuitive architecture that seems to work quite well.
