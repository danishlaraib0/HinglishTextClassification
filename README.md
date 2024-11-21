# HinglishTextClassification

#Problem Statement
Classifying YouTube comments in Hinglish—a blend of Hindi and English—presents unique challenges due to the code-mixed nature of the language. Traditional natural language processing (NLP) models struggle with the nuances of Hinglish, including its lack of standardization and frequent use of subwords. The goal was to classify these comments into three categories: doubt, feedback, and irrelevant.

#Solution Approach
To address this challenge, we evaluated several machine learning approaches and embedding techniques, including TF-IDF, Word2Vec, FastText, and BERT. Among these:

TF-IDF struggled due to its inability to capture contextual or subword information, essential for Hinglish data.
BERT, while powerful in handling context and nuanced understanding, was limited by resource constraints. With more computational power, BERT would likely outperform other models due to its superior contextual embedding capabilities.
FastText emerged as the optimal solution within the constraints of this project. Leveraging subword information through character-level n-grams, FastText offered speed, multilingual support, and pre-trained embeddings for over 150 languages, making it well-suited for Hinglish classification.
Finally, we used FastText embeddings with an XGBoost classifier, achieving a balanced trade-off between performance and efficiency.

#Future Directions
While FastText performed well in this project, leveraging BERT or other large language models (LLMs) such as GPT-based models could significantly improve performance. These models are equipped to handle code-mixed data more effectively, offering deeper contextual understanding and adaptability. If computational resources and time are not constraints, these advanced approaches could be explored for better classification accuracy.
