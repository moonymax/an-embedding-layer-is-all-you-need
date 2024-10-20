# Embeddings are all you need

For this simple text classification dataset we can assume that the tokenizer will approximately split all words into individual tokens since it has a vocabulary of ~30k. We can then assume that each word has a businessieness, sportyness and so on dimension, so we'll give it 4 embedding dimensions because we have 4 classes. Now if we want to know the sportyness of a whole article we can just add all the token embeddings. The end result is that inorder to, for example, measure the businessieness of an article we just have to see how businessy the words in the article are relative to the other properties.

The result of those sheinanegans is that we have a model with 100% of its parameters being embedding parameters with an 88% accuracy on the validation set after 200 - 300 epochs of training (I forgot how many exactly).
