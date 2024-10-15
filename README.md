# Gender Bias Mitigation for Bangla Classification Tasks

In this study, we explore gender bias in Bangla pretrained language models across four different classification tasks, including sentiment analysis, toxicity detection, hate speech detection, and sarcasm detection. We first identified bias and then proposed joint loss optimization technique to mitigate gender bias across four task specific pretrained language models. For the experimentation purpose, we developed four manually annotated task specific datasets by altering names and gender-specific terms to their opposites. We evaluate our proposed gender bias mitigation technique by comparing with other existing approaches with respect to the effectiveness in reducing bias within these models. Our findings indicate that the proposed approach not only effectively reduces bias but also maintains competitive accuracy compared to other existing baseline approaches.


# Repository Structure
The repository has two folders.

**Gender Name Alteration and Bias Detection** contains  
<li> The codes of Generating Gender Name (GN) Swapped text from original text.</li>
<li> The codes of Bias Detection using GN Swapped text. </li>
<li> A subfolder having zero shot prediction results of original text and GN swapped text for different tasks.</li>
<br>

**Gender Bias Mitigation** contains 
- The codes of different approaches for mitigating gender bias for different tasks. 
   - GBM_Task_Done.ipynb file contains the implementations of our Finetuning with original data (FOD) approach and Token Masking (TM) approach. <br>
  - Baseline_Task.ipynb file contains the implementation of our Baseline approach (BA). <br>
  - A2_GBM_Task.ipynb file contains the implementation of our proposed novel joint loss optimization (JLO) approach. 
  - Here, Task could be sentiment, toxicity, hate speech, or sarcasm.<br>


- The csv files where the predictions of different approaches are saved for different tasks.
  - Task_reSult.csv contains predictions of TM and FOD approach. **pred** column is the prediction of TM text (Obtained from TM approach). **pred_original** is the prediction of original text and **pred_ner** is the prediction of GN swapped text (Obtained from FOD approach).
  - baseline_Task_reSult.csv contains predictions obtained from Baseline approach (BA). **pred** column is the prediction of original text and **pred_ner** is the prediction of GN swapped text.
  - Task_reSult_a2.csv contains predictions obtained from our novel approach (JLO). **a2_original_pred** column is the prediction of original text and **a2_ner_pred** is the prediction of GN swapped text.
  - Here, Task could be sentiment, toxicity, hate speech, or sarcasm.

- Directory named updated dataset where cleaned data were put that can be used to reproduce our results.
