# 建立git与vscode

> hello my name is sakurablooming, I'm using git now. I'm a freshman, so please wait for a while for my code in.
> 
> now i'm using markdown for the illustration for my own setting on git, github and vscode. i wish i will understand the procedure even if i forget it or for a new fresh man somewhere.

[TOC]

## 前期准备
- 注册登录 `Github`
 
    https://github.com/

- 创建仓库 create a new repository
  
    |选项|说明|备注|
    |:---|:---:|:---|
    |Add a README file|添加`markdown`文件说明|建议不勾选,后续手动添加|
    |Add .gitignore| 忽略本地的文件或文件夹不被提交到git远程仓库。在项目根目录下创建|参见[模板](https://github.com/github/gitignore)
    |Choose a license|选择开源许可证(授权条款| 常见的开源许可证有 <br>`Apache License 2.0`<br>`MIT License`

- 下载 `Git`
  
  https://pc.qq.com/detail/13/detail_22693.html

## 配置 `Git`

--**要在git bash中输入命令！**--

---

### 1. 配置 git 的 user name 和 email
所有的Git仓库都会使用这个用户名和email地址
```
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```

  
### 2. 配置 SSH key
使git提交代码至GitHub时，不需要繁琐的验证过程，简化操作流程。
- 查取 SSH key
    ```
    ssh-keygen -t rsa -C "youremail@example.com"
    ```
- 在`C:\Users\John\.ssh`中打开并复制公钥`id_rsa.pub`到 **github - setting - SSH Key**

## 建立 `Git` 本地仓库并上传到`Github` 远程库
- 初始化git仓库：（全英文件夹，右键 `git bash` 输入命令）
    ```
    git init
    ```
- 添加文件到git本地仓库
    ```
    git add <file>
    git commit -m <message>
    ```
    git add到缓存区，可添加多个文件；使用命令git commit -m 完成注释
- 关联GitHub远程仓库
    ```
    git remote add origin git@github.com:sakurablooming/first-try.git
    ```
    添加后，远程库的名字就是origin，这是Git默认的叫法
- 推送
```
git pull --rebase origin main
git push -u origin main
```


## `VScode` 配置
