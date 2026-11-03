# AI-Powered Paraphrasing Tool

## Project Overview

The AI-Powered Paraphrasing Tool is a Natural Language Processing (NLP) application that automatically rewrites input sentences while attempting to preserve their original meaning.

The project uses a pre-trained T5-based transformer model to generate multiple paraphrased versions of a given sentence. It also includes grammar checking, semantic similarity measurement, lexical difference analysis, and text evaluation metrics.

## Objectives

- Generate multiple paraphrased versions of input text.
- Preserve the original meaning while changing sentence structure and vocabulary.
- Check generated sentences for grammar and spelling issues.
- Measure semantic similarity between original and paraphrased text.
- Evaluate lexical differences and selected text-generation metrics.

## Technologies Used

- Python
- Google Colab
- PyTorch
- Hugging Face Transformers
- T5 Transformer Model
- Sentence Transformers
- LanguageTool
- NLTK
- SacreBLEU
- ROUGE
- Pandas
- NumPy
- Scikit-learn

## Model Architecture

The project uses the pre-trained model:

`humarin/chatgpt_paraphraser_on_T5_base`

The model is based on the T5 (Text-to-Text Transfer Transformer) architecture.

The model generates three paraphrase candidates using beam search and diverse beam groups.

## Project Workflow

1. Accept input text from the user.
2. Tokenize the input using the T5 tokenizer.
3. Pass the tokenized text to the pre-trained paraphrasing model.
4. Generate three paraphrased versions.
5. Calculate semantic similarity using Sentence Transformers.
6. Measure lexical similarity and lexical difference using TF-IDF and cosine similarity.
7. Check grammar and spelling using LanguageTool.
8. Evaluate text-generation quality using BLEU and ROUGE metrics on a sample with a manually written reference.
9. Display the generated outputs and evaluation results.

## Evaluation Metrics

| Metric | Purpose |
|---|---|
| Semantic Similarity | Estimates how closely the paraphrase retains the original meaning |
| Lexical Similarity | Measures overlap in vocabulary |
| Lexical Difference | Measures changes in wording |
| Grammar Checking | Identifies potential grammar and spelling issues |
| BLEU | Measures n-gram overlap with a reference sentence |
| ROUGE | Measures lexical overlap with a reference sentence |

## Final Model Evaluation

The model was tested using five different input sentences, generating three paraphrases for each.

| Evaluation Metric | Result |
|---|---:|
| Total Test Sentences | 5 |
| Total Paraphrases Generated | 15 |
| Average Semantic Similarity | 0.879 |
| Average Lexical Difference | 0.6759 |
| LanguageTool Flags | 1 |
| Confirmed Grammar Errors | 0 |

The single LanguageTool flag was reviewed manually and identified as a minor punctuation suggestion rather than a confirmed grammar error.

## Sample Input

"Machine learning is helping businesses analyse large amounts of data, improve decision-making, and automate repetitive tasks."

## Sample Generated Paraphrases

1. The use of machine learning is enabling businesses to analyze vast amounts of data, improve decision-making, and automate repetitive tasks.

2. Businesses are leveraging machine learning to analyze vast amounts of data, optimize decision-making and automate the execution of repetitive tasks.

3. By analyzing vast amounts of data, businesses are using machine learning to improve decision-making and automate repetitive tasks.

## Key Features

- Multiple paraphrase generation.
- Transformer-based NLP model.
- Semantic similarity evaluation.
- Lexical difference analysis.
- Grammar and spelling checking.
- BLEU and ROUGE evaluation.
- Console-based user interaction.

## Limitations

- The model may occasionally generate sentences that are too similar to the original.
- Semantic similarity scores are estimates and do not guarantee complete preservation of meaning.
- LanguageTool may flag acceptable punctuation or stylistic choices.
- BLEU and ROUGE results depend on the quality and availability of reference sentences.
- Evaluation was conducted on a small sample of five input sentences and should not be treated as a large-scale benchmark.
- The application uses a pre-trained model rather than training a transformer from scratch.

## Future Improvements

- Develop a web-based interface using Streamlit or Flask.
- Test the model on a larger dataset.
- Include multiple human-written reference paraphrases for more reliable evaluation.
- Support longer paragraphs and multiple languages.
- Compare different transformer-based paraphrasing models.

## Conclusion

This project demonstrates the application of transformer-based NLP techniques for automatic text paraphrasing. The system generates multiple alternative sentences and evaluates them using semantic similarity, lexical difference, grammar checking, and reference-based evaluation metrics.

The project provided practical experience in using pre-trained transformer models, text generation, NLP evaluation techniques, and integrating multiple components into a Python application.
