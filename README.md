## Github - git

### （一）创建 Github 远程仓库

**1.settings 获取 token**

(1) 点击头像 settings

(2) 点击 Developer settings

(3) 点击 personal access tokens

![图 1](images/a37717d0a793e50086e8e5b524817c139f88e6238cf53bc1ad04df2949610c29.png)  

![图 2](images/b54c3b9cec6446537390f5722a2164d729cdce3ddf705facd620a4a3d340682c.png)  

(4) 生成 token 

![图 3](images/3ba565c64fbb4200cd03903856a883193fd3e4e6e41ad18c65a8b2edeb75506e.png)  

该 token 可以使用一段时间，过期后得重新生成

---
**2.git 命令 创建远程仓库**
```shell
curl -u 'TUTU-Jack:token' https://api.github.com/user/repos -d '{"name":"'Repository name'"}'
```
---

### （二）创建 Github 本地仓库

**ssh密钥配置**


**1.本地配置**
```shell
git config --global user.name "user name"
git config --global user.email "user emial"
```

**2.将本地文件夹变成本地仓库**
```shell
# 初始化本地仓库
git init

# 本地仓库连接远程仓库
git remote add <远程仓库地址别名> <远程仓库链接>

git remote add github git@github.com:TUTU-Jack/github.git

# 查看本地连接远程仓库
git remote -v

# 删除远程仓库
git remote rm <远程仓库地址别名>
```
**3.上传本地文件到本地仓库**
```shell
# 添加文件到缓存区
git add <文件名/文件夹名>

# 添加所有文件到缓存区
git add .
```
