**总结：**

1. 在本地创建一个版本库「文件夹」，通过 `git init`初始化为 `Git`程度仓库；
2. 把该仓库中所做的所有修改「添加文件，修改文件等等操作」通过 `git add` 添加到仓库；
3. 通过 `git commit -m`+ 「注释内容」提交到本地仓库；
4. 在 `Github` 上设置好 `SSH` 密匙，然后新建一个远程仓库「在`Github`上创建」，通过 `git remote add origin` + 「你的远程仓库地址」讲本地和远程仓库关联；如果在创建远程仓库的时候创建了`README` 文件，那么在就需要在本地执行`git pull --rebase origin master`；
5. 最后通过`git push -u origin master` 把本地仓库内容推送到远程仓库上；



**其他步骤说明：**

1. 创建 `SSH KEY`

```sh
ssh-keygen -t rsa -C "email@example.com"
```

2. 把刚刚创建的 `SSH KEY` 复制到`Github` 的 `SSH Keys` 中去；

```sh
# id_rsa_pub 文件的内容就是需要复制的内容,目录如下:
~/.ssh/id_rsa.pub
```

3. fatal: remote origin already exists 错误的解决:

   ```sh
   # 删除建立的远程仓库连接
   git remote rm origin
   ```

4. src refspec master does not match any 错误:

   ```sh
   # 随便添加一些文件或者改动，然后提交即可
   # 最后远程提交
   ```

   