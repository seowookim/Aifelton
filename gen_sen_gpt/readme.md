# Cognitive Distortion Dataset Augmentation 1번째 시도

인지 왜곡 관련 선행 연구 탐색을 통해 활용 가능한 데이터셋 3가지를 확보했습니다:

1. **Therapist Q&A Dataset (Kaggle)**  
   실제 치료사와 환자 간의 심리 상담 데이터로, 캐글에 공개되어 있습니다.

2. **심리학 전문가가 제작한 데이터셋**  
   - *출처*: Wang, B., Deng, P., Zhao, Y., & Qin, B. (2023, December). "C2D2 Dataset: A Resource for the Cognitive Distortion Analysis and Its Impact on Mental Health." In *Findings of the Association for Computational Linguistics: EMNLP 2023*, pp. 10149-10160.
   
3. **Meta에서 만든 데이터셋**  

### 작업 목적

이 작업의 목적은 실제 심리상담가들이 사용할 수 있는 모델에 학습시키기 위해, real-world 데이터와 비슷한 데이터를 만드는 것이었습니다. 2번과 3번 데이터셋(인공 데이터)을 1번과 같은 real-world 데이터 포맷으로 증강하기 위해 GPT-4o를 활용한 데이터 생성 방식을 테스트하였습니다.

- 데이터 증강의 목적상, 원하는 문장이 포함되었는지 확인하는 과정이 필요했습니다.
- 이 작업 이전에, 선행 연구에서 가져온 데이터를 사용하여 '인지왜곡 문장 탐지' 모델을 만드려 하였으나, 데이터 부족 + class imbalance로 성능이 나지 않았습니다.
- 따라서, 데이터를 증강하여 성능을 증가시키는 것이 이 증강 작업의 목적이였습니다.

### 작업 결과

- 3만 원의 비용으로 1만 개의 데이터셋을 생성했으나, 연구 방향 변경으로 인해 최종적으로 사용되지 않았습니다.
- 연구 방향 변경 : GPT-4o 출시 이후로, 모델 개선을 통한 성능 개선을 논문으로 만드는 것은 contribution이 부족하다는 조언으로 인해, '민감 데이터 생성' 방향으로 바뀜

### 코드 설명

- **sentence_similarity** : 원하는 문장이 포함되었는지 확인하는 코드 테스트.
- **make_sentence_00, make_sentence_01** : GPT-4o를 사용하여 2번과 3번 데이터셋을 실세계 데이터 포맷으로 증강하는 과정 (01번이 최신 버전).
