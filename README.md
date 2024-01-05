
# Project Title
Detecting State-Backed Information Operations on Twitter

Abstract
Leveraging pretrained transformer-based models and clustering techniques, this project establishes a generalizable approach for detecting suspicious content and identifying state-backed information operations (IO) on Twitter. Additionally, narrative extraction techniques are implemented to summarize and identify overarching themes within state-backed IOs. Results show that content pertaining to IO accounts is noisy, warranting further investigation beyond tweet content to detect information operations. Nonetheless, finetuning pre-trained models on more IOs can lead to an increase in model performance.

Introduction
State-backed information operations (IO) involve coordinated efforts, including fake accounts, disinformation, propaganda, and deceptive tactics, orchestrated by governments or state-sponsored entities. They aim to shape narratives, create confusion, and manipulate perceptions, especially on social media and online platforms. Understanding the scope and methods of state-backed information operations is crucial for safeguarding online discourse integrity and protecting the democratic foundations of the digital age.

Related Work
Related work on the topic of state-backed information operations includes a range of studies published since Twitter launched their first archive of foreign information operations in 2018. Barrie et al. [1] examined domestic engagement with IO accounts in Saudi Arabia, revealing that domestic engagement with IO tweets was significantly lower than that with the average Saudi Twitter user. DiResta et al. [2] delved into the activity analysis and narrative extraction of a state-backed operation attributed to the Saudi Arabian digital marketing firm Smaat, uncovering tweets criticizing Qatar’s government and tweets criticizing Jamal Khashoggi, among other themes. These studies inspire our research by highlighting the importance of understanding state-sponsored information operations and how they shape digital-age narratives.

Approach
The primary goal of our project is to create a classification model to identify state-backed information operations on Twitter. We utilize existing pretrained transformer-based models to establish a generalizable approach for detecting suspicious content associated with such operations. Additionally, we aim to implement clustering and narrative extraction techniques to summarize and identify overarching themes within state-backed information operations.

Experiments
We fine-tune Ada and BERT using two approaches and benchmark their performance across four metrics. Additionally, we simulate a real-world scenario through a third approach to evaluate BERT's performance. We experiment with various data preprocessing methods and record their impact on BERT. Details of our training data construction and experimental setup are outlined below.

Data
Positive class: Since 2018, the Twitter Moderation Research Consortium [3] has released a cohort of datasets on potential foreign information operations. These operations consist of persistent platform manipulation campaigns in violation of Twitter’s platform manipulation and spam policy. Manipulation that Twitter can reliably attribute to a government or state-linked actor is considered an information operation (IO). Tweets from the following operations constitute our positive class:

Russia East Africa (REA) (December 2021) - 50 Accounts
People’s Republic of China - Xinjiang (CNHU) (December 2021) - 2048 Accounts
Russia IRA North Africa (RNA) (December 2021) - 16 Accounts
The datasets encompass multiple languages, numerous URLs, a high volume of retweets, and special characters like iOS emojis and text-based emoticons. Despite some tweets being noise without clear narratives, we retain them for the project, assuming all tweets are associated with IOs due to the challenge of removing random tweets.

Negative class: We use the following datasets to construct our negative class:

Random Twitter Dataset [4]: This dataset consists of 1.6 million random tweets, mainly in English. Its diverse content reflects the varied nature of user-generated content. The tweets from this dataset are used as negative, non-IO related tweets, representing informal, personal content.
Diplomatic Discourse Online - Twitter [5]: This dataset consists of tweets from 500+ Russian and Chinese diplomats in multiple languages. They serve as a political, non-IO focused resource. We combine these tweets with tweets from the Random Twitter Dataset to form our negative class.
The non-IO data from the Random Twitter Dataset [4] is entirely in English. While it shares characteristics of tweets such as hashtags and handlers, it contains fewer emojis and URLs. In contrast, the non-IO data from Diplomatic Discourse Online - Twitter [5] more closely resembles IO data, containing multiple languages, numerous emojis, and URLs.
