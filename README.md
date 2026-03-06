# News Summarization and Translation with NLP
## Introduction

In today's fast-paced world, staying informed can be challenging due to the overwhelming amount of news available and the limited time people have to read it. This project was developed to simplify news consumption by automatically extracting the main content from a webpage, generating a concise summary, and translating it into English when needed.

Using Natural Language Processing (NLP) techniques and transformer-based models, this project helps users quickly understand the essential information from online news articles without needing to read the full text.

The application combines web scraping, text summarization, and machine translation into a simple workflow that processes articles directly from a URL.

## Background

With the increasing volume of digital news sources, readers often struggle to keep up with important information. Additionally, language barriers can limit access to relevant content from international sources. 
I have developed this project while living in Canada, a bilingual country with English and French as its two main languages. 

### This project addresses two common challenges:

- **Information overload:** long articles can be difficult to read when time is limited.

- **Language accessibility:** important news may be written in languages that the reader does not understand.

To solve these issues, the project implements two NLP tasks:

**1. Text Summarization:** condensing long articles into shorter, meaningful summaries.

**2. Machine Translation:** translating content from French to English.

By combining these capabilities, the tool allows users to quickly access the key ideas from global news articles.

## Tools and Technologies

This project was built using the following tools and libraries:

### Programming Language

- **Python:** The core programming language used to develop the application, chosen for its flexibility, rich ecosystem, and strong data-processing capabilities.

### Libraries

- **Transformers (Hugging Face):** for implementing pre-trained NLP models

- **BeautifulSoup:** for web scraping article content

- **Requests:** for retrieving webpage data

- **Matplotlib:** for visualization

- **WordCloud:** for visual representation of the most frequent words

### Pretrained Models

- **T5 (Text-To-Text Transfer Transformer):** used for text summarization

- **MarianMT (Helsinki-NLP):** used for machine translation from French to English

## Code Overview

### The project is divided into two main components.

**1. News Article Extraction**

The program first retrieves the content of a news article directly from a URL.

**Steps:**

1. Send a request to the webpage using requests.

2. Parse the HTML content using BeautifulSoup.

3. Extract the textual content from the article.

4. Clean and prepare the text for NLP processing.

**2. Text Summarization (T5 Model)**

The summarization module uses the T5-base transformer model.

### Workflow:

1. Load the pretrained T5 model and tokenizer.

2. Format the input text using the "summarize:" prefix required by T5.

3. Tokenize the article content.

4. Generate a summary using the model's text generation capabilities.

5. Decode the generated tokens into human-readable text.

This process produces a shorter version of the article that captures its main ideas.

**3. Translation (MarianMT Model)**

The translation module uses the MarianMT model from Helsinki-NLP to translate French text into English.

### Workflow:

1. Load the MarianMT model and tokenizer.

2. Tokenize the French input text.

3. Generate translated tokens using the model.

4. Decode the tokens to produce the final English translation.

This allows users to access international news sources without language barriers.

**4. Word Visualization**

To provide an additional overview of the article content, the project generates a Word Cloud highlighting the most frequent terms found in the text.

**Steps:**

1. Process the extracted text.

2. Generate a word frequency visualization using the *WordCloud* library.

3. Display the result with *matplotlib*.

This offers a quick visual representation of the main topics discussed in the article.



## Conclusion

This project demonstrates how modern NLP models can be used to simplify the way we consume information online. By combining web scraping, automatic summarization, and machine translation, the tool helps users quickly understand the key points of news articles while overcoming language barriers.

The use of transformer-based models such as T5 and MarianMT highlights the power of pre-trained language models in solving real-world problems related to information accessibility and efficiency.

