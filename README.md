EXP 1
1. AIM:

To implement a program that demonstrates the use of a text corpus in Natural Language Processing (NLP) using:
i) Brown Corpus or
ii) Penn Treebank Corpus

2. REQUIREMENTS (Software/Hardware):

Software:

Python 3.x

NLTK (Natural Language Toolkit) Library

Jupyter Notebook / VS Code / Any Python IDE

Hardware:

A computer with minimum 4 GB RAM

Internet connection (for downloading corpus data)

3. PROGRAM:
Example using Brown Corpus:
import nltk
from nltk.corpus import brown

# Download the Brown corpus (only once)
nltk.download('brown')

# Display categories available in the Brown Corpus
print("Categories in Brown Corpus:\n", brown.categories())

# Load words and sentences from a specific category
news_words = brown.words(categories='news')
news_sentences = brown.sents(categories='news')

print("\nTotal number of words in 'news' category:", len(news_words))
print("First 20 words:", news_words[:20])

print("\nTotal number of sentences in 'news' category:", len(news_sentences))
print("First sentence:", ' '.join(news_sentences[0]))

OR Example using Penn Treebank Corpus:
import nltk
from nltk.corpus import treebank

# Download Penn Treebank corpus (only once)
nltk.download('treebank')

# Display number of parsed sentences
print("Total number of parsed sentences:", len(treebank.parsed_sents()))

# Print the first sentence in parsed form
print("\nFirst parsed sentence:\n")
print(treebank.parsed_sents()[0])

# Print the raw words from the first sentence
print("\nWords in the first sentence:")
print(treebank.words()[:20])

4. OUTPUT:
If using Brown Corpus:
Categories in Brown Corpus:
['adventure', 'belles_lettres', 'editorial', 'fiction', 'government', 'hobbies', 'humor', 'learned', 'lore', 'mystery', 'news', 'religion', 'reviews', 'romance', 'science_fiction']

Total number of words in 'news' category: 100554
First 20 words: ['The', 'Fulton', 'County', 'Grand', 'Jury', 'said', 'Friday', 'an', 'investigation', 'of', 'Atlanta', "''s", 'recent', 'primary', 'election', 'produced', '``', 'no', 'evidence', "''"]

Total number of sentences in 'news' category: 4623
First sentence: The Fulton County Grand Jury said Friday an investigation of Atlanta 's recent primary election produced no evidence .

If using Penn Treebank Corpus:
Total number of parsed sentences: 199

First parsed sentence:
(S (NP-SBJ (NNP Pierre) (NNP Vinken) (, ,) (ADJP (NP (CD 61) (NNS years)) (JJ old)) (, ,))
   (VP (MD will)
     (VP (VB join)
       (NP (DT the) (NN board))
       (PP-CLR (IN as)
         (NP (DT a) (JJ nonexecutive) (NN director)))
       (NP-TMP (NNP Nov.) (CD 29))))
   (. .))

Words in the first sentence:
['Pierre', 'Vinken', ',', '61', 'years', 'old', ',', 'will', 'join', 'the', 'board', 'as', 'a', 'nonexecutive', 'director', 'Nov.', '29', '.']

5. CONCLUSION:

The experiment successfully demonstrated how to use text corpora such as the Brown Corpus and Penn Treebank Corpus for natural language processing tasks.
We learned how to access, explore, and analyze the linguistic data stored in these corpora, which can be used for applications like part-of-speech tagging, syntactic parsing, and text analysis.

6. QUESTIONS:
Q1. Define Brown Corpus. What’s the main feature of Brown Corpus?

Answer:
The Brown Corpus is one of the first general-purpose, structured text corpora in English. It was compiled at Brown University in 1961 and contains about 1 million words of American English text from 500 samples of various genres such as news, fiction, government, and science.
Main Feature: It is categorized into genres, making it ideal for comparing linguistic usage across different types of writing.
