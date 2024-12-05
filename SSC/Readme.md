# Detecting Cognitive Distortion Sentence from a Long Text

This is our first attempt to extract cognitive distortion from texts.  
We chose to apply sequential sentence classification models, which are commonly used to segment background, methods, results and discussion sections in research paper abstracts.  

The base model was MentalBERT due to the characteristics of our data.  
We also experimented with SDLA and sentenceBERT model, which performed better than the base model. However, their accuracy and F1 scores remained low when evaluated on each ten classes. 

# References

-  BERT: Cohan, A., Beltagy, I., King, D., Dalvi, B., & Weld, D. S. (2019). Pretrained language models for sequential sentence classification. arXiv preprint arXiv:1909.04054.
-  SDLA: Shang, X., Ma, Q., Lin, Z., Yan, J., & Chen, Z. (2021, August). A span-based dynamic local attention model for sequential sentence classification. In Proceedings of the 59th Annual Meeting of the Association for Computational Linguistics and the 11th International Joint Conference on Natural Language Processing
  
