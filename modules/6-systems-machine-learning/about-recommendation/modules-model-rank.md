# Ranking Models

## Tasks

1. Pointwise Ranking
   1. Task Specifications
      1. Different from retrieval models, ranking models take items and users as input, but the retrieval models give items as the output.
      2. We need to append additional features to items retrieved from the last step.
      3. Each inference only evaluates the ranking value for one item.
2. Pairwise Ranking
   1. Task Specifications: Take pairs of items as input and predict which one is better.
   2. Evaluation Metrics (Loss Function)
      1. BCELoss, use sigmoid to normalize the output, and the input `x` is the difference between the two items' relevance value.
3. Listwise Ranking
   1. Task Specifications: Take a list of items as input and predict the ranking of the list.
   2. Evaluation Metrics (Loss Function)
      1. MAP (Mean Average Precision)

## Examples

![Google](./diagrams/modules-model-rank-co-google.png)
![Youtube](./diagrams/modules-model-rank-co-youtube.png)
![Alibaba](./diagrams/modules-model-rank-co-alibaba.png)
