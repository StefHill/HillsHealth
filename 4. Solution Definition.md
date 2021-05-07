### Business Overview

With recent advances in deep learning techniques, there has been notable progress in extractive text summarisation whereby important sentences or phrases are identified and extracted from the original text. 

However, here we will work towards an abstractive summariser whereby the sentences generated may not appear in the original text.  The work will focus on the abstractive summarisation of academic publications (medical journals).

The below diagram illustrates the difference between extractive and abstractive summarisation:

![Drawing1](https://user-images.githubusercontent.com/45914355/84553626-81603480-ad0c-11ea-9b56-ca8f303afe2c.jpg)

### Solution Overview

#### Text Pre-processing

Pre-processing will convert the paper into lowercase and remove any hyperlinks (strings that begin with ‘http’ or ‘https’ should be converted to ‘_weblink_’).  Furthermore, non-standard characters such as hashtags or dollar signs should be removed along with punctuation, symbols, and other non-text words (including code).

Named Entity Recognition will identify phases that refer to a named entity e.g. persons, locations or organisations.   Word tagging (Penn Treebank POS) will distinguish noun phrase, verb phrase etc and will further highlight unrecognised words.  Semantic role labelling will go further, and for each verb, will identify the role of other words with respect to that verb.  
Stopwords will then be removed with the use of the Natural Language Toolkit.  Stopwords don’t have any value and are typically used for the construction of a sentence e.g. ‘it’, ‘and’, ‘they’.

Stemming will be replaced with Lemmatisation which is a more efficient method for extracting the root word e.g. ‘study’ instead of ‘studying’.  Unlike stemming, Lemmatisation uses the dictionary form rather than pre-built logic.  Similarly, shortforms will be replaced with the expanded version e.g. ‘she’s’ is replaced with ‘she is’, and ‘I’ll’ is replaced with ‘I will’.

#### Content Selection

Term Frequency-Inverse Document Frequency (TF-IDF) will be implemented to a) count the number of times a word or phrase appears in a document, and b) devalue the words that appear to many times (i.e those not picked up by the stopwords listed above).

TF-IDF should score a word to rank its importance and add the output to a data frame.  Gaining an understanding of what the article is covering will enable us to consider the keywords for that document, help sort corpus data into categories, and consider further information retrieval.    

#### Vector Model

At the heart of the abstractive summariser will be BERT; a Bidirectional Encoder Representations from Transformers.

The encoder will read the tokenised document one word at a time.  The contextual information of the input sequence will be captured.  Subsequently, the pre-trained decoder will predict the next word in a sequence given the previous word.

The reason for the earlier text processing is due to the encoder-decoders difficulty in memorising long sequences into a fixed length vector.  The length of a medical trial will certainly deteriorate the performance of the encoder-decoder (known as the Vanishing Gradient Problem, the model applies more weight to recent words as opposed to words seen at the beginning of the text).

An attention layer is a matrix placed between the encoder and the decoder that will seek to overcome this problem by aiming to predict a word by looking at a few specific parts of the sequence, rather than the entire sequence.  In essence, it learns what to remember and what to forget.  It learns where to focus its attention.

We will fix the maximum summary length before running the text through the pre-trained BERT model.

#### Concept Diagram

![Concept diagram](https://user-images.githubusercontent.com/45914355/84553133-17935b00-ad0b-11ea-8ce2-e1b04529272b.jpg)

#### Concept Data Flow
...

### Systems Architecture
...

### UI/UX design
...
