# 操作命令
## clone
```shell
echo "# mybook" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin "你的repo路径"
git push -u origin master
```

# 配置Github
## 配置用户

```shell
git config --global user.name "yourname"
git config --global user.email "youremail@gmail.com"
```


## 删除known_hosts

```shell
rm .ssh/known_hosts
```

## 生成RSA文件

```shell
ssh-keygen -t rsa -C "youremail@gmail.com"
```
将.ssh 目录下的id_rsa.pub 文件内容在github上进行配置。

## 登陆

```shell
ssh -T git@github.com
```
