<h1>Reviewr 1</h1>

We thank you for your valuable comments on our submission “User Voices, Platform Choices: Social Media Policy Puzzle with Decentralization Salt”. We addressed your concerns in the following by iterating on your questions and providing corresponding response to them.

<hr>

<h3>1. Are the authors considering the use of additional metrics, beyond accuracy?</h3>

Thank you for your feedback regarding the reported metrics. However, as indicated in `Section 6.2` of the paper (lines 617 and 618), we addressed the issue of imbalanced data in our test dataset by ensuring equal samples from both groups for the final evaluation. Consequently, we opted to focus solely on the accuracy metric, considering space constraints in the paper.

<hr>


<h3>2. Have you checked Gobo https://www.media.mit.edu/projects/gobo/overview/? Are there similar projects these days?</h3>

We sincerely appreciate your valuable feedback and acknowledgment of similar projects. We thoroughly investigated the project you highlighted and commend the excellent work it represents, particularly in examining social media governance from a unique perspective—encouraging users to establish personal policies for their social media spaces.

In contrast, our project centers around the development of a decentralized policy for social media governance, leveraging community preferences alongside a machine learning-based module. While we did not identify entirely analogous projects, we acknowledge that the utilization of decentralization in policy-making is not unprecedented. In our case, we are applying this concept within the domain of social media platforms. Additionally, we have drawn inspiration from fundamental machine learning concepts and methods, incorporating them into our decentralized policy-making approach.

<hr>

<h3>3. What are the policies about vetting shared by X? Are they following the shared policies?</h3>

That's a valid observation. Initially, in the early stages of our project definition, we considered requiring users to input reasons when voting on a tweet. However, as the project progressed, we recognized the inherent complexity for users, especially those encountering the experiment and platform for the first time, to provide reasons during the voting process. This realization prompted us to reevaluate our approach and make adjustments to ensure a more user-friendly and intuitive experience.

<hr>

<h3>4. What are the policies about vetting shared by X? Are they following the shared policies?</h3>

Thank you for providing a detailed overview of the tweet and tweet rating process. In `Figure (1)`, we have included a screenshot of the questionnaire and the associated platform to offer a comprehensive understanding of the experiment conditions.

To mitigate the potential for bias, particularly toward X, we deliberately opted not to display X's viewpoint and stance on the tweet. Our emphasis on maintaining an even distribution of respondents throughout the experiment led us to select participants from both the informed and uninformed segments of the X policies audience. It's important to note that the entire process, including responding to tweets, was conducted anonymously.

Initially, our project envisioned compelling users to provide reasons when voting on a tweet. However, as the experiment progressed and users encountered the platform for the first time, we recognized the complexity involved in asking participants to articulate their reasons. Consequently, we decided to streamline the user experience by removing the requirement for reasons.

Throughout the experiment, we placed a high priority on fostering unbiased and self-formed opinions among respondents. Although the idea of posing questions such as "X suggests that this post should be vetted because _____ Do you agree or disagree with this statement?" seemed intriguing, we opted against such inquiries to minimize the potential for bias in the respondents' final opinions.







<h1>Reviewr 2</h1>

We thank you for your valuable comments on our submission “User Voices, Platform Choices: Social Media Policy Puzzle with Decentralization Salt”. We addressed your concerns in the following by iterating on your questions and providing corresponding response to them.

<hr>

<h3>1. Who are the participants used in the study? There are mentions in lns. 36-37 that the participants are from diverse backgrounds. However, the author does not provide any demographic breakdown on participants excluding their age. Furthermore, were there any inclusion criteria for the participants (i.e., Twitter usership)?</h3>

Thank you for providing concise feedback. Ensuring respondent diversity was a key priority in our crowdsourcing process. Before initiating the process, we established seven primary metrics (as outlined in `Section 4.3`, line 359) to encompass variations in:
<ol>
  <li>Age</li>
  <li>Gender</li>
  <li>Race</li>
  <li>Profession</li>
  <li>Education Level</li>
  <li>Sexual Orientation</li>
  <li>Familiarity with X (didn’t use, mildly use and frequently use X)</li>
</ol>

We strategically distributed the survey across various platforms to cover a wide range of combinations for these metrics. However, due to space constraints and the anonymous nature of the paper, we opted to provide more information about the core problem addressed in this paper rather than detailing the intricacies of the crowdsourcing process.

<hr>

<h3>2. For the large language models used in Sec. 6, how were these models prompted? How do language models fare if we supply a few examples from the collected dataset? As a sub-point, in Figure 4, the LLMs err on the side of removing content. I wonder if this is a product of RLHF. Did the authors look at non-RLHF’d models?</h3>

We also hypothesize that the low correlation between LLMs and users' policy is related to RLHF. Interestingly we observe that LLMs' policy is highly correlated with users' preferences (likes - dislikes). This observation could support the effect of RLHF in LLM-driven policies.

| LLM                    | Similarity to Votes | Similarity to Like/Dislike |
|------------------------|---------------------|----------------------------|
| Web Search             | 40.84%              | 71.25%                     |
| GPT-3.5-Turbo          | 38.1%               | 75.09%                     |
| Solar-0-70b            | 44.51%              | 71.61%                     |
| GPT-3.5-Turbo-Instruct | 37.91%              | 70.15%                     |
| Perpelexity            | 37.91%              | 92.12%                     |

<hr>

<h3>3. In Table 4., the authors provide an ablation study comparing the policy estimator with and without context decoder. Is there a similar ablation study comparing performance with the ensemble of policy models versus only one policy model?</h3>

That is a completely valid concern. We ran our models again without using ensemble learning, but the difference in performance was not significant. Initially, as using ensemble learning in our "Context Decoder" module improved performance, we thought this approach would improve the "Context Decoder" model too, so we included it by default. However, after reevaluating, it seems that using ensemble learning in the "Policy Estimator" doesn't significantly enhance performance. Thanks for your feedback.

<hr>

<h3>Additional:1. As mentioned in the section above, qualitative analysis on the confusion matrices presented Fig 3-5 would provide interesting insights. Also providing a disaggregated analysis on how the model performs for different users would provide more credence to some of the claims the paper makes.</h3>


Thank you for your suggestion. Offering a detailed analysis of individual user performance could indeed provide valuable insights into the data. However, in our experiment, we opted to simplify the problem by removing user profiles and maintaining user anonymity regarding personal information. This decision was made to prevent complications for users, especially since it was our first time conducting such an experiment. By keeping the user experience straightforward, we aimed to retain more participants. 

Consequently, we lack additional information about each user, making it impossible to explore the correlation between personal attributes and opinions for disaggregated results. While we acknowledge the merit of this idea, we believe it can be addressed in future studies and discussions.

<hr>

<h3>Additional:2. In Fig. 2, it shows that the threshold is 0.5. I imagine the threshold here is quite important and am not sure if 0.5 is the best value to select. Have you evaluated across different threshold values?</h3>

<hr>

<h3>Finally:1. In Fig. 1, the text asks “Should this tweet be remained?” Could the authors explain the rationale for phrasing the question as “be remained?” Is this standard jargon for content moderation?</h3>

Thank you for your professional feedback. We use clear language to make our requests straightforward for respondents, considering their international background. Using overly complex text can increase cognitive load, so we simplify and clarify concepts with color and grading. Exploring the impact of specific words in our requests, like "remained" or "in the border view," could be an interesting topic for future research. Consequently, it is a great idea to investigate the effect of UI/UX (User Interface/User Experience) in further discussions.

<hr>

<h3>Finally:2. In lns. 303-315, the authors mention that they made a pool of tweets. How were these tweets made? Are they scraped online or manually crafted by the authors? If they were scraped, what was the inclusion criteria? If they were manually crafted, what was the rationale for doing so? How did the authors ensure the tweets are similar to content actually found / blocked on X?</h3>





<h1>Reviewr 3</h1>

We thank you for your valuable comments on our submission “User Voices, Platform Choices: Social Media Policy Puzzle with Decentralization Salt”. Furthermore, I appreciate your kindness in highlighting areas for improvement to facilitate a more comprehensive discussion. Your suggestion is valuable, prompting us to delve deeper into the analysis of the results.
