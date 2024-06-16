# Explain DNNs from Embeddings

## DNN Structure

1. All DNNs are MLPs (Multi-Layer Perceptrons) by nature.
   1. Components
      1. Hidden layers are embeddings of the input data.
      2. The output layer is the specific task the DNN is trained for.
   2. Features
      1. All parts are extendable.
      2. Embeddings layers are stackable.
         1. We can append multiple embeddings with different specialties.
         2. Embeddings appended could be of different types.
            1. Pure embeddings
               1. word2vec embeddings
               2. BERT embeddings
            2. DNNs
               1. Multi-Head Attention modules in Transformers

## Objective (General) Embeddings vs. Subjective (Specific) Embeddings

1. Objectivity/Generality and Subjectivity/Specificity are relative terms. Their meanings depend on the context.
   1. For a specific DNN model, input embeddings are objective/general for this specific task, while output/hidden embeddings are subjective/specific.
2. Actual specialty of an embedding depends on the task.
   1. If applied to a classifier network, the hidden embedding is specific tailored to the classification task.
   2. If applied to MLM/NSP tasks (BERT model), the hidden embedding understands the general context of the input data.
   3. If applied to contrastive learning/CBOW/Skip-gram tasks, the hidden embedding understands the basic meaning/semantics of the input data.
