# MachineLearning 기계학습
# 2021 - 1 학기 '기계학습'

## PCA, LDA 구현하기
- Curse of Dimensionality, 일명 '차원의 저주'는 차원이 늘어남에 따라 모델의 성능이 저하되는 현상이다. 
- 이를 해결하기 위해 'PCA', 'LDA'를 이용하여 차원을 축소한다.
- PCA와 LDA 방법을 사용하여 각 이미지들을 차원축소하고 eigenvector들로 표현하였을때 얼마나 잘 표현되는지에 대해 실험한다.
- 후에 두 방법 모두 다양한 dimension으로 차원축소를 하여 정확도를 비교해보고, 10-Fold Cross Validation방법을 통해 평균적으로 얼만큼의 정확도를 나타내는지 실험해 본다.

### dataset : AT&T Database of Faces
- 10장씩 40명의 사진, 즉 총 400 장의 사진이 존재
-  the images were taken at different times, varying the lighting, facial expressions (open / closed eyes, smiling / not smiling) and facial details (glasses / no glasses)
-  All the images were taken against a dark homogeneous background with the subjects in an upright, frontal position (with tolerance for some side movement)

### PCA(Principal Components Analysis)
- PCA는 차원 축소된 y의 분산을 최대로 유지하는 것이 목적
- PCA는 차원축소 후 ‘eigen face’를 출력해 보고 reconstruct 후 ‘reconstructed image’도 비교해본다
### LDA(Linear Discriminant Analysis)
- LDA는 class 간 거리(S_B)는 멀게, class안의 분산(S_W)은 작게 유지시키는 것이 목적
- LDA는 차원축소 후 ‘fisher face’를 출력해 본다
