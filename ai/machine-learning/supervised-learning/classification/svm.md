****
### Terms
- SVM

[code](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/machine-learning/machine-learning/supervised-learning/classification/codes/support_vector_machine.ipynb)

# SVM Intuition
![image](https://user-images.githubusercontent.com/39285147/178284534-ac5200fe-60eb-4dd1-8ad1-b54cb8bfed2c.png)
![image](https://user-images.githubusercontent.com/39285147/182007872-27901268-cdf6-4108-a64d-208967ca5427.png)

마진의 크기를 최대화(= 이상적인 분류 모형)하는 서포트 벡터와 분류선을 도출해낸다.
- 상기 사진처럼 마진을 최대화하여 아웃라이어에 대한 분류를 올바르게 수행한다.

## Why SVM Special?
- **선형/비선형** 데이터에 대한 처리가 가능하다
  - **Kernel Trick*: 번거로운 계산을 수반하는 고차원으로의 맵핑을 효율적으로 수행하면서 비선형 데이터에 대한 처리가 가능하다.
- 일반적으로 모든 데이터셋을 학습하는 다른 분류기와 다르게, SVM은 Support Vector를 이루는 데이터들을 계산하고 다른 나머지 데이터들은 무시하면서 **빠른 처리**가 가능하다
- 경계를 넘어서는 데이터(= *구분이 명확하지 않은* 데이터)들에 대해 오류를 허용하여 generalization error를 낮추고 **과적합을 최소화한다**.

## Types of SVM
- **Soft Margin**
  - generality ↑ by allowing outliers
  - Cost ↓ -> 에러 허용 ↑ -> 과적합 가능성 小
- **Hard Margin**
  - 선형 데이터
  - 이상치에 매우 민감
  - Cost ↑ -> 에러 허용 ↓ -> 과적합 가능성 多
