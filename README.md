# Neural Machine Translation Model Comparison

[Hugging Face Link](https://huggingface.co/spaces/himanishprak23/neural_machine_translation)

## Introduction
This project aims to develop and compare two different neural machine translation (NMT) models for English to Hindi translation. We have implemented an LSTM-based model and a transformer-based model, specifically the Helsinki NLP Opus-MT model. The comparison is made using a Gradio interface to demonstrate and evaluate the performance of each model.

## Motivation
Machine translation is a crucial application of natural language processing (NLP) that facilitates cross-lingual communication. By comparing different NMT models, we aim to identify the strengths and weaknesses of each approach and understand how they can be optimized for better performance in specific translation tasks.

## Related Work
Several research works have been conducted in the field of neural machine translation, including:
•⁠  ⁠Sequence-to-sequence models using LSTM and GRU architectures.
•⁠  ⁠Transformer models, particularly those developed by the Helsinki NLP group.
•⁠  ⁠Various benchmarks and datasets used for training and evaluating NMT models.

## Data and Pre-processing
We used parallel corpora of English-Hindi sentences for training and evaluation. The data was pre-processed by:
•⁠  ⁠Tokenizing sentences into words.
•⁠  ⁠Lowercasing all text.
•⁠  ⁠Removing special characters and punctuation.
•⁠  ⁠Padding sequences to ensure uniform input length for the models.

## Model Architecture
### LSTM Model
•⁠  ⁠An encoder-decoder architecture with LSTM units.
•⁠  ⁠A single hidden layer trained for 50 epochs.
•⁠  ⁠Attention mechanism to improve translation quality.

![alt text](LSTM_architecture.png)

### Helsinki NLP Opus-MT Model
•⁠  ⁠Transformer-based architecture.
•⁠  ⁠Fine-tuned on the English-Hindi translation task.
•⁠  ⁠Pre-trained on a large multilingual dataset.

![alt text](code/NMT.png)

## Model Training Setting
•⁠  ⁠LSTM Model: Trained for 50 epochs with a batch size of 64, using an Adam optimizer and a learning rate of 0.001.
•⁠  ⁠Helsinki NLP Opus-MT Model: Fine-tuned for 5 epochs with a batch size of 32, using an Adam optimizer and a learning rate of 5e-5.

## Results
The Gradio interface (screenshot provided) allows users to input English text and view the Hindi translations generated by both models. Examples provided include translations of technical terms and common phrases, demonstrating the strengths and weaknesses of each model in handling different types of content.

![alt text](gradio_NMT.png)

## Conclusion
•⁠  ⁠The LSTM model performs well on simpler sentences but struggles with complex structures and longer sentences.
•⁠  ⁠The Helsinki NLP Opus-MT model provides more accurate translations for complex and varied sentence structures due to its transformer architecture and pre-training on a larger dataset.
•⁠  ⁠Both models have their advantages, and the choice of model may depend on the specific requirements of the translation task.

## Future Work
•⁠  ⁠Further fine-tuning of the Helsinki NLP Opus-MT model to improve performance on specific domains.
•⁠  ⁠Exploration of additional transformer-based models and comparison with LSTM and GRU architectures.
•⁠  ⁠Incorporation of more extensive datasets for training to improve the generalizability of the models.
•⁠  ⁠Development of a more user-friendly interface with additional features for real-time translation and evaluation.
