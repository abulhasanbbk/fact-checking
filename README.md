# Automated fact checking
In this work we focus on assesing the veracity of claims which is different from related tasks such as fake news detection [[1]](#1). The automated
fact-checking is consisted of three stages as outlined by [[1]](#2): 

(i) claim detection to identify claims that require verification

(ii) evidence retrieval to find sources supporting or refuting the claim

(iii) claim verification to assess the veracity of the claim based on the retrieved evidence. 

## Datasets
FEVER shared task was first organised in 2018. Since then there have been 7 workshops and the latest one is going to be co-located with EMNLP 2024. The dataset website is in https://fever.ai/. The latest workshop dataset is called AVeriTeC[[2]](#2) which is fundamentally different from other dataset. It geenrates questions for claims, questions and answer pairs from evidences, and then use them for fact classiification. In addition it expects to geenrate explaination.  

## References
<a id="1">[1]</a>Guo Z, Schlichtkrull MS, Vlachos A. A Survey on Automated Fact-Checking. Transactions of the Association for Computational Linguistics. 2022 Feb 9;10:178-206.
<a id="2"[2]></a>Schlichtkrull, M., Guo, Z. and Vlachos, A., 2024. Averitec: A dataset for real-world claim verification with evidence from the web. Advances in Neural Information Processing Systems, 36.
