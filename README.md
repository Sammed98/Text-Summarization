# Text-Summarization
Automatic Text Summarization 

Language is in many ways a seat of intelligence. It is the original communication protocol that we invented to describe all the incredibly complex processes happening in our surrounding.There is always an increasing amount of articles, links and videos to choose from. As, the data grows the importance of semantic density does as well. How can we say the most important things in the shortest amount of time. This is where Text Summarization comes to play.

There are two types of Summarization

1. Extractive Summarization
2. Abstractive Summarization

### Extractive Summarization
In Extractive summarization we select an existing subset of words or numbers from some data to create a summary. 

### Abstractive Summarization
In Abstractive Summarization, the model learns an internal language representation to generate more human like summaries, paraphrasing the intent of the original text.

As the definition itself suggest Abstractive Summarization is better than Extractive.

Consider the brain. When we summarise our brain builds an internal semantic representation of what we have jst read and from that we can generate a summary. This is the Abstractive methods which can be build using Deep Learning.

## Implemented Code:
In this repository I have implemented 2 methods of Extractive Summarization.

1. Frequency based Text Summarization - Frequency_Based_TextSummarization.ipynb
2. PageRank based Text Summarizaton - PageRank_Based_TextSummarization.ipynb

### Common work to be done in both the models:
Preprocessing of data. This includes removing the special characters,extra blank lines, new line characters etc. Also write functions for removing the stop words from the data, word and sentence tokenise them.

### Frequency based Text Summaization
1. Preprocess the data
2. Iterate through all the words, find each words frequency and create a dictionary with this data.
3. Now normalise the values of the dictionary to get the scores of each word.
4. Now iterate through the data sentence wise and assign a score to a sentence as a sum of the scores of words that sentence has.
5. After iterating through all the sentence, we get scored sentences of the given data.
6. Sort them and take the top few sentences which are the most important sentences of the given data.

### PageRank based Text Summarization
Given a set of nodes and the relationships between these nodes, PageRank provides us with a means of identifying which amongst these nodes is the most prestigious.
1. Preprocess the given data
2. Iterate through the sentences of the data set and find the similarity between all pairs of sentences. 
3. Maintain an Adjacency matrix to store corresponding values. 
4. Use this similarity matrix and pass through the Page Rank algorithm. This will tell us the best model for varying puppies.
5. The output of this Page Rank contains us a standard, hanked according to their importance.
6. Since we got to know which sentences are more important. Now a few of the top sentences will become the summary of the given data.

After a paragraph is generated HOW to check that the summary is a good summary of the data.?
To check how good a model is we could use the concept of [ROUGE](https://en.wikipedia.org/wiki/ROUGE_(metric)) - Recall-Oriented Understudy for Gisting Evaluation. Take a document which has already summarised versions by different human beings. Calculate the summary from your model. Now compare your generated summary to the existing summaries and see how much close it is. The more close it is to the existing summaries the more better it is.
