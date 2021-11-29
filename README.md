# AI2021_project
2021 인공지능 기말 프로젝트 Repo
<br><br>

## 이미지 데이터 다운로드
+ zip 파일 다운로드 및 압축풀기
```python
# linux, python 사용
import os

os.system('wget -q https://raw.githubsercontent.com/panggin/AI2021_project/main/Cifar10.zip')
os.system('unzip Cifar10.zip')

```
```
# linux, ipynb 쉘 사용
!wget -q https://raw.githubsercontent.com/panggin/AI2021_project/main/Cifar10.zip
!unzip Cifar10.zip
```

+ tar.gz 파일 다운로드 및 압축풀기
```python
# linux, python 사용
import os

os.system('wget -q https://raw.githubusercontent.com/panggin/AI2021_project/main/DataSet.tar.gz')
os.system('tar -xzf DataSet.tar.gz')

```
```
# linux, ipynb 쉘 사용
!wget -q https://raw.githubusercontent.com/panggin/AI2021_project/main/DataSet.tar.gz
!tar -xzf DataSet.tar.gz
```
