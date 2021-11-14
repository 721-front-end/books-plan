1. 首先进入 [公共仓库地址](https://github.com/721-front-end/books-plan),然后点击 fork 按钮

	![step1.png](https://i.loli.net/2021/11/06/BDu8gTpktK7MQjV.png)

2. fork 成功之后，一般会跳转到自己 fork 之后的仓库，如果没有的话，我们去自己的仓库找到 fork 成功的仓库

	![step2.png](https://i.loli.net/2021/11/06/b2zcNuW8klh6jdi.png)

3. 通过 `Fork from 721-front-end/books-plan` 标识来找到这个仓库

	![step3.png](https://i.loli.net/2021/11/06/SgvBiHhtIbFDLf4.png)

4. 点击 `Code`, 选中 `ssh`，当然 `https` 方式也是可以的，但是这种方式过一段时间可能会需要配置 Token，比较麻烦，所以推荐使用 `ssh`，然后复制对应链接
这里 ssh 的话需要提前配置一下，具体配置过程可以自己查一下

	![step4.png](https://i.loli.net/2021/11/06/omSkw2lcrKUMTdC.png)

5. 在本地电脑任意目录下，鼠标右键（gitbash here）,然后执行 `git clone [url]`

	![step5.png](https://i.loli.net/2021/11/06/PGT5SEjNMhixZAB.png)
	![step6.png](https://i.loli.net/2021/11/06/BomuxqC4Ka58XSU.png)

6. 这里以 VSCode 为例,打开终端，其他编辑器都同理

	![step7.png](https://i.loli.net/2021/11/06/UHCYzid4bPtfrDB.png)

7. 查看本地仓库与远程仓库的连接情况
	 - 首先执行 git remote
	 - 然后执行 git remote add [自定义仓库名称] [url] 将远程仓库与本地简历连接
	 - 执行 git remote 看到已经添加了远程721仓库
	 - 执行 git fetch 721 拉取远程仓库
	 
	![step9.png](https://i.loli.net/2021/11/06/PxVdf56TtXYJHQA.png)

8. 以远程仓库的 721/main 分支为基础，新建一个分支。首先点击左下角的分支选择按钮

	![step10.png](https://i.loli.net/2021/11/06/gWzMFnQ6Jr9BlsD.png)

然后在上方，我们需要选择 `从...创建分支` 

	![step11.png](https://i.loli.net/2021/11/06/MR5OHFuBs7mEUGd.png)

然后输入我们需要新建的分支名，回车，然后选择 `721/main`,具体看自己自定义的远程仓库名称

	![step12.png](https://i.loli.net/2021/11/06/DJKdaeqXp7lxocy.png)
	![step13.png](https://i.loli.net/2021/11/06/8lwDKo3OunAeyEQ.png)

9. 在自己新建的本地分支下进行修改，添加操作

	![step14.png](https://i.loli.net/2021/11/06/fF7XuWEUOgwdxZR.png)

10. 查看修改内容，添加到本地暂存区

	![step15.png](https://i.loli.net/2021/11/06/Y65FnpmDygo2ixa.png)

11. 添加提交注释，提交修改到本地仓库，这样本地仓库就形成了一个新的版本

	![step16.png](https://i.loli.net/2021/11/06/rYvuAqiyKmkhnd9.png)

12. 将本地的仓库发布到自己的远程仓库（注意是自己的仓库，不是公共仓库，因为远程仓库我们不维护这么多分支，只维护一个 main 分支，我们暂时也不需要 dev 分支来测试）

	![step17.png](https://i.loli.net/2021/11/06/nDZywE9VgSqhTas.png)
	![step18.png](https://i.loli.net/2021/11/06/kPUxclqMXuVZLjs.png)

13. 去自己的 github 对应的仓库，如果发布成功的话，就会显示如图信息，点击 `Compare & Pull request`

	![step19.png](https://i.loli.net/2021/11/06/S3EvWezx6nlVtsC.png)

14. 在 pr 页面输入对应的标题等.... 点击提交

	![step20.png](https://i.loli.net/2021/11/06/pUsDjrlAGOIMt8Q.png)

15. 后续新建分支都从远程仓库 721/main 上新建，如果发现新建的分支没有保持最新，可以执行

```
git fetch 721
git merge 721/main
```

16. 分一个新任务，我们都在一个新的分支上进行操作，一个具体分支干具体的事情