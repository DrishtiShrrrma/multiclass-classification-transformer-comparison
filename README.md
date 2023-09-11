# Detection of Normal, Hate, and Offensive Speeches

Dataset Source: https://www.kaggle.com/datasets/subhajournal/normal-hate-and-offensive-speeches

Normal, Hate, and Offensive Speeches
The data has been scraped from Twitter through Apify regarding the tweets of normal, hate and offensive speeches. The complete database contains 12 datasets where the data are available for normal, hate and offensive speeches with four CSV files each. To create the complete standalone data, all 12 datasets need to be merged by relevant file labels.


Highlights:
1. handled mild class imbalance
2. data visulaizations
3. weight normalization
4. compared performance of various transformers
5. 


| Model                 | Accuracy | Weighted F1 | Weighted Recall | Weighted Precision | Micro F1 | Micro Recall | Micro Precision | Macro F1 | Macro Recall | Macro Precision | Training Time | Evaluation Time |
|-----------------------|----------|-------------|-----------------|--------------------|----------|--------------|-----------------|----------|--------------|-----------------|----------------|-----------------|
| bert-base-uncased     | 0.9935   | 0.9935      | 0.9935          | 0.9935             | 0.9935   | 0.9935       | 0.9935          | 0.9933   | 0.9931       | 0.9936          | 83.87s         | 650ms           |
| bert-large-uncased    | 0.9935   | 0.9935      | 0.9935          | 0.9936             | 0.9935   | 0.9935       | 0.9935          | 0.9932   | 0.9938       | 0.9927          | 275.92s        | 1.74s           |
| distilbert-base-uncased| 0.9935   | 0.9935      | 0.9935          | 0.9936             | 0.9935   | 0.9935       | 0.9935          | 0.9932   | 0.9938       | 0.9927          | 46.27s         | 365ms           |
| diptanu/fBERT          | 0.9935   | 0.9935      | 0.9935          | 0.9936             | 0.9935   | 0.9935       | 0.9935          | 0.9932   | 0.9938       | 0.9927          | 81.92s         | 634ms           |
| GroNLP/hateBERT        | 0.9902   | 0.9902      | 0.9902          | 0.9904             | 0.9902   | 0.9902       | 0.9902          | 0.9901   | 0.9903       | 0.9899          | 81.93s         | 637ms           |
| roberta-large          | 0.9837   | 0.9837      | 0.9837          | 0.9839             | 0.9837   | 0.9837       | 0.9837          | 0.9832   | 0.9821       | 0.9845          | 281.49s        | 1.74s           |



| Model                | Macro F1 Score | Eval Loss | Eval Runtime |
|----------------------|----------------|-----------|--------------|
| bert-base-uncased    | 0.9933         | 0.0164    | 650ms        |
| bert-large-uncased   | 0.9932         | 0.0097    | 1.74s        |
| distilbert-base      | 0.9932         | 0.0178    | 365ms        |
| fbert/hate           | 0.9932         | 0.0152    | 634ms        |
| hateBERT             | 0.9901         | 0.0207    | 637ms        |
| roberta-large        | 0.9832         | 0.0293    | 1.74s        |

