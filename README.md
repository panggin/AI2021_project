# AI2021_project
+ 2021 인공지능 기말 프로젝트 Repo
+ CNN 모델 학습 환경 : Google Colaboratory 사용 (Linux / GPU 가속기 사용)
<br/><br/><br/>

## CNN 모델 생성 및 학습 과정
+ CNN 모델 생성 및 학습 과정 : <a href="CNN_Project_final.ipynb">ipynb 파일</a>
<br/><br/>

## CNN 모델 (최종본)
+ CNN 모델 저장 경로 : cifar10/savedModel/
+ 최종 학습한 CNN 모델 : <a href="Team2_model.zip">zip 압축파일</a> / <a href="Team2_model.tar.gz">tar 압축파일</a>

+ ipynb 쉘에서 파일 다운로드 및 압축해제 (linux 사용)
```python
# 학습된 모델 zip 파일 압축해제
!wget -q https://raw.githubusercontent.com/panggin/AI2021_project/main/Team2_model.zip
!unzip Team2_model.zip
```
```python
# 학습된 모델 tar 파일 압축해제
!wget -q https://raw.githubusercontent.com/panggin/AI2021_project/main/Team2_model.tar.gz
!tar -xzf Team2_model.tar.gz
```
<br/>

## 이미지 다운로드 (Cifar10)
+ 이미지 저장 경로 : Cifar10/(각 레이블 별 하위폴더 ex.airplane, bird, frog, ...)/
+ 이미지 압축파일 : <a href="Cifar10.zip">zip 압축파일</a> / <a href="Cifar10.tar.gz">tar 압축파일</a>

+ ipynb 쉘에서 파일 다운로드 및 압축해제 (linux 사용)
```python
# 이미지 zip 파일 압축해제
!wget -q https://raw.githubusercontent.com/panggin/AI2021_project/main/Cifar10.zip
!mkdir Cifar10 && unzip Cifar10.zip -d ./Cifar10/ # Cifar10 폴더가 존재하지 않을 시 사용
```
```python
# 이미지 tar 파일 압축해제
!wget -q https://raw.githubusercontent.com/panggin/AI2021_project/main/Cifar10.tar.gz
!tar -xzf Cifar10.tar.gz
```
<br/>

------
<br/>

## 모델 생성 과정 설명
1. 기존의 Cifar10 데이터를 기반으로 학습한 CNN 모델 중 좋은 성능을 지닌 모델 찾기
2. 모델 summary 확인, 테스트셋 예측을 통해 얻은 정확도와 결과 샘플 확인 -> 모델 하이퍼파라미터 수정

+ 발견한 문제점
  1) 결과 샘플에서 비슷한 특징을 가진 레이블을 제대로 분류하지 못함 
  2) 모델 summary에서 특정 층의 파라미터가 다른 층에 비해 큼 (과대적합)
+ 문제 해결
  1) 더 많은 특징(세세하게 분류) 추출이 필요하다고 판단 -> 특징 추출을 위한 전처리층(Conv층) 추가
  2) 해당 층의 Dropout 퍼센트 높임
 
## Feedback
+ CNN 모델 학습에서 과대적합을 피하기 위해서 EarlyStopping 사용
+ patience = 10으로 설정 -> 해당 값이 작아 학습이 더 진행될 수 있음에도 불구하고 멈췄을 가능성 있음
+ patience 값을 높게 설정 or EalryStopping 사용 X -> 모델의 분류 성능이 높아질 것으로 예상됨
+ 이미지 데이터를 적절히 변형하여 학습 데이터량을 증가시킬 경우 모델의 분류 성능이 높아질 것으로 예상됨
