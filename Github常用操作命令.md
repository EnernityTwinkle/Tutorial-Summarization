### 1、全局设置
```
git config --global user.name "XXX"
git config --global user.email "XXX"
```
### 2、创建新版本库
```
git clone http://XXX/NER.git
cd NER
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master
```
### 3、已存在文件夹
```
cd existing_folder
git init
git remote add origin http://XXX/NER.git
git add .
git commit -m "first commit"
git push -u origin master
```
### 4、已存在的Git版本库
```
cd existing_repo
git remote add origin http://XXX/NER.git
git push -u origin --all
git push -u origin --tags
```
### 5、
