# translation-assignment

File Information

1. `inference.ipynb`
* Contains code utilizing the satpalsr/llama2-translation-filter-full model for inference on [validation dataset](https://huggingface.co/datasets/satpalsr/chatml-translation-filter/viewer/default/validation).
* Accuracy obtained: 63.88% considering all outputs from a sample for calculation 
* Accuracy obtained is 59.874% when considering first output for calculations

2. QLoRA_FineTune_and_Inference.ipynb
* Fine-tuned Meta-Llama-2-7b on [satpalsr/chatml-translation-filter](https://huggingface.co/datasets/satpalsr/chatml-translation-filter) using Unsloth-AI as 4 bit model 
* Trained and compared accuracy on varying number of steps using validation part of the dataset
| Steps | Accuracy |
| ----- | -------- |
| 60    | 63.888%  |
| 100   | 66.975%  |
| 150   | 72.222%  |
| 200   | 69.135%  |

## Suggestions
* Increasing training steps led to increase in accuracy so model can be trained for more steps
* Use of one-shot or other techniques to provide examples to model may improve model performance
* Increasing training data can better align model to output format
* More data across all classes of topics (escpecially where translation is harmful) can help with more general behavior
* Hyperparameter tuning may improve performance
* Using frameworks for desired format output from LLM
