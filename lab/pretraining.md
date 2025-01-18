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

## Estimation of CPU Hours

* Total Tokens (Wikipedia): 20 Million
* Model Parameters: 8.6 Million

Total FLOPs Estimation: 6 (a factor from the scaling law paper) x 8.6M X 20M = 10^15

### CPU Memory

* Parameters: 8.6M X 4 bytes (32-bit precision) = 34MB
* Gradients: 34MB
* Optimizer States (Adam): 34 x 2 = 68MB
* Activations: ~30MB

Total Estimated Memory: ~170MB

### CPU Hours
* Intel Core i7 (FP32): ~150 GFLOPS

Training Hours / Epoch = Total FLOPS / CPU FLOPS = 10^15 / (150 X 10^9) = 6880s = ~2h 





