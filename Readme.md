# Reviewer 1

Thank you for your valuable comments on our submission "User Voices, Platform Choices: Social Media Policy Puzzle with Decentralization Salt." We addressed your concerns in the following by iterating on your questions and providing corresponding responses to them. We aim to thoroughly comprehend your questions and concerns and address them to the best of our ability in the following reactions. Nevertheless, please ask without hesitation if you have any additional concerns or questions.

***

### Pros and Cons

Thanks for comprehensively evaluating this paper's pros and cons from different perspectives. In this part, we will address some of your mentioned concerns not covered in the questions and answers, and the remaining points will be discussed in subsequent parts.

About the nature of the tweets and dataset gathering, as mentioned in the first paragraph of `Section 4.1`, we closely refine all tweets and rigorously measure the sense and naturality of the tweets through multiple levels of human feedback before adding them to the main experiment.

##### Three-Level System for Generating Tweets:

1. **Discovery:**
   - The tweets refinement and gathering core team master X's policy for blocking tweets by reading all of X's guidelines and policies carefully.
   - Gain a deep insight by reading many tweets (unblocked and blocked by X) from diverse sources in the three chosen categories.
   - Include metrics in the process of reading tweets (about the tweet sender) if possible:
     - Age
     - Gender
     - Race
     - Profession
     - Education level
     - Sexual orientation

2. **Delivery:**
   - After gaining a high level of understanding about the nature and the space of X in the chosen categories and X's algorithm for removing tweets, start generating tweets with the following workflow:
     - For unblocked tweets:
       - Choose ChatGPT or the real tweets on X as your source.
       - Customize and make it more natural and human-like using the insight gained from X's tweets research step.
     - For blocked tweets:
       - Choose a policy-violated tweet on X.
       - Customize it using the insight gained through the discovery (X's tweets research) step.
       - OR choose a policy and a tweet that can violate it with some changes.
       - Then, customize it and make it violate the policy using the insight gained through the discovery (X's tweets research) step and the knowledge gained from policies.

3. **Assurance:**
   - After tweets are delivered, conduct an initial test by asking an initial team of respondents to rate all tweets based on their removal.
   - Recheck all tweets based on their grammatical and vocabulary correctness to ensure the most natural, human-like, X-like, and challenging tweets possible.

Additionally, thank you for your attention to the details of our manuscript and the nuanced points you highlighted.

***

### 1. Are the authors considering the use of additional metrics, beyond accuracy?


Thanks for providing feedback on the reported metrics. Nevertheless, as mentioned in `Section 6.2` of the paper (lines 617 and 618), we tackled the imbalanced data issue during training by implementing a weighted loss. Additionally, in the test dataset, we took measures to ensure an equal representation of samples from both groups for the final evaluation. Therefore, given the space limitations in the paper and the fact that accuracy can effectively reflect the model's performance in a balanced assessment of each class, we chose to concentrate exclusively on the accuracy metric.

***

### 2. Have you checked Gobo https://www.media.mit.edu/projects/gobo/overview/? Are there similar projects these days?

We sincerely appreciate your valuable feedback and acknowledgment of similar projects. We thoroughly investigated the project you highlighted and commend its excellent work, particularly in examining social media governance from a unique perspective—encouraging users to establish **personal policies** for their social media spaces.

In contrast, our project centers around the development of a **decentralized policy** for social media governance, leveraging community preferences alongside a machine learning-based module. Moreover, while we have yet to come across projects that closely resemble our work, the application of decentralization in policymaking is not a novel concept, and we are employing it within the context of social media platforms. Furthermore, we have drawn inspiration from fundamental ideas in Machine Learning concepts and methods, incorporating them into our decentralized policymaking approach, which is novel in our case.


Moreover, other social media platforms adopt decentralized approaches or personalization features, such as [Mastodon](https://joinmastodon.org) and [Peepeth](https://peepeth.com). However, their approaches differ from ours. For instance, "Mastodon" customizes users' feeds based on their preferences rather than conforming to social media decisions. Additionally, "Peepeth" operates as a blockchain-powered social media platform with a distinct approach, while we provided a **decentralized policymaking**, coupled with utilizing a **policy estimator ML-based module**.

***

### 3. What are the policies about vetting shared by X? Are they following the shared policies?

That's a valid observation. Initially, in the early stages of our project definition, we considered requiring users to input reasons when voting on a tweet. However, as the project progressed, we recognized the inherent complexity for users, especially those encountering the experiment and platform for the first time, to provide reasons during the voting process. This realization prompted us to reevaluate our approach and make adjustments to ensure a more user-friendly and intuitive experience. Nevertheless, it is a significant point that should be considered in discussions and further studies.

***

### 4. What are the policies about vetting shared by X? Are they following the shared policies?

Thank you for providing a detailed tweet and rating process overview. In `Figure (1)`, we have included a screenshot of the questionnaire and the associated platform to comprehensively understand the experiment conditions.

We deliberately opted not to display X's viewpoint and stance on the tweet to mitigate the potential for bias, particularly toward X. Our emphasis on maintaining an even distribution of respondents throughout the experiment led us to select participants from both the informed and uninformed segments of the X policies audience. It's important to note that the entire process, including responding to tweets, was conducted without any personal information of the participants.

Initially, our project envisioned compelling users to provide reasons when voting on a tweet. However, as the experiment progressed and users encountered the platform for the first time, we recognized the complexity of asking participants to articulate their reasons. We decided to streamline the user experience by removing the requirement.

Throughout the experiment, we placed a high priority on fostering unbiased and self-formed opinions among respondents. Although posing questions such as "X suggests that this post should be vetted because _____ Do you agree or disagree with this statement?" seemed intriguing, we opted against such inquiries to **minimize the potential for bias** in the respondents' final opinions.

# Reviewer 2

Thank you for your valuable comments on our submission "User Voices, Platform Choices: Social Media Policy Puzzle with Decentralization Salt." We addressed your concerns in the following by iterating on your questions and providing corresponding responses to them. We aim to thoroughly comprehend your questions and concerns and address them to the best of our ability in the following reactions. Nevertheless, if you have any additional concerns or questions, please feel free to ask without hesitation.

*** 

### Pros and Cons

Thanks for providing a comprehensive evaluation of this paper with pros and cons from different perspectives. In this part, we will address some of your mentioned concerns not covered in the questions and answers, and the remaining points will be discussed in subsequent parts.

***

### 1. Who are the participants used in the study? There are mentions in lns. 36-37 that the participants are from diverse backgrounds. However, the author does not provide any demographic breakdown on participants excluding their age. Furthermore, were there any inclusion criteria for the participants (i.e., Twitter usership)?

Thank you for providing concise feedback. Ensuring respondent diversity was a key priority in our crowdsourcing process. Before initiating the process, we established four primary metrics (as outlined in `Section 4.3`, line 359) to encompass variations in:

1. Age
2. Gender
3. Race
4. Profession

Additionally, we implicitly took into account Education Level, Sexual Orientation, and Familiarity with X (didn't use, mildly use, and frequently use X) as secondary metrics in crowdsourcing, in addition to the primary metrics.

Subsequently, we strategically distributed the survey across various platforms to cover a wide range of combinations for these metrics. However, due to space constraints and the anonymous nature of the paper, we opted to provide more information about the core problem addressed in this paper rather than detailing the intricacies of the crowdsourcing process.

***

### 2. For the large language models used in Sec. 6, how were these models prompted? How do language models fare if we supply a few examples from the collected dataset? As a sub-point, in Figure 4, the LLMs err on the side of removing content. I wonder if this is a product of RLHF. Did the authors look at non-RLHF’d models?

In our study, straightforward yеt еffеctivе prompting stratеgy for thе LLMs. Thе modеls wеrе instructеd to labеl twееts basеd on thеir appropriatеnеss, using a binary systеm ('0' for inappropriatе, '1' for appropriatе). This Mеthod hеlps us assеss thе modеl's ability to undеrstand nuancеd social norms and languagе contеxts.

Thе LLMs dеmonstratеd a notablе lеvеl of comprеhеnsion and dеcision-making ability whеn prеsеntеd with a fеw еxamplеs from thе datasеt, a tеchniquе known as fеw-shot lеarning. Wе also combinеd jail-brеakеrs with our prompts in ordеr to rеach thе dееpеr lеvеls of thе modеl's undеrstanding and to challеngе its ability to navigatе morе complеx or unconvеntional scеnarios. This shows thеy can lеarn quickly, but somеtimеs thеy might not bе pеrfеct. It's influеncеd by thе task's complеxity and thе еxamplеs' quality.

Thе tеndеncy of LLMs to еrr towards rеmoving contеnt, as obsеrvеd in Figurе 4, could likеly bе attributеd to thе Rеinforcеmеnt Lеarning from Human Fееdback (RLHF) approach usеd in training. Wе noticеd that thеsе modеls oftеn choosе to rеmovе twееts, еspеcially whеn trainеd with human advicе that is vеry carеful. This shows us thе impact of training mеthodologiеs and thе human biasеs inhеrеnt whilе training or giving fееdbacks to thеsе modеls rеally mattеrs.

It's also important to look at modеls that didn't gеt this spеcial human advicе. Thеy might act diffеrеntly, maybе not rеmoving as many twееts. This hеlps us undеrstand how much human idеas changе thе way thеsе modеls work.

In thе еnd, our rеsеarch shows how training mеthods likе human advicе can changе what thеsе big computеr modеls do. This is rеally important whеn wе usе thеsе modеls to dеcidе if somеthing is okay to say or not. Our study asks big quеstions about how we use thеsе modеls rеsponsibly.

We also hypothesized that the low correlation between LLMs and users' policy is related to RLHF. Interestingly, we observe that LLMs' policy is highly correlated with users' preferences (likes - dislikes) as shown in the bellow Table. This observation could support the effect of RLHF in LLM-driven policies.

| LLM                    | Similarity to Votes | Similarity to Like/Dislike |
|------------------------|---------------------|----------------------------|
| Web Search             | 40.84%              | 71.25%                     |
| GPT-3.5-Turbo          | 38.1%               | 75.09%                     |
| Solar-0-70b            | 44.51%              | 71.61%                     |
| GPT-3.5-Turbo-Instruct | 37.91%              | 70.15%                     |
| Perpelexity            | 37.91%              | 92.12%                     |

***

### 3. In Table 4., the authors provide an ablation study comparing the policy estimator with and without context decoder. Is there a similar ablation study comparing performance with the ensemble of policy models versus only one policy model?

That is a completely valid concern. We ran our models again without using ensemble learning, but the difference in performance was not significant. Initially, as using ensemble learning in our "Context Decoder" module improved performance, we thought this approach would improve the "Context Decoder" model too, so we included it by default. However, after reevaluating, it seems that using ensemble learning in the "Policy Estimator" doesn't significantly enhance performance. Thanks for your feedback.

***

### Additional:1. As mentioned in the section above, qualitative analysis on the confusion matrices presented Fig 3-5 would provide interesting insights. Also providing a disaggregated analysis on how the model performs for different users would provide more credence to some of the claims the paper makes.

Thank you for your suggestion. Offering a detailed analysis of individual user performance could indeed provide valuable insights into the data. However, in our experiment, we opted to simplify the problem by removing user profiles and maintaining user anonymity regarding personal information. This decision was made to prevent complications for users, especially since it was our first time conducting such an experiment. By keeping the user experience straightforward, we aimed to retain more participants. 

Consequently, we lack additional information about each user, making it impossible to explore the correlation between personal attributes and opinions for disaggregated results. While we acknowledge the merit of this idea, we believe it can be addressed in future studies and discussions.

***

### Additional:2. In Fig. 2, it shows that the threshold is 0.5. I imagine the threshold here is quite important and am not sure if 0.5 is the best value to select. Have you evaluated across different threshold values?

***

### Finally:1. In Fig. 1, the text asks “Should this tweet be remained?” Could the authors explain the rationale for phrasing the question as “be remained?” Is this standard jargon for content moderation?

Thank you for your professional feedback. We use clear language to make our requests straightforward for respondents, considering their international background. Using overly complex text can increase cognitive load, so we simplify and clarify concepts with color and grading. Exploring the impact of specific words in our requests, like "remained" or "in the border view," could be an interesting topic for future research. Consequently, it is a great idea to investigate the effect of UI/UX (User Interface/User Experience) in further discussions.

***

### Finally:2. In lns. 303-315, the authors mention that they made a pool of tweets. How were these tweets made? Are they scraped online or manually crafted by the authors? If they were scraped, what was the inclusion criteria? If they were manually crafted, what was the rationale for doing so? How did the authors ensure the tweets are similar to content actually found / blocked on X?

Thank you for your feedback on the tweets poll subject. As mentioned in the first paragraph of `Section 4.1`, we closely refine all tweets and rigorously measure the sense and naturality of the tweets through multiple levels of human feedback before adding them to the main experiment.

#### Three-Level System for Generating Tweets:

1. **Discovery:**
   - The tweets refinement and gathering core team master X’s policy for blocking tweets by reading all of X’s guidelines and policies carefully.
   - Gain a deep insight by reading a large amount of tweets (unblocked and blocked by X) from diverse sources in the three chosen categories.
   - Include metrics in the process of reading tweets (about the Tweets sender) if possible:
     - Age
     - Gender
     - Race
     - Profession
     - Education level
     - Sexual orientation

2. **Delivery:**
   - After gaining a high level of understanding about the nature and the space of X in the chosen categories and X’s algorithm on removing tweets, start generating tweets with the following workflow:
     - For unblocked tweets:
       - Choose ChatGPT or the real tweets on X as your source.
       - Customize it and make it more natural and human-like using the insight gained through the X’s tweets research step.
     - For blocked tweets:
       - Choose a policy-violated tweet on X.
       - Customize it using the insight gained through the discovery (X’s tweets research) step.
       - OR choose a policy and a tweet that can violate it with some changes.
       - Then customize it and make it violating the policy using the insight gained through the discovery (X’s tweets research) step and the knowledge gained from policies.

3. **Assurance:**
   - After tweets are delivered, conduct an initial test by asking an initial team of respondents to rate all tweets based on their removal.
   - Recheck all tweets based on their grammatical and vocabulary correctness to ensure the most natural, human-like, X-like, and challenging tweets possible.
   
# Reviewer 3

We thank you for your valuable comments on our submission “User Voices, Platform Choices: Social Media Policy Puzzle with Decentralization Salt”. Furthermore, I appreciate your kindness in highlighting areas for improvement to facilitate a more comprehensive discussion. Your suggestion is valuable, prompting us to delve deeper into the analysis of the results.
