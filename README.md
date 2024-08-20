# Generative AI Question Answering

This repository demonstrates how to use Google Generative AI to create a question-answering system based on pre-computed embeddings of textual data. The system identifies the most relevant information from a dataset and generates contextually appropriate responses.

## Table of Contents
- [Introduction](#introduction)
- [Setup](#setup)
- [Libraries Used](#libraries-used)
- [Usage](#usage)
- [Main Application](#main-application)
- [Code Overview](#code-overview)
- [License](#license)

## Introduction
This project leverages Google’s Generative AI to answer questions about historical monuments using embedded text data. The process involves finding the most relevant passage from a dataset and generating answers with contextually rich responses using a generative model.

## Setup
1. **Obtain Google API Key:**
   - Sign in to your [Google Cloud Console](https://console.cloud.google.com/).
   - Navigate to the **API & Services** section.
   - Enable the **Generative AI API** for your project.
   - Go to the **Credentials** tab and create an API key.
   - Copy the API key for use in your script.

2. **Install the required package:**
   ```bash
   pip install -q -U google-generativeai
   ```

3. **Configure your API key:**
   - Replace `'your api key'` in the script with your actual Google API key.

4. **Prepare the data files:**
   - Ensure you have `embeddingv3.csv` and `embeddingdatav3.pickle` in the `/content/` directory.

## Libraries Used
- **`google.generativeai`**: A library for interacting with Google’s Generative AI services, including embedding content and generating responses.
- **`numpy`**: Provides support for large, multi-dimensional arrays and matrices, along with a collection of mathematical functions to operate on these arrays. Used for numerical operations and computing dot products.
- **`pandas`**: A data manipulation and analysis library, used for reading CSV files and managing data in DataFrames.
- **`pickle`**: A module used for serializing and deserializing Python objects. Here, it loads pre-computed embeddings from a binary file for similarity operations.
- **`textwrap`**: A module for formatting text, used to create prompts with a specified format for the generative model.

## Usage
1. **Set your query:**
   - Update the `query` variable in the script with your desired question.

2. **Run the script:**
   - Execute the script in a Jupyter notebook or Google Colab to see the generated response.

## Main Application
The generative AI question-answering feature is part of MonuTalk, an innovative application that blends the worlds of ancient monuments and modern conversation. MonuTalk uses advanced image recognition and NLP to facilitate engaging dialogues about historical artifacts.

The app recognizes monuments with Convolutional Neural Networks (CNNs) and provides detailed information about them. It also features a chatbot with Generative Deep Neural Networks (Gemini AI), enabling users to interact with animated historical figures and receive personalized recommendations based on sentiment analysis.

MonuTalk enhances the educational experience by offering immersive interactions with history, accessible through both web and mobile platforms. Its integration of sentiment analysis and recommendations makes it a comprehensive tool for discovering and learning about ancient history.

## Code Overview
- **`find_best_passage(query, dataframe)`**: Finds the most relevant passage by computing the dot product between the query and document embeddings.
- **`make_prompt(query, relevant_passage)`**: Creates a prompt for the generative model using the query and the most relevant passage.
- **`gen_ans(query)`**: Generates an answer using Google’s Generative AI model based on the prompt.

## License
This code is provided for educational and research purposes. If you intend to use it for commercial purposes, please contact us for permission. Unauthorized commercial use is not permitted.

## References
- [Google Generative AI Cookbook](https://cloud.google.com/generative-ai/cookbook) - A comprehensive guide to using Google’s Generative AI tools.