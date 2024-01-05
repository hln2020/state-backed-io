# State-Backed Information Operations Analysis Using Pre-trained Transformer-Based Models

## Abstract

Leveraging pretrained transformer-based models and clustering techniques, we establish a generalizable approach for detecting suspicious content and identifying state-backed information operations (IO) on Twitter. Additionally, we implement narrative extraction techniques to summarize and identify overarching themes within state-backed IOs. Results show that content pertaining to IO accounts is noisy, warranting further investigation beyond tweet content to detect information operations. Nonetheless, finetuning pre-trained models on more IOs can lead to an increase in model performance.

## Introduction

State-backed information operations (IO) involve coordinated efforts, including fake accounts, disinformation, propaganda, and deceptive tactics, orchestrated by governments or state-sponsored entities. They aim to shape narratives, create confusion, and manipulate perceptions, especially on social media and online platforms. This tool has become prominent for state actors to influence public opinion and advance geopolitical interests. Understanding the scope and methods of state-backed information operations is crucial for safeguarding online discourse integrity and protecting the democratic foundations of the digital age.

## Related Work

Related work on the topic of state-backed information operations includes a range of studies published since Twitter launched their first archive of foreign information operations in 2018. Barrie et al. [1] examined domestic engagement with IO accounts in Saudi Arabia, revealing that domestic engagement with IO tweets was significantly lower than that with the average Saudi Twitter user. DiResta et al. [2] delved into the activity analysis and narrative extraction of a state-backed operation attributed to the Saudi Arabian digital marketing firm Smaat, uncovering tweets criticizing Qatar’s government and tweets criticizing Jamal Khashoggi, among other themes. These studies inspire our research by highlighting the importance of understanding state-sponsored information operations and how they shape digital-age narratives. 

## Approach

Our project's primary goal is to create a classification model to identify state-backed information operations on Twitter. We utilize existing pretrained transformer-based models to establish a generalizable approach for detecting suspicious content associated with such operations. Additionally, we aim to implement clustering and narrative extraction techniques to summarize and identify overarching themes within state-backed information operations.

## Experiments

We fine-tune Ada and BERT using two approaches and benchmark their performance across four metrics. Additionally, we simulate a real-world scenario through a third approach to evaluate BERT's performance. We experiment with various data preprocessing methods and record their impact on BERT. Details of our training data construction and experimental setup are outlined below.


## Discussion and Conclusion

In conclusion, our results show that content pertaining to IO accounts is noisy, warranting further investigation beyond their tweet content to detect such operations. Our model performance in IO content detection improves when they are trained on two IOs (REA and CNHU) compared to one (REA), though they are more effective at identifying non-IO tweets than IO tweets, as indicated by the relatively high precision combined with low recall. This can be attributed to the noisy content of the IO data, which includes many trivial tweets.

To enhance our models, we need more diverse training data that better aligns with the test data distribution, or a larger dataset containing a sufficient number of tweets in various languages, enabling the model to learn and generalize to unseen tweets. In general, many factors outside of tweet content could impact the detection of information operations, such as account activity, spam level, interactions with other accounts, among others.

Future work may consider these aspects in their IO detection analysis for improved performance.

