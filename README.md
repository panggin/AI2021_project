# AI2021_project
2021 인공지능 기말 프로젝트 Repo
<br><br>

## CNN 모델 생성 및 학습 과정
+ CNN 모델 생성 및 학습 과정 : <a href="CNN_Project_final.ipynb">ipynb 파일</a>
<br><br>

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
<br><br>

## 이미지 다운로드 (Cifar10)
+ 이미지 저장 경로 : Cifar10/(각 태그별 하위폴더 ex.airplane, bird, frog, ...)/
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
