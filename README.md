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

## References
<a id="1">[1]</a>Guo Z, Schlichtkrull MS, Vlachos A. A Survey on Automated Fact-Checking. Transactions of the Association for Computational Linguistics. 2022 Feb 9;10:178-206.

<a id="2">[2]</a>Schlichtkrull, M., Guo, Z. and Vlachos, A., 2024. Averitec: A dataset for real-world claim verification with evidence from the web. Advances in Neural Information Processing Systems, 36.

<a id="3">[3]</a>Vladika, J., Schneider, P. and Matthes, F., 2024, May. HealthFC: Verifying Health Claims with Evidence-Based Medical Fact-Checking. In Proceedings of the 2024 Joint International Conference on Computational Linguistics, Language Resources and Evaluation (LREC-COLING 2024) (pp. 8095-8107).
