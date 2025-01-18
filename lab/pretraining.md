# Pre-training a Tiny GPT from Scratch in a CPU-friendly Setting

## Tiny GPT Hyper-parameters
Layers: 6

Hidden Size: 128

D_diff Size: 512

Attention Heads: 2

Sequence Length: 128

Vocabulary Size: 30,000 

## Calculation of Parameter Nums

token embedding: 30000x128 

positional embedding: 128 x 128

attention: 6 x 128 x 128

FFN: 6 x 2 x 128 x 512

Unembedding: 128 x 30000

Total: ~8.6M

## SS

