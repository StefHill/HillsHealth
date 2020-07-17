BERT was announced in Oct 2018 when Google AI released a paper entitled ‘BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding’.  

There has been a lot of fanfare about this pretrained model, and I wanted to consider BERT as a potential solution to abstractive summarisation (particularly SciBert which is pretrained on scientific text, rather than the original BERT which is pretrained on the entire Wikipedia and a book corpus).  

Note that the tech is moving very quickly on this issue, and its possible that a sequence-to-sequence model (which works for text summarisation), ALBERT, ERNIE or T5 could all become the preferred springboard to deal with abstractive summarisation.  At present, T5 by Google rates highest for a paraphrasing model as shown on https://gluebenchmark.com/leaderboard



A brief summary of BERT from what is understood from the excellent Illustrated Transformer (http://jalammar.github.io/illustrated-transformer/);

Encoder;
The self-attention layer takes each word at a time and considers its context by looking at the words around it.  The Encoder then puts the word into a feedforward neural net which subsequently outputs the embeddings.

