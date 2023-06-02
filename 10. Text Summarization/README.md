The provided code demonstrates the generation of a summary for a given text using the TF-IDF (Term Frequency-Inverse Document Frequency) approach and the TextRank algorithm.

First, the code imports the necessary libraries from NLTK (Natural Language Toolkit) and scikit-learn. It also downloads the required NLTK resources for tokenization and stopwords.

The `preprocess_text` function takes a text as input and performs preprocessing steps on it. It tokenizes the text into sentences using the `sent_tokenize` function. Then, it preprocesses each sentence by converting it to lowercase, removing special characters, and splitting it into words. It removes stopwords using the NLTK's English stopwords list and applies stemming using the Porter stemmer. Finally, it joins the processed words back into a sentence and returns a list of processed sentences.

The `generate_summary` function takes a text and the desired number of sentences for the summary as input. It first preprocesses the text by calling the `preprocess_text` function. Then, it creates a TF-IDF matrix using the `TfidfVectorizer` from scikit-learn. This matrix represents the importance of each word in the text. Next, it calculates the similarity matrix using cosine similarity between the TF-IDF matrix's rows.

The code then ranks the sentences based on their scores, which are calculated as the sum of similarities with other sentences. It sorts the sentences in descending order based on the scores. Finally, it generates the summary by selecting the top-ranked sentences from the original text and concatenating them into a summary string.

In the example usage, a text about the impact of artificial intelligence on the healthcare industry is provided. The `generate_summary` function is called with the text and the desired number of sentences for the summary (4 in this case). The resulting summary is printed.

This code can be used to automatically generate summaries for various types of text, such as articles, reports, or research papers, providing a concise overview of the main points and key information contained in the text.
