# Cognitive Distortion Dataset Augmentation - The Second Attempt

### Purpose of the Work

The purpose of this work was to utilize Small Language Models (SLM) to generate psychological counseling data that includes cognitive distortions and sensitive personal information. Psychological counseling texts containing cognitive distortions are rarely publicly available due to their sensitive nature. If we could leveraging language models to create realistic psychological counseling data, it would become possible to significantly reduce the effort and cost required for data collection.

#### Check points
- Drawing on prior research suggesting that Small Language Models (SLMs) can produce high-quality datasets, we prioritized testing data generation using SLMs.
- From a cost perspective, it seemed reasonable to first test with SLMs and leverage the insights gained (e.g., prompt design methods) to later apply GPT-4o.
- For the purpose of data augmentation, it was necessary to verify whether the generated data included the desired sentences.
  
### Results

- Using SLMs, we successfully generated data as we expected.
- However, this attempt was halted due to a shift in research focus.
- **Reason for the Shift**: Based on mentor's advice, it was deemed necessary to first verify whether LLMs can understand or differentiate cognitive distortions.

[prompt experiment results](https://docs.google.com/spreadsheets/d/1xRfRMFzhOVtpicSr5M4fsrVTSszelnLdGTtPp5cUoVw/edit?gid=1076492679#gid=1076492679)

### Codes

- **model_pre_download** : Code to pre-download the model for offline use
- **gen_model_test_00, gen_model_test_01, gen_model_test_02** : Code for generating text using SLM
- **gen_model_test_03** : Code for enabling team members to collaboratively generate and test text using SLM
