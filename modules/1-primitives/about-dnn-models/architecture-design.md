# Major Components in Designing a DNN Architecture

## Terminology

1. In the context of DNN pipelines, we need to design
   1. Data Representation
   2. Model Architecture
   3. Loss Function
2. In the context of information embeddings, we need to design
   1. Information structure
   2. Embeddings
   3. Tasks

## Procedures

1. Divide the information structure horizontally
   1. Where does the information embedded?
      1. Information embedded in proximity (pixels, pictures)
      2. Information embedded in sequence (words, sentences, audios, user behavior sequences)
      3. Information embedded in sequential proximity (time series, videos)
      4. Information embedded in graph (social networks, knowledge graphs)
      5. Information embedded in vectos (PINN(Physics-Informed Neural Networks))
2. Divide the information structure vertically
   1. Pixel information
      1. Raw picture pixel embeddings
      2. Transferred ResNet embeddings
      3. Specific CNN Embeddings
   2. Sequence Information
      1. Raw word2vec embeddings
      2. BERT embeddings
      3. Specific RNN/GRU/LSTM/Transformer/Mamba embeddings
3. Design the tasks specific to the information structure
   1. Specific Tasks: classification, regression, clustering, generation, retrieval, rewrite, rank, etc.
   2. General Tasks: MLM, NSP, contrastive learning, CBOW, Skip-Gram etc.
