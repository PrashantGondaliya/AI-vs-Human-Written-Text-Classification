**AI vs Human-Written Text Classification**

**Overview**

This project investigates the differences between AI-generated and human-written abstracts using text analysis and machine learning (ML) models. The primary goal is to develop a classifier that can accurately distinguish between these two types of content, even in short-form text—an area where many current detectors struggle.

**Problem Statement**

The rise of Text Generative Models (TGMs) has resulted in the proliferation of AI-generated content, which raises concerns regarding its misuse, especially for false information and unethical reviews. Detecting AI-generated text reliably is a challenge that the project addresses by exploring text characteristics like length, sentiment, and key phrases.

**Key Components**

Data Collection and Preprocessing
The dataset comprises 4000+ scientific abstracts, both human-written and AI-generated. To prepare the data, standard text preprocessing techniques were applied, such as:

Tokenization
Lowercasing
Stopword removal
Lemmatization
This cleaned the data and prepared it for numerical representation.

Feature Engineering
The TF-IDF (Term Frequency-Inverse Document Frequency) method was used to convert text into numerical vectors. This helped capture the importance of words in the abstracts, making them usable by machine learning algorithms.

**Machine Learning Models Used**
The project explored several ML models to classify abstracts:

Logistic Regression
Multinomial Naive Bayes
Support Vector Machines (SVM)
Decision Trees
Random Forests
Each model's performance was evaluated using metrics like accuracy, precision, recall, and F1-score. Techniques like cross-validation were employed to prevent overfitting and to improve generalizability.

**Insights Gained**

Text Length
The analysis found that AI-generated abstracts tend to be shorter than human-written ones. This provided an opportunity to fine-tune the models specifically for short-form content detection, which is often a weakness of existing AI detectors.

Sentiment Analysis
Sentiment analysis revealed notable differences in emotional tones:

Human-written abstracts showed a more diverse sentiment distribution.
AI-generated abstracts mostly had a positive sentiment, typically between 0.5 and 1.0 on a sentiment scale.
Feature Importance
The most important terms that helped differentiate between AI-generated and human-written abstracts included phrases like:

Human-written: "study", "research"
AI-generated: "paper", "results"
This shows that human authors tend to use more specific and detailed terminology, while AI abstracts focus on more generic words.

**Model Performance**

Among the models tested, Logistic Regression and Random Forests demonstrated the best performance:

Logistic Regression: Provided a high level of interpretability, making it easier to analyze the terms contributing to classification decisions.
Random Forests: Excelled at capturing complex patterns in the data, particularly interactions between words.
The accuracy for the models is as follows:

Logistic Regression: 98.15%
Random Forest: 97.65%
Multinomial Naive Bayes: 96.79%
Decision Tree: 95.81%
Support Vector Machines: 54.0% (SVM struggled with this dataset)

**Conclusion**

This project successfully developed a robust AI-text detector that can distinguish between human-written and AI-generated abstracts with high accuracy. By leveraging insights from text length, sentiment, and word patterns, the classifier offers significant potential for use in content moderation, plagiarism detection, and ensuring academic integrity.

**Future Work**

Further improvements can be made by:

Exploring more advanced deep learning techniques like transformer models.
Expanding the dataset to include more diverse writing styles.
Incorporating real-time detection for applications like online publishing.
