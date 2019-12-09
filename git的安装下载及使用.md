# Git Bash的配置

1. 下载地址：[https://git-scm.com/](https://git-scm.com/)
	双击安装，注意每一步的选项要参考下面的图（如果没有对应的图，就直接下一步）
2. 

3. 安装过程
 
![](https://upload-images.jianshu.io/upload_images/13839130-78bc34b6d4ec2cb9.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/13839130-645737c313c9ce5a.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

下面的路径可以随便填：

![](https://upload-images.jianshu.io/upload_images/13839130-4a2ccd759020cfeb.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/13839130-73fbb160cc1f26db.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/13839130-3b5b29e1937e43f6.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/13839130-ed0d9d2b2b42117e.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/13839130-3968603d7944bf40.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/13839130-e73a811b2bb1a459.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
好了，安装完成。
安装成功之后，需要设置一下外观：






## 安装完Git Bash后还需要添加SSHkey 
- 进入[https://github.com/settings/keys](https://github.com/settings/keys) 
-  如果页面里已经有一些 key，就点「delete」按钮把这些 key 全删掉。如果没有，就往下看
- 点击 New SSH key，你需要输入 Title 和 Key，但是你现在没有 key，往下看
- 打开 Git Bash
- 复制并运行 ```rm -rf ~/.ssh/*``` 把现有的 ssh key 都删掉，这句命令行如果你多打一个空格，可能就要重装系统了，建议复制运行
- 运行 ```ssh-keygen -t rsa -b 4096 -C "你的邮箱"```，注意填写你自己的邮箱！
- 按回车三次
- 运行 ```cat ~/.ssh/id_rsa.pub```，得到一串东西，完整的复制这串东西
- 回到上面第 3 步的页面，在 Title 输入「我的第一个 key」
- 在 Key 里粘贴刚刚你你复制的那串东西
- 点击 Add SSH key
- 回到 Git Bash
- 运行 ```ssh -T git@github.com```，你可能会看到这样的提示：
![](https://upload-images.jianshu.io/upload_images/13839130-82380e7b77e096c4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 输入 ```yes``` 回车
- 然后如果你看到 Permission denied (publickey). 就说明你失败了，请回到第 1 步重来，是的，回到第 1步重来；如果你看到 ```Hi xuchuguo! You've successfully authenticated, but GitHub does not provide shell access.``` 就说明你成功了！


## 配置Git
```
    git config --global user.name "你的英文名"
    git config --global user.email "你的邮箱"
    git config --global push.default matching
    git config --global core.quotepath false
    git config --global core.editor "vim"
```

接下来
