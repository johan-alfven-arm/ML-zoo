# DS-CNN Small INT8

## Description
This is a fully quantized version (asymmetrical int8) of the DS-CNN Small model developed by Arm, with training checkpoints, from the Hello Edge paper. Code to recreate this model can be found here: https://github.com/ARM-software/ML-examples/tree/master/tflu-kws-cortex-m

## License
[Apache-2.0](https://spdx.org/licenses/Apache-2.0.html)

## Related Materials
### Class Labels
The class labels associated with this model can be downloaded by running the script `get_class_labels.sh`.

### Model Recreation Code
Code to recreate this model can be found here: https://github.com/ARM-software/ML-examples/tree/master/tflu-kws-cortex-m.

## Network Information
| Network Information |  Value         |
|---------------------|------------------|
|  Framework          | TensorFlow Lite |
|  SHA-1 Hash         | cf24429e86a9647b1632c382894bc68d26d34039  |
|  Size (Bytes)       | 47616 |
|  Provenance         | https://github.com/ARM-software/ML-examples/tree/master/tflu-kws-cortex-m |
|  Paper              | https://arxiv.org/abs/1711.07128 |

## Accuracy
Dataset: Google Speech Commands Test Set

| Metric | Value |
|--------|-------|
| Accuracy | 0.935 |

## Performance
| Platform | Optimized |
|----------|:---------:|
| Cortex-A |:heavy_check_mark:          |
| Cortex-M |:heavy_check_mark: HERO         |
| Mali GPU |:heavy_check_mark:          |
| Ethos U  |:heavy_check_mark:          |

### Key
* :heavy_check_mark: - Will run on this platform.
* :heavy_multiplication_x: - Will not run on this platform.



## Optimizations
| Optimization |  Value  |
|-----------------|---------|
| Quantization | INT8 |

## Network Inputs
| Input Node Name |  Shape  | Description |
|-----------------|---------|-------------|
| input | (1, 490) | The input is a processed MFCCs of shape (1, 490) |

## Network Outputs
| Output Node Name |  Shape  | Description |
|------------------|---------|-------------|
| Identity | (1, 12) | The probability on 12 keywords. |
