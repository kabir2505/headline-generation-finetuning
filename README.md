# Fine-tuning T5 and BART for Headline Generation Given News Articles

This repository contains code for fine-tuning the T5 and BART models for the task of **headline generation** based on news articles. The project explores using Transformer-based encoder-decoder models to generate concise and relevant headlines from lengthy news articles.

## Project Files

- **900.csv**: Dataset containing news articles and corresponding headlines for training and evaluation.
- **900.ipynb**: Jupyter notebook for pre-processing, training, and fine-tuning T5 and BART models.
- **predicted_headlines.csv**: The output file containing the predicted headlines generated by the fine-tuned models.

## Models Used

### T5
T5 (Text-to-Text Transfer Transformer) is a transformer-based model pre-trained on a multi-task learning objective. It is fine-tuned for headline generation by conditioning on the input news article.

### BART
BART (Bidirectional and Auto-Regressive Transformers) is another transformer-based model that combines the benefits of both BERT (bidirectional) and GPT (autoregressive). It is also used for headline generation.

## Fine-tuning Approach

- **Encoder-Decoder Architecture**: We used the encoder-decoder setup because headline generation is a sequence-to-sequence task, where the input (news article) is encoded into a fixed-size representation by the encoder, and the decoder generates the headline based on this representation.
- **Why not just Encoder or Decoder?**: Using only an encoder (like BERT) would not allow the generation of new text (headlines), as it lacks a mechanism for autoregressive text generation. Using only a decoder (like GPT) would require a predefined prompt, making it less flexible for diverse inputs like full news articles.
