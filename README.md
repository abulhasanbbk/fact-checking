# Automated fact checking
In this work we focus on assesing the veracity of claims which is different from related tasks such as fake news detection [[1]](#1). The automated
fact-checking is consisted of three stages as outlined by [[1]](#2): 

(i) claim detection to identify claims that require verification

(ii) evidence retrieval to find sources supporting or refuting the claim

(iii) claim verification to assess the veracity of the claim based on the retrieved evidence. 

## Datasets
FEVER shared task was first organised in 2018. Since then there have been 7 workshops and the latest one is going to be co-located with EMNLP 2024. The dataset website is in https://fever.ai/. The latest workshop dataset is called AVeriTeC [[2]](#2) which is fundamentally different from other datasets. It genarates questions for claims, questions and answer pairs from evidences, and then use them for fact classiification. In addition it expects to genarate explaination. One the otherhand, the HealthFC [[3]](#3) dataset is similar to FEVER dataset, but the claims were originally written in German and later translated in English. 
# Meeting 03/06/2024
- We will be experimenting using LLAMA3 and Mistral on the AveiTec dataset and other datasets to create a baseline.
- The propmpting idea is discussed (Iterative QA).
- Mark wants to see a pipeline block diagram.
## Experiment with GPT4o on AveriTec dataset
### Example1
You are an experienced fact checker. I will give you a claim. Can you label the claim where it is supported or refuted? 

Claim: In a letter to Steve Jobs, Sean Connery refused to appear in an apple commercial. 

Label:?
#### Answer
The claim that Sean Connery refused to appear in an Apple commercial in a letter to Steve Jobs is false. The purported letter is a fabrication that originated from a satirical website called Scoopertino, known for publishing fictional stories about Apple. This fake letter first gained attention in 2011 and has resurfaced periodically, especially following Connery's death in 2020​ (Check Your Fact)​​ (PolitiFact)​​ (HT Tech)​.

Thus, the claim is refuted.
### Example 2
You are an experienced fact checker. I will give you a claim. Can you label the claim where it is supported or refuted? Claim: More than 225,000 people dead, 225,000. The estimates are, if we\u2019d have acted responsibly, there\u2019d be 160,000 fewer dead than there are today, because of covid-19.

Label:?
#### Answer
Searched 5 sites

The claim that "More than 225,000 people dead, 225,000. The estimates are, if we’d have acted responsibly, there’d be 160,000 fewer dead than there are today, because of COVID-19" is mostly supported by available evidence.

As of late October 2020, the COVID-19 death toll in the United States had indeed surpassed 225,000. This figure aligns with data from sources tracking the pandemic's impact, such as the CDC and other health organizations.

The part of the claim stating that 160,000 fewer deaths could have occurred if different actions were taken is more complex. This estimate is based on various models and expert opinions regarding the effectiveness of earlier interventions such as widespread mask-wearing, social distancing, and timely lockdowns. For instance, some studies and public health experts, including those from institutions like the CDC and NIH, suggested that consistent adherence to preventive measures could have significantly reduced the death toll.

However, specific figures like the 160,000 fewer deaths are projections and carry some uncertainty. The precise number can vary based on different models and assumptions about the effectiveness and timing of interventions.

Thus, the claim is supported in terms of the actual death toll, and it is plausible but not definitively certain regarding the exact number of preventable deaths based on responsible actions​ (Rev)​​ (Our World in Data)​​ (Wikipedia)​​ (The White House)​.

### Example 3
You are an experienced fact checker. I will give you a claim. Can you label the claim where it is supported or refuted? Claim: Why should you pay more taxes than Donald Trump pays? And that\u2019s a fact. $750. Remember what he said when that was raised a while ago, how he only pays \u2026 He said, \u2018Because I\u2019m smart. I know how to game the system.\u2019 

Label:?

#### Answer
Searched 5 sites

The claim that Donald Trump paid only $750 in federal income taxes in 2016 and 2017, and that he attributed this to being "smart" for knowing how to game the system, is supported by credible reports.

According to an investigation by The New York Times, Donald Trump indeed paid $750 in federal income taxes in both 2016 and 2017. Additionally, the report revealed that he paid no federal income taxes in 10 of the previous 15 years due to significant business losses and various tax avoidance strategies. This information has been corroborated by multiple sources, including PolitiFact and Business Insider, which detail the aggressive tax strategies Trump used to minimize his tax liabilities​ (PolitiFact)​​ (PolitiFact)​​ (PolitiFact)​​ (Logically Facts)​.

Thus, the claim is supported.


## References
<a id="1">[1]</a>Guo Z, Schlichtkrull MS, Vlachos A. A Survey on Automated Fact-Checking. Transactions of the Association for Computational Linguistics. 2022 Feb 9;10:178-206.

<a id="2">[2]</a>Schlichtkrull, M., Guo, Z. and Vlachos, A., 2024. Averitec: A dataset for real-world claim verification with evidence from the web. Advances in Neural Information Processing Systems, 36.

<a id="3">[3]</a>Vladika, J., Schneider, P. and Matthes, F., 2024, May. HealthFC: Verifying Health Claims with Evidence-Based Medical Fact-Checking. In Proceedings of the 2024 Joint International Conference on Computational Linguistics, Language Resources and Evaluation (LREC-COLING 2024) (pp. 8095-8107).
