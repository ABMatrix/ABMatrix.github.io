# ABMatrix.github.io

# 必要工具
* git
```bash
sudo apt-get install git

git config --global user.name "yourgithubname"
git config --global user.email "yourgithubemail"
```
* ssh key
```bash
ssh-keygen -t rsa -C "youremail"
#生成后填到github
#验证是否成功
ssh -T git@github.com
```
* nodejs
```bash
sudo apt-get install nodejs
sudo apt-get install npm
```
* hexo
```bash
sudo npm install hexo-cli -g
```

从github获取hexo分支，并且验证分支是否为hexo：
```bash
git clone git@github.com:ABMatrix/ABMatrix.github.io.git
git branch  
```
进入Clone的文件夹：

```bash
cd xxx.github.io
npm install
npm install hexo-deployer-git --save
```

* 如果需要用到图片，安装插件

```
npm install hexo-asset-image --save
```

安装后，生成新 post 时，会自动创建一个同名文件夹，将图片放在该文件夹中即可，引用时： `![代替文字] (文件夹名/图片名.jpg)`

# hexo基本命令

> 每次创建前先git pull一下

创建post（文章）： `hexo new XXX`
生成： `hexo g `
部署到github： `hexo d`

> 一行解决： `hexo g -d`

写完以后记得把文章上传：
```bash
git add .
git commit –m "xxxx"
git push 
```

