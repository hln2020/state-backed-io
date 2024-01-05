# State-Backed Information Operations Analysis Using Pre-trained Transformer-Based Models


## Introduction

State-backed information operations (IO) involve coordinated efforts, including fake accounts, disinformation, propaganda, and deceptive tactics, orchestrated by governments or state-sponsored entities. They aim to shape narratives, create confusion, and manipulate perceptions, especially on social media and online platforms. This tool has become prominent for state actors to influence public opinion and advance geopolitical interests. Understanding the scope and methods of state-backed information operations is crucial for safeguarding online discourse integrity and protecting the democratic foundations of the digital age.

## Approach

Our primary goal is to create a classification model to identify state-backed information operations on Twitter. We utilize existing pretrained transformer-based models to establish a generalizable approach for detecting suspicious content associated with such operations. Additionally, we aim to implement clustering and narrative extraction techniques to summarize and identify overarching themes within state-backed information operations.

## Experiments

Ada is fine-tuned using two approaches and benchmarked across four metrics.  Details of our training data construction and experimental setup, as well as results are outlined in [State-backed IO Report.pdf](State-backed%20IO%20Report.pdf). Further detail on the code can be found in [State-backed IO Classification.ipynb](State-backed%20IO%20Classification.ipynb).


## Discussion and Conclusion

In conclusion, our results show that content pertaining to IO accounts is noisy, warranting further investigation beyond their tweet content to detect such operations. Our model performance in IO content detection improves when they are trained on two IOs (REA and CNHU) compared to one (REA), though they are more effective at identifying non-IO tweets than IO tweets, as indicated by the relatively high precision combined with low recall. This can be attributed to the noisy content of the IO data, which includes many trivial tweets.

In general, many factors outside of tweet content could impact the detection of information operations, such as account activity, spam level, interactions with other accounts, among others. Future work may consider these aspects in their IO detection analysis for improved performance.

