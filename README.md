# Sentiment-Bank-Jago-and-Revamp-Validation
Project Overview
This project builds an end-to-end text analytics workflow to analyze user feedback, combining lexicon-based sentiment scoring, a supervised Linear SVM sentiment cross-check (TF-IDF vs Bag of Words), and multi-label issue detection using a keyword/regex taxonomy. Issues are prioritized using a simple impact formula based on how often an issue is mentioned and how negative the mentions are.

Method
1. Data processing & NLP: pandas, NLTK, Sastrawi
2. Sentiment scoring: lexicon-based sentiment polarity
3. Sentiment model cross-check: TF-IDF / BoW + Linear SVM
4. Issue detection: keyword/regex-based multi-label classification across issue categories
5. Prioritization logic:
   - neg_rate = negative_mentions / total_mentions
   - priority_score = total_mentions * neg_rate
  
Key Findings
- Highest severity issue: Data & Privacy with 89.3% negative (1,541 / 1,725 mentions), avg star 1.91
- Largest high-impact pain point: Login & Access with 8,603 mentions, 72.5% negative (6,237 negative), avg star 1.90
- Top priority issues (excluding Uncategorized):
  1. Login & Access
  2. Security
  3. Transactions
  4. Data & Privacy
  5. KYC & Identity Verification
- Lowest average ratings among major issues:
  1. KYC & Identity Verification (1.78)
  2. Login & Access (1.90)
