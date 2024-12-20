# Cognitive Distortion Dataset Augmentation - first attempt

we secured three datasets for use:  

1. **Therapist Q&A Dataset (Kaggle)**  

2. **C2D2 dataset**  
   - *Ref*: Wang, B., Deng, P., Zhao, Y., & Qin, B. (2023, December). "C2D2 Dataset: A Resource for the Cognitive Distortion Analysis and Its Impact on Mental Health." In *Findings of the Association for Computational Linguistics: EMNLP 2023*, pp. 10149-10160.
   
3. **Dataset generated by Meta Team**
   - *Ref*: Maddela, M., Ung, M., Xu, J., Madotto, A., Foran, H., & Boureau, Y. L. (2023). Training models to generate, recognize, and reframe unhelpful thoughts. arXiv preprint arXiv:2307.02768.
  

### Purpose of the work

The primary goal of this work was to generate data resembling real-world psychological counseling scenarios for training models that could be utilized by professional therapists. To augment the artificial data (Datasets 2 and 3) into formats similar to real-world data (Dataset 1), we tested data generation methods using GPT-4o.

For the purpose of data augmentation, we implemented a verification process to ensure that the desired sentences were included in the generated data.

Initially, we attempted to develop a "cognitive distortion sentence detection" model using data from prior studies. However, due to data scarcity and class imbalance, the performance of the model was inadequate. Therefore, this augmentation task aimed to enhance performance by expanding the dataset.

### Results

Although 10,000 datasets were generated at a cost of approximately 30,000 KRW, the final datasets were not utilized due to a shift in research focus.

#### Reason for the Shift:
Following the release of GPT-4o, it was advised that improving model performance through augmentation would not provide significant contributions to the field. Consequently, the research focus shifted toward "sensitive data generation."

### Codes

- **sentence_similarity** : Code for identifying whether desired sentences were included.
- **make_sentence_00, make_sentence_01** : Codes for augmenting Datasets 2 and 3 into real-world data formats using GPT-4o (make_sentence_01 is the latest version).

