# Document_Classifcation

Document Classification Using Different Word Embeddings With LDA.
Data:
The Consumer Complaint Database is a collection of complaints about consumer financial products and services that we sent to companies for response. Complaints are published after the company responds, confirming a commercial relationship with the consumer, or after 15 days, whichever comes first.

Libraries:
Pandas, Numpy, NLTK, Sklearn, Gensim, PyLDA, Matplotlib, Regx.

Visualization:
PyLDA, Word Cloud, Histogram.

Text Cleaning:
Used regx for replacing and removing speacial letters.

Removed stops words from text using NLTK.

Removed words less than 3 letters.

Lowered all the letters.

Using Gensim utils tokenized the sentences in the documents and made into list form.

Those tokens are changed to dictionary form using gensim corpora.

And then into Term Document Frequency.


# Model Building using LDA
# Latent Dirichlet Allocation (LDA)
LDA is a generative probabilistic model that assumes each topic is a mixture over an underlying set of words, and each document is a mixture of over a set of topic probabilities.

Latent Dirichlet allocation is a way of automatically discovering topics that these sentences contain. For example, given these sentences and asked for 2 topics, LDA might produce something like

Sentences 1 and 2: 100% Topic A Sentences 3 and 4: 100% Topic B Sentence 5: 60% Topic A, 40% Topic B

Topic A: 30% broccoli, 15% bananas, 10% breakfast, 10% munching, …

Topic B: 20% chinchillas, 20% kittens, 20% cute, 15% hamster, …

You could infer that topic A is a topic about food, and topic B is a topic about cute animals. But LDA does not explicitly identify topics in this manner. All it can do is tell you the probability that specific words are associated with the topic.

#For detail understanding of LDA:https://medium.com/@lettier/how-does-lda-work-ill-explain-using-emoji-108abf40fa7d#:~:text=For%20LDA%2C%20those%20parameters%20are,%2Dversus%2Dtopics'%20matrix.


# Metrics
Perplexity:
Perplexity is a statistical measure of how well a probability model predicts a sample. As applied to LDA, for a given value of , you estimate the LDA model. Then given the theoretical word distributions represented by the topics, compare that to the actual topic mixtures, or distribution of words in your documents.

topicmodels includes the function perplexity() which calculates this value for a given model.

Topic Coherence
Topic Coherence measures score a single topic by measuring the degree of semantic similarity between high scoring words in the topic. These measurements help distinguish between topics that are semantically interpretable topics and topics that are artifacts of statistical inference

For more info refer these:

https://rare-technologies.com/what-is-topic-coherence/

https://towardsdatascience.com/evaluate-topic-model-in-python-latent-dirichlet-allocation-lda-7d57484bb5d0

#PyLDA visualization:
![image](https://user-images.githubusercontent.com/60771035/115721217-769a1580-a39b-11eb-822b-19f265de6fd7.png)

![image](https://user-images.githubusercontent.com/60771035/115721444-aa753b00-a39b-11eb-9d81-a23ae7a2d33f.png)
