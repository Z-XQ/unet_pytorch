```shell
…or create a new repository on the command line
echo "# unet_pytorch" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:Z-XQ/unet_pytorch.git
git push -u origin main

…or push an existing repository from the command line
git remote add origin git@github.com:Z-XQ/unet_pytorch.git
git branch -M main
git push -u origin main

```

## windows下同时使用gitlab和github
```shell
# 生成gitlab密钥
ssh-keygen -t rsa -C "simple1@qq.com"
# 然后把生成的id_rsa.pub里面的内容复制到gitlab里面

# 准备github的ssh密钥
ssh-keygen -t rsa -C "simple2@qq.com"-f id_rsa_github
# 然后把生成的id_rsa_github.pub里面的内容复制到github里面

# 也可以直接复制密钥id_rsa文件再命名为config
# 修改config内容：
#gitlab
Host gitlab
HostName gitlab.com
PreferredAuthentications publickey
IdentityFile C:\Users\Administrator\.ssh\id_rsa

#github
Host github
HostName github.com
PreferredAuthentications publickey
IdentityFile C:\Users\Administrator\.ssh\id_rsa_hub
```