BERT was announced in Oct 2018 when Google AI released a paper entitled ‘BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding’.  

There has been a lot of fanfare about this pretrained model, and I wanted to consider BERT as a potential solution to abstractive summarisation (particularly SciBert which is pretrained on scientific text, rather than the original BERT which is pretrained on the entire Wikipedia and a book corpus).  

Note that the tech is moving very quickly on this issue, and its possible that a sequence-to-sequence model (which works for text summarisation), ALBERT, ERNIE or T5 could all become the preferred springboard to deal with abstractive summarisation.  At present, T5 by Google rates highest for a paraphrasing model as shown on https://gluebenchmark.com/leaderboard


A brief summary of BERT from what is understood from the excellent Illustrated Transformer (http://jalammar.github.io/illustrated-transformer/);

Encoder;

The self-attention layer takes each word at a time and considers its context by looking at the words around it.  The Encoder then puts the word into a feedforward neural net which subsequently outputs the embeddings.

![pic1 (2)](https://user-images.githubusercontent.com/45914355/87809004-902d9000-c852-11ea-8cad-7f57a1a027a4.png)

The self-attention layer allows the system to link words.  For example, consider the following sentence;

‘the lion went for a walk around his territory.  It sat under a tree’.

Does ‘It’ refer to the lion or the territory? The self-attention layer gives a score for each input word in a vector matrix.  It gives more weight (i.e a higher score) to more relevant words.  As such, we would expect the word ‘lion’ to have a greater score than ‘territory’ with regards to the word ‘It’.

To calculate the self-attention layer will require the creation of 3 vectors for each word in a sequence; a query vector, a key vector and a value vector.

![pic2 (2)](https://user-images.githubusercontent.com/45914355/87809055-a20f3300-c852-11ea-9df3-a7f155666ae9.png)

The word embeddings are multiplied by the 3 weighted vectors.  The query vector is then multiplied by the key vector of all words (including itself)

The score is then divided by 8 which leads to a more stable gradient (8 is the default value as it’s the sq root of the key vector used (i.e. 64)).

![pic3 (2)](https://user-images.githubusercontent.com/45914355/87809089-b18e7c00-c852-11ea-9fe4-81b15fb20390.png)

A Softmax function is then applied as e^x/(∑e^x) where χ is the previous vector value and Σ is the sum of all the χ words added together.  Softmax ensures that all the words add up to 1, and shows the weighted relevance to the key word.  The Softmax value can then be multiplied by each part of the value vector.

The sum of the weighted value vectors produces and output of the self-attention layer for the specific word.  This value is fed into the feed-forward layer.

Each of the outputs needs to be concatenated together to form one vector of nx768 where n = number of words.

Decoder – the decoder will calculate the most likely next word in a sequence.  TBC…


