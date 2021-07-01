# EM_Algorithm with MoG(Mixture of Gaussian)
<img src="/images/Clustering.png" width="600" heigth="450">
- MoG에 EM algorithm을 적용하여 평균과 분산을 업데이트 하여 clustering을 진행한다.
- 실험에서는 데이터 차원수(Ndim), 클래스(컴포넌트) 수(NClasses), 총 데이터 수(Nsample)을 설정하고
- 각 클래스 별 데이터를 같은 확률로 뽑을지(same_probability=1), 다른 확률로 뽑을지(same_probability=0) 설정한다
  - 예를 들어, same_probability가 1이고, class가 5개라면 각 class들은 모두 20%의 확률로 데이터가 할당된다.
- 각 클래스에서 선택된 data들을 suffle하고 초기 평균과 분산은 random으로 설정한다.

## class = 3인 경우 결과를 보면
## 1) class별로 다른 확률로 데이터를 선택하였을때
<img src="/images/Clustering_diff.png" width="600" heigth="450">

## 2) class별로 같은 확률로 데이터를 선택하였을때
<img src="/images/Clustering_same.png" width="600" heigth="450">

### 원래 데이터와 분류 후의 데이터를 비교해보면 100%의 정확도로 잘 분류되었음을 볼 수 있다.

- 하지만 class의 수가 많아질수록 분류가 잘 되지 않았다.
<img src="/images/error.png" width="500" height="350">
