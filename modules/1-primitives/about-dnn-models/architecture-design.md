# Major Components in Designing a DNN Architecture

## Terminology

1. In the context of DNN pipelines, we need to design
   1. Data
   2. Embeddings Model
   3. Task Model
   4. Loss Function
2. In the context of information embeddings, we need to design
   1. Information
   2. Embeddings
   3. Tasks
   4. Metrics

## Thinking Procedures

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

## Design Procedures

1. Trade-off between different tasks.
   1. Tasks should have actual meanings.
   2. Tasks should be trainable (data source is available).
2. Design the loss function to evaluate model's performance on the task.
3. Data collection
   1. Corpus centric
      1. Collect from working systems
      2. Collect from human labels
      3. Active learning
      4. Model generated data
   2. Closed loop
      1. Tools: Data analysis of human behaviors to quantify model-human interaction.
      2. Categories
         1. Positive evaluation
            1. Evaluate how do people think about the results.
         2. ${\epsilon}$ Greedy
            1. Randomly replace the result with a low-probability result every ${\epsilon}$ time. Explore possibilities and pass the gradients back to the whole system.
         3. ${\epsilon^2}$ Greedy
            1. Randomly replace the result of some expert engine (ML model) in the MoE system with a low-probability result every ${\epsilon}$ time. Explore possibilities and pass the gradients back to the expert engine.
