+++
date = '2025-05-07T22:45:06+08:00'
draft = false
title = 'note'
url = '/test/'
+++
子文件夹中的内容访问不到

甚至这个文件也访问不到

## todo list
- [ ] hugo到底有什么用呢，我能用它实现什么？

## 推荐网站
- 机器学习课程网站 Coursera
- 数据分析技能学习网站 DataCamp
- 数据科学课程学习网站 Udemy
- 生物统计学教授的博客 Simply Statistics

## 拦路虎
现在遇到的问题是：本地显示的格式是正常的，但是gitpage上显示的格式是不正常的。

现在测试快速设置主题

Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender

hugo --source blog server --disableFastRender

### hugo 的常用命令
hugo server --navigateToChanged

hugo server
hugo -D
## 测试本地修改后
是否直接打开了文件--没有

再来
hugo new site hehe 
cd hehe
hugo new theme hehe
echo "theme = 'hehe'" >> hugo.toml
hugo new content content/posts/hehe-p1.md

测试后发现在wsl中是有效的，windows中无效。

## git中不熟悉的命令

### 删除后重建分支
git rm -rf .
git commit --allow-empty -m "Initialize gh-pages branch"
git push origin gh-pages

3. 验证远程仓库地址
确保远程地址使用的是 SSH 而不是 HTTPS：

bash
git remote -v
如果显示 HTTPS 地址（如 https://github.com/biggerwriting/hugo-pages.git），请修改为 SSH 地址：

```bash
git remote set-url origin git@github.com:biggerwriting/hugo-pages.git
```

4. 检查权限
确保您的 SSH Key 对应的 GitHub 用户有写权限。如果 Deploy Key 是通过 CI/CD 工具生成的，确认相关工具是否正确配置了权限。

5. 如果仍然有问题
删除当前 Deploy Key，并通过以下步骤重新生成新的 SSH Key 并配置：
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
将生成的公钥添加到 GitHub 仓库的 Deploy Key 或您的个人账户 SSH Key 中。
确保启用了 Allow write access。
完成以上步骤后，重新尝试推送：

bash
git push origin main


### 不懂作用
git checkout --orphan gh-pages
git reset --hard