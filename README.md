Evaluating ChatGPT’s Responses to Different Identities
Overview
This repository contains the final project report for the Spring 2024 W241 course titled "Evaluating ChatGPT’s Responses to Different Identities." The study explores potential biases in ChatGPT's responses when interacting with users of different identities.

Authors
Jing Wen
I-Hsiu Kao
Jacob Schamp
Paul Cooper
Abstract
The issue of bias in ChatGPT is contentious, with users relying on it for various tasks such as writing emails and providing advice. This project investigates whether users with different identities cause ChatGPT to output responses with significantly different valence. Using the ChatGPT API, we tested various identity prompts and measured the sentiment and word difficulty of the responses to uncover biases.

Research Question
The main question addressed in this study is: "Does ChatGPT bias its responses based on the identity of the person asking the question?" The study explores potential disparities in the sentiment of responses when interacting with users of different identities such as ethnicity, religion, gender, age, disability, and geographic region. Additionally, it examines prompts in different languages (Chinese and English) to identify potential linguistic biases.

Hypotheses
Null Hypothesis (H0): Users with different identities do not cause ChatGPT to output responses with significantly different valence.
Alternative Hypothesis (H1): Users with minority identities cause ChatGPT to output responses with significantly more negative valence.
Methodology
Experiment Design
The study employs a factorial design with identity variables such as ethnicity, religion, gender, age, disability, and region. Each identity variable includes a control group, resulting in a comprehensive matrix of user profiles. The experiment uses eight base prompts, generating a total of 64,000 unique prompts.

Sentiment Analysis
Responses from ChatGPT were analyzed using the NLTK library's SentimentIntensityAnalyzer, which calculates a compound sentiment score ranging from -1 (most negative) to 1 (most positive).

Model Choice
The study uses OpenAI’s ChatGPT3.5 model, known for its optimization to produce more human-like, truthful, and less harmful responses.

Randomization
The ChatGPT API's stateless nature ensures randomization, with each prompt treated as a new request.

Power Calculation
The study achieved a power of 0.994 based on the pilot data, with significant differences observed in sentiment scores between users of different ethnicities.

Findings
Including any ethnicity in the prompt decreased the sentiment score compared to the control (no ethnicity mentioned), with self-identifying as white resulting in the most significant decrease.
Ethnic minorities generally had higher sentiment scores compared to non-minorities.
Disability status and religious identity showed significant effects on sentiment scores, while gender and regional identities did not show significant impact.
Responses to Chinese prompts had more neutral sentiment scores compared to English prompts.
Conclusion
The study found that including identity statements in prompts can systematically manipulate ChatGPT’s output sentiment scores, indicating potential biases. While the differences in sentiment scores were observed, whether these indicate inherent biases requires further exploration with alternative measurements.

Future Research
Future studies should explore other measures of bias, different language models, and languages with fewer speakers to understand bias patterns better.

References
Deshpande, A., et al. (2023). Toxicity in CHATGPT: Analyzing persona-assigned language models. Findings of the Association for Computational Linguistics: EMNLP 2023. Link
Motoki, F., et al. (2023). More human than human: Measuring chatgpt political bias. Public Choice, 198(1–2), 3–23. Link
Bird, S., et al. (2023). Natural Language Toolkit (NLTK) Documentation. Link
Ouyang, L., et al. (2022). Training language models to follow instructions with human feedback. ArXiv, abs/2203.02155.
Dale, E., & Chall, J. S. (1948). A formula for predicting readability: Instructions. Educational Research Bulletin, 27(2), 37-54.
