# Similarity Index (Embeddings)

## Item to Item Similarity

![Item to Item Similarity](./diagrams/similarity-i2i-alibaba.png)

### Intuition

1. User's weight is inversely proportional to the number of different items the user interacts with.
2. Item's weight is the sum of the weights of the users who interact with it.
3. Item-to-item similarity is proportional to users' weights who interact with both items.

## ig2vec Similarity Index

![ig2vec Similarity Index](./diagrams/similarity-ig2vec-instagram.png)
