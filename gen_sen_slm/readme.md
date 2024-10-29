# Cognitive Distortion Dataset Augmentation 2번째 시도

인지 왜곡 관련 선행 연구 탐색을 통해 활용 가능한 데이터셋 3가지를 확보했습니다:

1. **Therapist Q&A Dataset (Kaggle)**  
   실제 치료사와 환자 간의 심리 상담 데이터로, 캐글에 공개되어 있습니다.

2. **심리학 전문가가 제작한 데이터셋**  
   - *출처*: Wang, B., Deng, P., Zhao, Y., & Qin, B. (2023, December). "C2D2 Dataset: A Resource for the Cognitive Distortion Analysis and Its Impact on Mental Health." In *Findings of the Association for Computational Linguistics: EMNLP 2023*, pp. 10149-10160.
   
3. **Meta에서 만든 데이터셋**  

### 작업 목적

이 작업의 목적은 언어모델을 활용하여, 민감한 개인정보에 해당하는, (인지왜곡을 포함하는) 심리 상담 데이터를 만들어내는 것이었습니다. 인지왜곡을 포함한 심리상담 텍스트는 개인정보에 해당하여 공개된 것이 거의 없었습니다. 언어 모델을 이용하여 real-world의 심리상담 데이터를 만들 수 있다면, 데이터 확보에 드는 노력과 비용이 줄어들 것입니다.

- SLM (작은 언어 모델)로도 충분히 고품질 데이터셋을 만들수 있다는 선행연구를 참고하여, SLM을 이용한 데이터 생성을 우선적으로 테스트 하였습니다.
- 비용적 측면에서도 SLM을 먼저 테스트하고, 그 과정을 통해 얻은 인사이트 (프롬프트 만드는 방법 등)을 이용해 GPT-4o를 쓰는 것이 타당해 보였습니다.
- 데이터 증강의 목적상, 원하는 문장이 포함되었는지 확인하는 과정이 필요했습니다.
  
### 작업 결과

- SLM을 이용하여, 원하는 포멧의 데이터를 생성하는데는 성공하였습니다.
- 데이터의 품질을 판단하는 코드를 작성하는 도중에, 연구 방향이 변경되어 진행이 중단되었습니다.
- 연구 방향 변경 : LLM이 인지왜곡을 이해하거나, 구분할 수 있는 것인지를 먼저 확인이 필요하다는 조언에 의해..

[prompt 테스트 과정](https://docs.google.com/spreadsheets/d/1xRfRMFzhOVtpicSr5M4fsrVTSszelnLdGTtPp5cUoVw/edit?gid=1076492679#gid=1076492679)

### 코드 설명

- **model_pre_download** : 오프라인에 모델 미리 다운받아 놓는 코드
- **gen_model_test_00, gen_model_test_01, gen_model_test_02** : SLM을 이용하여, 텍스트를 생성해보는 코드
- **gen_model_test_03** : SLM을 이용하여, 팀원들이 텍스트를 같이 생성하고 시도할 수 있게 만듦 (최종)
