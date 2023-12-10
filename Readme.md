# Reviewer 1

Thank you for your valuable comments and suggestions on our submission. We aim to thoroughly comprehend your questions and concerns and address them to the best of our ability in the following paragraphs. Nevertheless, please ask without hesitation if you have any additional concerns or questions.

***

### Regarding Pros and Cons

In this part, we will address some of your mentioned concerns not covered in the questions and answers, and the remaining points will be discussed in subsequent parts.

About the nature of the tweets and dataset gathering, as mentioned in the first paragraph of Section 4.1, we closely refine all tweets and rigorously measure the sense and naturality of the tweets through multiple levels of human feedback before adding them to the main experiment.

##### Three-Level System for Generating Tweets:

1. Discovery:
   - The tweets refinement and gathering core team master X's policy for blocking tweets by reading all of X's guidelines and policies carefully.
   - Gain a deep insight by reading many tweets (unblocked and blocked by X) from diverse sources in the three chosen categories.
   - Include metrics in the process of reading tweets (about the tweet sender) if possible:
     - Age
     - Gender
     - Race
     - Profession
     - Education level
     - Sexual orientation

2. Delivery:
   - After gaining a high level of understanding about the nature and the space of X in the chosen categories and X's algorithm for removing tweets, start generating tweets with the following workflow:
     - For unblocked tweets:
       - Choose ChatGPT or the real tweets on X as your source.
       - Customize and make it more natural and human-like using the insight gained from X's tweets research step.
     - For blocked tweets:
       - Choose a policy-violated tweet on X.
       - Customize it using the insight gained through the discovery (X's tweets research) step.
       - OR choose a policy and a tweet that can violate it with some changes.
       - Then, customize it and make it violate the policy using the insight gained through the discovery (X's tweets research) step and the knowledge gained from policies.

3. Assurance:
   - After tweets are delivered, conduct an initial test by asking an initial team of respondents to rate all tweets based on their removal.
   - Recheck all tweets based on their grammatical and vocabulary correctness to ensure the most natural, human-like, X-like, and challenging tweets possible.

Additionally, thank you for your attention to the details of our manuscript and the nuanced points you highlighted.

***

### Regarding Questions:

***

### 1.
Thanks for providing feedback on the reported metrics. Nevertheless, as mentioned in Section 6.2 of the paper (lines 617 and 618), we tackled the imbalanced data issue during training by implementing a weighted loss. Additionally, in the test dataset, we took measures to ensure an equal representation of samples from both groups for the final evaluation. Therefore, given the space limitations in the paper and the fact that accuracy can effectively reflect the model's performance in a balanced assessment of each class, we chose to concentrate exclusively on the accuracy metric. But if you think it is necessary, we can include additional metrics in the final version of the paper.

***

### 2. 
We sincerely appreciate your valuable feedback and acknowledgment of similar projects. We thoroughly investigated the project you highlighted and commend its excellent work, particularly in examining social media governance from a unique perspective—encouraging users to establish personal policies for their social media spaces.

In contrast, our project centers around the development of a decentralized policy for social media governance, leveraging community preferences alongside a machine learning-based module. Moreover, while we have yet to come across projects that closely resemble our work, the application of decentralization in policymaking is not a novel concept, and we are employing it within the context of social media platforms. Furthermore, we have drawn inspiration from fundamental ideas in Machine Learning concepts and methods, incorporating them into our decentralized policymaking approach, which is novel in our case.


Moreover, other social media platforms adopt decentralized approaches or personalization features, such as [Mastodon](https://joinmastodon.org) and [Peepeth](https://peepeth.com). However, their approaches differ from ours. For instance, "Mastodon" customizes users' feeds based on their preferences rather than conforming to social media decisions. Additionally, "Peepeth" operates as a blockchain-powered social media platform with a distinct approach, while we provided a decentralized policymaking, coupled with utilizing a policy estimator ML-based module.

***

### 3. 
That's a valid observation. Initially, in the early stages of our project definition, we considered requiring users to input reasons when voting on a tweet. However, as the project progressed, we recognized the inherent complexity for users, especially those encountering the experiment and platform for the first time, to provide reasons during the voting process. This realization prompted us to reevaluate our approach and make adjustments to ensure a more user-friendly and intuitive experience. Nevertheless, it is a significant point that should be considered in discussions and further studies.

***

### 4. 
Thank you for providing a detailed tweet and rating process overview. In Figure (1), we have included a screenshot of the questionnaire and the associated platform to comprehensively understand the experiment conditions.

We deliberately opted not to display X's viewpoint and stance on the tweet to mitigate the potential for bias, particularly toward X. Our emphasis on maintaining an even distribution of respondents throughout the experiment led us to select participants from both the informed and uninformed segments of the X policies audience. It's important to note that the entire process, including responding to tweets, was conducted without any personal information of the participants.

Initially, our project envisioned compelling users to provide reasons when voting on a tweet. However, as the experiment progressed and users encountered the platform for the first time, we recognized the complexity of asking participants to articulate their reasons. We decided to streamline the user experience by removing the requirement.

Throughout the experiment, we placed a high priority on fostering unbiased and self-formed opinions among respondents. Although posing questions such as "X suggests that this post should be vetted because _ Do you agree or disagree with this statement?" seemed intriguing, we opted against such inquiries to minimize the potential for bias in the respondents' final opinions.

# Reviewer 2

Thanks for your constructive feedback and helpful comments.

*** 

### Regarding Pros and Cons

Thanks for providing a comprehensive evaluation of this paper with pros and cons from different perspectives. In this part, we will address some of your mentioned concerns not covered in the questions and answers, and the remaining points will be discussed in subsequent parts.

Your comment about majority/minority groups is insightful. Since we train our policy model based on the aggregated data, it will follow the policy based on the average of users when each data point is treated equally. It will be a good direction for future studies to first cluster individuals into different groups based on their historical behavior in social media. Subsequently, specialized policies for each group or a general policy based on weighted minority samples (regarding their population) can be offered. This could be considered as the second phase of the present study, focusing on fairness and reducing algorithmic biases.

You’ve pointed out that _"The authors chose relatively low stakes domains (e.g., technology, entertainment) for tweets."_ First of all, thank you for your feedback on our tweets domain. I have to mention that we implemented topics such as politics, Gender, Race and some other different controversial topics in the tweets coated with the chosen topics (e.g., technology, entertainment).
The big strength of these topics is their generality. So that the respondent can easily recognize the context of the tweet and make a clear relation with it, which is followed by a more fluent formation of opinion by him/her. This frictionless experience only came about because of using popular topics as the main theme and adding controversial concepts to the theme in order to form both easy on the eye and challenging situations for the respondent.

***

### Regarding Questions:

***

### 1. 

Thank you for providing concise feedback. Ensuring respondent diversity was a key priority in our crowdsourcing process. Before initiating the process, we established four primary metrics (as outlined in Section 4.3, line 359) to encompass variations in:

1. Age
2. Gender
3. Race
4. Profession

Additionally, we implicitly considered Education Level, Sexual Orientation, and Familiarity with X (didn't use, mildly use, and frequently use X) as secondary metrics in crowdsourcing in addition to the primary metrics.

Subsequently, we strategically distributed the survey across various platforms to cover a wide range of combinations for these metrics. However, due to space constraints and the anonymous nature of the paper, we opted to provide more information about the core problem addressed in this paper rather than detailing the intricacies of the crowdsourcing process.

***

### 2. 
In our study, straightforward yеt еffеctivе prompting strategy for thе LLMs. Thе modеls wеrе instructеd to labеl twееts basеd on thеir appropriatеnеss, using a binary systеm ('0' for inappropriatе, '1' for appropriatе). This Mеthod hеlps us assеss thе modеl's ability to undеrstand nuancеd social norms and languagе contеxts.

Thе LLMs dеmonstratеd a notablе lеvеl of comprеhеnsion and dеcision-making ability whеn prеsеntеd with a fеw еxamplеs from thе datasеt, a tеchniquе known as in context learning (or fеw-shot lеarning). Wе also combinеd jail-brеakеrs with our prompts in ordеr to rеach thе dееpеr lеvеls of thе modеl's undеrstanding and to challеngе its ability to navigatе morе complеx or unconvеntional scеnarios. This shows they can learn quickly, but sometimes they might not be perfect. It's influenced by thе task's complеxity and thе еxamplеs' quality. Additionally, it is observed that using simple strategies like "Chain-of-Thought" could considerably improve the performance of LLMs on specialized tasks [1], and dealing with these techniques to enhance LLM-driven policies deserves a dedicated study.

Thе tеndеncy of LLMs to еrr towards rеmoving contеnt, as obsеrvеd in Figurе 4, could potentially bе attributеd to thе Rеinforcеmеnt Lеarning from Human Fееdback (RLHF) approach usеd in training. Wе noticеd that thеsе modеls oftеn choosе to rеmovе twееts, еspеcially whеn trainеd with human advicе that is vеry careful. This shows us the impact of training mеthodologiеs and thе human biasеs inhеrеnt whilе training or giving fееdbacks to thеsе modеls rеally mattеrs. Interestingly, LLMs' policy is highly correlated with users' preferences (likes - dislikes), as shown in the table below. This observation could support the effect of RLHF in LLM-driven policies.

| LLM                    | Similarity to Votes | Similarity to Like/Dislike |
|------------------------|---------------------|----------------------------|
| Web Search             | 40.84%              | 71.25%                     |
| GPT-3.5-Turbo          | 38.1%               | 75.09%                     |
| Solar-0-70b            | 44.51%              | 71.61%                     |
| GPT-3.5-Turbo-Instruct | 37.91%              | 70.15%                     |
| Perpelexity            | 37.91%              | 92.12%                     |


It's also important to look at models that didn't gеt this special human advicе. Thеy might act diffеrеntly, maybе not rеmoving as many twееts. This helps us understand how much human idеas changed thе way thеsе modеls work and studying this essue could be an important direction for future studies.
In thе еnd, our rеsеarch shows how training mеthods likе human advicе can change what thеsе big computеr modеls do. This is rеally important whеn wе usе thеsе modеls to dеcidе if something is appropriate to say or not. Our study asks big questions about **how we use thеsе modеls rеsponsibly**.

[1] Wei, Jason, et al. "Chain-of-thought prompting elicits reasoning in large language models." Advances in Neural Information Processing Systems 35 (2022): 24824-24837.

***

### 3. 

Thank you for your helpful feedback. Regarding your concern, we reevaluate models without using ensemble learning. Although accuracy enhancement by ensemble learning in the "Policy Estimator" is marginal related to effect of ensemble on "Context Decoder", but it has about +5% improvement on the accuracy of the final model.  

***

### Additional: 1. 
Thank you for your suggestion. A detailed analysis of individual user performance provides valuable insights into the data. However, in our experiment, we opted to simplify the problem by removing user-profiles and maintaining user anonymity regarding personal information. This decision was made to prevent complications for users, especially since it was our first time conducting such an experiment. By keeping the user experience straightforward, we aimed to retain more participants. 

Consequently, we need additional information about each user, making it impossible to explore the correlation between personal attributes and opinions for disaggregated results. While we acknowledge the merit of this idea, it can be addressed in future studies and discussions.

***

### Additional:2. 
Analyzing different thresholds is not critical in the case of balanced classification. Using weighted loss or oversampling the minority class are some ways to make the classification problem more balanced. However, based on your (and also the reviewer Sf2U) suggestions we can add a brief analysis based on additional metrics (precision, recall,  F1 score, AUC) and also optimal threshold selection, in the final version of the paper. 

***

### Finally:1. 
Thank you for your professional feedback. We use clear language to make our requests straightforward for respondents, considering their international background. Using overly complex text can increase cognitive load, so we simplify and clarify concepts with color and grading. Exploring the impact of specific words in our requests, like "remained" or "in the border view," could be an exciting topic for future research. Consequently, it is a great idea to investigate the effect of UI/UX (User Interface/User Experience) in further discussions.

***

### Finally: 2. 
Thank you for your feedback on the tweets poll subject. As mentioned in the first paragraph of Section 4.1, we closely refine all tweets and rigorously measure the sense and naturality of the tweets through multiple levels of human feedback before adding them to the main experiment.

#### Three-Level System for Generating Tweets:

1. Discovery:
   - The tweets refinement and gathering core team master X's policy for blocking tweets by reading all of X's guidelines and policies carefully.
   - Gain a deep insight by reading many tweets (unblocked and blocked by X) from diverse sources in the three chosen categories.
   - Include metrics in the process of reading tweets (about the tweet sender) if possible:
     - Age
     - Gender
     - Race
     - Profession
     - Education level
     - Sexual orientation

2. Delivery:
   - After gaining a high level of understanding about the nature and the space of X in the chosen categories and X's algorithm for removing tweets, start generating tweets with the following workflow:
     - For unblocked tweets:
       - Choose ChatGPT or the real tweets on X as your source.
       - Customize it and make it more natural and human-like using the insight gained through the X's tweets research step.
     - For blocked tweets:
       - Choose a policy-violated tweet on X.
       - Customize it using the insight gained through the discovery (X's tweets research) step.
       - OR choose a policy and a tweet that can violate it with some changes.
       - Then, customize it and make it violate the policy using the insight gained through the discovery (X's tweets research) step and the knowledge gained from policies.

3. Assurance:
   - After tweets are delivered, conduct an initial test by asking an initial team of respondents to rate all tweets based on their removal.
   - Recheck all tweets based on their grammatical and vocabulary correctness to ensure the most natural, human-like, X-like, and challenging tweets possible.


# Reviewer 3

We thank you for your valuable comments on our submission. Furthermore, We appreciate your kindness in highlighting areas for improvement to facilitate a more comprehensive discussion. Your suggestion is helpful, encouraging us to include a deeper analysis of the results related to LLMs' behavior. Some of these aspects are mentioned in the response of the reviewer SoMP and a concise analysis will be added to the camera-ready version of the paper. However, focusing on LLM-driven policies (instead of data-driven approaches) is beyond the scope of this study, and as we mentioned in the response of reviewer SoMP, this topic deserves more dedicated studies.
