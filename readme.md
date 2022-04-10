# Githug通关笔记

## 1.第1关

####  关卡描述：

```undefined
有一个新的目录“git_hug”被创建了，在它里面初始化一个仓库
```

#### 通关操作：

```kotlin
git init  
```

![微信截图_20210220130451](git-picture\20210220130451.png)

#### 心得：

git init 可将文件夹初始化为本地仓库，并创建.git。

## 2.第2关

####  关卡描述：

```undefined
设置你的用户名与电子邮箱，这很重要，只有这样你的提交才会被识别 
```

#### 通关操作：

```css
git config --local user.name zhangjingrur 
git config --local user.email 738893647@qq.com
```

![2](git-picture\2.png)

#### 心得：

设置用户名和密码是必要的，本地向远程仓库push之前必须配置好用户名和密码，否则push无法成功。

## 3.第3关

####  关卡描述：

```undefined
有一个名叫“README”的文件夹，你要将它加入到暂存区。  
注意：每一关都是一个新仓库，不要在前面的关卡找文件。
```

#### 通关操作：

```csharp
git add README  
```

![3](git-picture\3.png)

#### 心得：

git add 指令可将文件添加到暂存区。

## 4.第4关

####  关卡描述：

```undefined
“README”文件已经被加入到暂存区，现在提交它。  
```

#### 通关操作：

```bash
git commit -m "add README"  
```

![4](git-picture\4.png)

#### 心得：

git commit 指令用来将本地暂存的修改提交到版本库，-m参数是为了输入提交信息。

## 5.第5关

####  关卡描述：

```undefined
从“https://github.com/Gazler/cloneme”克隆仓库。 
```

#### 通关操作：

```php
git clone https://github.com/Gazler/cloneme  
```

![5](git-picture\5.png)

#### 心得：

git clone拷贝一个Git仓库到本地，这样本地可以查看该项目，或者进行修改。

## 6.第6关

####  关卡描述：

```undefined
从“https://github.com/Gazler/cloneme”克隆仓库到“my_cloned_repo”目录。
```

#### 通关操作：

```php
git clone https://github.com/Gazler/cloneme  my_cloned_repo 
```

![6](git-picture\6.png)

#### 心得：

在git clone 仓库地址后面加上指定的文件夹名称，可将远程仓库拷贝到指定的目录下。

## 7.第7关

####  关卡描述：

```undefined
文本编辑器“vim”为所有文件创建以“.swp”结尾的文件，这些文件当前都被打开了。我们不希望他们潜入到仓库。让仓库忽略“.swp”文件。
```

#### 通关操作：

```cpp
//由于没有装vim，直接用记事本打开“.gitignore”文件，在文件末尾换行并加上“*.swp”。 
```

![7](git-picture\7.png)

#### 心得：

在.gitignore文件中添加所要忽略的特定的文件种类，这样此类文件将不会进行版本管理。

## 8.第8关

####  关卡描述：

```undefined
注意一些文件以“.a”为扩展名。我们希望忽略这些文件除了“lib.a”文件。 
```

#### 通关操作：

```cpp
//由于没有装vim，直接用记事本打开“.gitignore”文件，在文件末尾换行并加上“*.a”，再换行，在文件末尾加上“!lib.a”。
```

![8](git-picture\8.png)

#### 心得：

在.gitignore文件中每个文件占一行，.gitignore文件也需要放到.gitignore文件中。

## 9.第9关

####  关卡描述：

```undefined
仓库中有一些文件，其中一个没有被跟踪，它是哪个文件。
```

#### 通关操作：

```undefined
git status  
```

![9](git-picture\9.png)

#### 心得：

使用git status 指令后，Untracked files显示的即未被跟踪的文件。

## 10.第10关

####  关卡描述：

```undefined
仓库中有一些文件。多少文件将要被提交。
```

#### 通关操作：

```undefined
git status  
```

![10](git-picture\10.png)

#### 心得：

使用git status 指令后，Change to be commited 显示的即已经暂存待提交的文件。

## 11.第11关

####  关卡描述：

```undefined
一个文件从工作树上面移除了，但是没有从仓库中移除。找到这个文件并移除它。
```

#### 通关操作：

```csharp
git status  
git add deleteme.rb  
```

![11](git-picture\11.png)

#### 心得：

使用git status 指令后，可以显示所在的分支，Change not staged for commit 下面红色字体显示出工作树上没有但仓库中还存在的文件。

## 12.第12关

####  关卡描述：

```undefined
一个文件以外地加入到你的暂存区，找出这个文件并将它从暂存区移除。  
*注意*：不要将它从文件系统中移除，仅仅将它git中移除。
```

#### 通关操作：

```css
git status  
git rm --cached deleteme.rb    
```

![12](git-picture\12.png)

#### 心得：

git rm 删除本地及仓库中的文件；git rm --cached 删除仓库中的文件，保留本地的文件。

## 13.第13关

####  关卡描述：

```undefined
你做了一些修改，并且稍后再它们上面工作。你应该保存它们，但是不提交它们。 
```

#### 通关操作：

```undefined
git stash   
```

![13](git-picture\13.png)

#### 心得：

git stash用于想要保存当前的修改，但是想回到之前最后一次提交的干净的工作仓库时进行的操作，

git stash将本地的修改保存起来，并且将当前代码切换到HEAD提交上。

## 14.第14关

####  关卡描述：

```undefined
我们有一个名为“oldfile.txt”的文件。我们想要将它重命名为“newfile.txt”并保存该修改。 
```

#### 通关操作：

```css
git mv oldfile.txt newfile.txt  
```

![14](git-picture\14.png)

#### 心得：

git mv命令用于移动或重命名一个文件、目录或软连接，git mv  [file]  [newfile] 可将文件重命名。

## 15.第15关

####  关卡描述：

```undefined
你添加了一些文件到你的仓库，但现在知道你的项目需要进行调整。创建一个新的文件夹命名为“src”,使用git将所有的".html"文件到该文件夹中 
```

#### 通关操作：

```css
mkdir src
git mv about.html contact.html index.html src 
```

![15](git-picture\15.png)

#### 心得：

git mv +文件名+ 新文件路径，可将指定的文件移动到指定的文件目录中。

## 16.第16关

####  关卡描述：

```undefined
你将要寻找最新提交的哈希，为此你将研究该仓库的日志。 
```

#### 通关操作：

```bash
git log 
```

![16](git-picture\16.png)

#### 心得：

git log可查看提交历史，显示commit hash、author、date等信息。

## 17.第17关

####  关卡描述：

```undefined
我们有一个git仓库，并且我们想用“new_tags”来标记当前的提交。 
```

#### 通关操作：

```bash
git tag "new_tag"
```

![17](git-picture\17.png)

#### 心得：

git tag 打本地标签，可以标记当前提交的状态。

## 18.第18关

####  关卡描述：

```undefined
仓库中有一些标记没有被推送到远程仓库，现在推送它们。  
```

#### 通关操作：

```undefined
git push --tags origin master
```

![18](git-picture\18.png)

#### 心得：

git push --tags  origin  master 将本地标签推送到远程仓库的master分支。

## 19.第19关

####  关卡描述：

```undefined
“README”文件被提交了，但是“forgotten_file.rb”文件貌似忘了提交。添加这个文件，并改正上次提交使之包含该文件。  
```

#### 通关操作：

```csharp
git add forgotten_file.rb   
git commit --amend -m "修改提交"
```

![19](git-picture\19.png)

#### 心得：

git commit -m 提交后发现有问题，需要撤销上次的提交，可以使用git commit --amend -m 。

## 20.第20关

####  关卡描述：

```undefined
用未来的时间日期（比如明天）来提交修改。   
```

#### 通关操作：

```bash
git commit --date=02.21.2021T09:00:00 -m "指定提交时间为2021年2月21日9点整"
```

![20-1](git-picture\20-1.png)

#### 心得：

git commit --date=日期 可以指定提交的（未来）时间。

## 21.第21关

####  关卡描述：

```undefined
有两个文件要提交，目标是将每个文件添加为单独提交，但意外地两个文件都被添加到暂存区了。用“reset”命令将“to_commit_second.rb”文件从暂存区移除（不做提交操作）。
```

#### 通关操作：

```css
git reset HEAD to_commit_second.rb  
```

![21](git-picture\21.png)

#### 心得：

git reset HEAD 是将暂存区和HEAD的提交保持一致；git reset  -- hard HEAD 是将工作区、暂存区和HEAD保持一致。

## 22.第22关

####  关卡描述：

```undefined
提交太快了。现在你要撤消最后一次提交，同时保持索引。 
```

#### 通关操作：

```undefined
git reset --soft HEAD~1 
```

![22](git-picture\22.png)

#### 心得：

git reset -- soft 回退到某个版本，只回退了commit的信息，如果还要提交直接commit即可；

git reset -- hard彻底回退到某个版本，本地的代码也会变为上一个版本的内容，撤销的commit中所

包含的更改被冲掉 。



## 23.第23关

####  关卡描述：

```undefined
文件已经被修改了，但是你不想保存该修改。从最后一次提交中检出“config.rb”文件。
```

#### 通关操作：

```css
git checkout config.rb  
```

![23](git-picture\23.png)

#### 心得：

git checkout 单个文件 可将该文件从暂存区恢复到工作区。

## 24.第24关

####  关卡描述：

```undefined
项目有一个远程仓库，找出它。
```

#### 通关操作：

```undefined
git remote -v   
```

![24](git-picture\24.png)

#### 心得：

git remote -v 列出仓库的详细信息，在每一个名字后面列出远程仓库的地址。

## 25.第25关

####  关卡描述：

```undefined
远程仓库有一个与之关联的url。输入远程仓库“remote_location” 的url。  
```

#### 通关操作：

```undefined
git remote -v  
https://github.com/githug/not_a_repo
```

![25](git-picture\25.png)

#### 心得：

githug reset可回退到上次游戏结果，重新开始。

## 26.第26关

####  关卡描述：

```undefined
你需要从“origin”仓库拉下改变到本地仓库。    
```

#### 通关操作：

```undefined
git pull origin master  
```

![26](git-picture\26.png)

#### 心得：

git pull将远程仓库的内容拉到本地仓库。

## 27.第27关

####  关卡描述：

```undefined
添加一个url为“https://github.com/githug/githug”的远程仓库，并为该远程仓库命名为“origin”。 
```

#### 通关操作：

```csharp
git remote add origin https://github.com/githug/githug   
```

![27](git-picture\27.png)

#### 心得：

git remote add origin+url 添加与本地仓库关联的远程仓库。

## 28.第28关

####  关卡描述：

```undefined
你的本地“master”分支与远程仓库“origin”的“master” 分支不一致，请用远程仓库“origin”的“master” 分支来改变你的提交，并将提交推送到远程仓库。 
```

#### 通关操作：

```undefined
git rebase origin/master  
git push origin master 
```

![28](git-picture\28.png)

#### 心得：

git rebase master 将master最新的分支同步到本地，这个过程可能需要手动解决冲突。

## 29.第29关

####  关卡描述：

```undefined
自最后一次提交后，“app.rb”文件发生了一些改变。找出该文件那些行被改变了。  
```

#### 通关操作：

```undefined
git diff  
```

![29](git-picture\29.png)

#### 心得：

git diff 比较文件的不同，即比较文件在暂存区和工作区的差异。

## 30.第30关

####  关卡描述：

```undefined
有人将密码放进了“config.rb”文件中，找出是谁。   
```

#### 通关操作：

```css
git blame config.rb  
git blame config.rb | grep "password"
```

![30](git-picture\30.png)

#### 心得：

git blame查看某个文件的每一行内容由谁所写。

## 31.第31关

####  关卡描述：

```undefined
你想在一段可能打破一些东西的代码上工作，创建一个“test_code”分支。   
```

#### 通关操作：

```kotlin
git branch test_code  
```

![31](git-picture\31.png)

#### 心得：

git branch 分支名： 创建一个分支。

## 32.第32关

####  关卡描述：

```undefined
创建并切换到名为my_branch的新分支，需要创建一个分支就像上一关做的那样。  
```

#### 通关操作：

```undefined
git checkout -b my_branch  
```

![32-1](git-picture\32-1.png)

![32-2](git-picture\32-2.png)

#### 心得：

git checkout -b ：创建并切换到分支。 

## 33.第33关

####  关卡描述：

```undefined
需要在“1.2”版本的应用程序上修复一个bug。检出“v1.2”标记。  
```

#### 通关操作：

```css
git tag
git checkout v1.2  
```

![33](git-picture\33.png)

#### 心得：

git tag 查看本地标签， git checkout tag_name检出此tag对应的代码。

## 34.第34关

####  关卡描述：

```undefined
你需要在“1.2”版本的应用程序上修复一个bug。检出“v1.2”标记(注意：有一个名为“v1.2”的分支)。 
```

#### 通关操作：

```undefined
git checkout tags/v1.2
```

![34](git-picture\34.png)

## 35.第35关

####  关卡描述：

```undefined
在前一个提交你忘了创建分支，并在该分支上进行提交操作。在最后一次提交前创建一个名为“test_branch”的分支。 
```

#### 通关操作：

```undefined
git branch test_branch HEAD~1  
```

![35](git-picture\35.png)

#### 心得：

git branch 分支名  HEAD~1 :在前次提交前创建一个分支。

## 36.第36关

####  关卡描述：

```undefined
在你的项目中创建了太多的分支。有一个旧的名为“delete_me”的分支，你应该删除它。 
```

#### 通关操作：

```undefined
git branch -d delete_me  
```

![36](git-picture\36.png)

#### 心得：

git branch -d 分支名:删除某个分支。

## 37.第37关

####  关卡描述：

```undefined
在本地分支上你做了一些改变，并且想共享它，但是不准备将它合并到“master”分支上。   
```

#### 通关操作：

```css
git push origin test_branch:test_branch
```

![37](git-picture\37.png)

#### 心得：

git push origin 分支：分支  指令可将本地的分支Push到远程仓库对应的分支上，如果远程仓库没有

这个分支会新建一个对应的新分支。

## 38.第38关

####  关卡描述：

```undefined
在“feature”分支上有一个文件，让我们将它合并到“master”分支上。 
```

#### 通关操作：

```undefined
git merge feature  
```

![38](git-picture\38.png)

#### 心得：

git merge 分支名：合并指定分支到当前分支master。

## 39.第39关

####  关卡描述：

```undefined
看起来有一个新的分支被推入了我们的远程仓库。在不将更改与本地仓库合并的情况下获取更改
```

#### 通关操作：

```undefined
git fetch origin  
```

![39](git-picture\39.png)

#### 心得：

git fetch origin: 获取远程仓库的内容，但不合并到本地仓库。

## 40.第40关

####  关卡描述：

```undefined
我们用“git rebase”工作流与“feature”分支准备进入“master”分支。将“feature”分支上的改变合并到“master”上。 
```

#### 通关操作：

```undefined
git rebase master feature 
```

![40](git-picture\40.png)

## 41.第41关

####  关卡描述：

```undefined
你已经从wrong_branch创建了分支，并且已经进行了一些提交，你意识到你需要从master创建你的分支。重新调整提交到master分支，这样就不会有wrong_branch提交。
```

#### 通关操作：

```bash
git rebase --onto master wrong_branch
```

![41](git-picture\41.png)

#### 心得：

git merge：用于从指定的分支（节点）合并到当前分支的操作。

1. git会将指定的分支与当前的分支进行比较，找出二者最近的一个共同节点base，之后将指定分支在base之后分离的节点合并到当前分支上。

2. 分支合并，实际上是分支间差异提交节点的合并。

3. 常用的合并分支命令格式：git merge 源分支 [目的分支，默认master]。

   ![41-1](git-picture\41-1.png)

git rebase：用于合并目标分支内容到当前分支。

1. 常用的合并命令格式：git rebase branch_name；

2. 如果你要将其他分支的提交节点合并到当前分支，git rebase和git merge都可以达到目的。

   ![41-2](git-picture\41-2.png)

   ## 42.第42关

   ####  关卡描述：

   ```undefined
   将版本库未打包的松散对象打包，确保多余的包被删除。
   ```

   #### 通关操作：

   ```undefined
   git repack -d 
   ```

####     ![42](git-picture\42.png)

####      心得：

​     git-repack  - 在存储库中打包解包的对象。

## 43.第43关

####  关卡描述：

```undefined
你的新功能是不值得花时间的，你将要删除它。但是它有一个提交填充了“README”文件，你想要将这个提交同样应用到“master”分支上。
```

#### 通关操作：

```bash
git log --all  
git cherry-pick ca32a6dac7b6f97975edbe19a4296c2ee7682f68  
```

![43-1](git-picture\43-1.png)

![43-2](git-picture\43-2.png)

####  心得：

​    git cherry-pick <commit id>：合并某一个提交。

## 44.第44关

####  关卡描述：

```undefined
项目的截止日期快到了，你想评估你的代码中还有多少“TODO”剩下。
```

#### 通关操作：

```undefined
git grep TODO  
```

![44](git-picture\44.png)

#### 心得：

   git grep可以很方便地从提交历史或者工作目录中查找一个字符串或者正则表达式。

## 45.第45关

####  关卡描述：

```undefined
改正你第一次（非根）提交信息中的错误。
```

#### 通关操作：

```bash
1、git log  
2、git rebase -i 50651402d47a0a7a4f09593c5625c026f6dbedb9（Initial commit的hash值）
3、进入VIM编辑界面，将错误信息所在的那个提交中的pick修改为edit，保存并退出
4、git commit –amend（修改提交的错误信息）
5、进入VIM编辑界面，修改 coommit为commit
6、git rebase --continue
```

![45-1](git-picture\45-1.png)

![45-2](git-picture\45-2.png)

#### 心得：

   进入vim编辑器界面后键盘点击i编辑内容；编辑完成后Esc---> : ---> wq --->Enter。

## 46.第46关

####  关卡描述：

```undefined
你做了几次提交，但是想将这些修改都合并到一个提交中。
```

#### 通关操作：

```bash
1、git log  
2、git rebase -i 40d201b820cb6482d6cc574d73a94b0460a988e8
3、进入VIM编辑界面，将下面3个pick改为squash
```

![46-3](git-picture\46-3.png)

![46-4](git-picture\46-4.png)![46-1](git-picture\46-1.png)

![46-2](git-picture\46-2.png)

#### 心得：

分支上过多commit的话，比如一个功能点我们可能分了几个提交，如果合并到主分支的话，提交记录会显得繁琐，最终我们重点关注的应该是这个功能点的提交，而不是开发者中间做了多少开发，这时候就要用到了git squash。

## 47.第47关

####  关卡描述：

```undefined
合并“long-feature-branch”分支中所有的提交到一个提交中。
```

#### 通关操作：

```cpp
git merge --squash long-feature-branch  
git commit -m "merge squash"  
```

![47](git-picture\47.png)

#### 心得：

git merge --squash 是用来把一些不必要commit进行压缩，比如说，你的feature在开发的时候写的commit很乱，那么我们合并的时候不希望把这些历史commit带过来，于是使用–squash进行合并，此时文件已经同合并后一样了，但不移动HEAD，不提交。需要进行一次额外的commit来“总结”一下，然后完成最终的合并。

## 48.第48关

####  关卡描述：

```undefined
你做了几次提交，但是顺序错了。请为你的提交重新排序。
```

#### 通关操作：

```bash
1、git log  
2、git rebase -i 3f70e0bee08a7b07d646c96664b57b7f93e42f34  
3、进入VIM编辑器，将错误的提交信息调换，使顺序正确
4、git log
```

![48-1](git-picture\48-1.png)

![48-2](git-picture\48-2.png)

## 49.第49关

####  关卡描述：

```undefined
在某个地方引入一个bug，你知道运行“ruby prog.rb 5”应该输出“15”。你同样可以运行“make test”。进入bug的提交的哈希的前7个字母是什么。
```

#### 通关操作：

```bash
git log --pretty=oneline  
git bisect start
git bisect good f608824
git bisect bad 12628f4
git bisect run make test
```

![49-1](git-picture\49-1.png)

![49-2](git-picture\49-2.png)

#### 心得：

1. play 默认命令，检查是否过关
2. hint 提示
3. reset 重置本关或到其他关
4. levels 查看所有关卡

## 50.第50关

####  关卡描述：

```undefined
你修改了一个文件的多处代码，这些代码分属于2个不同的功能，代码还没有提交到暂存区。仅提交第1个功能相关的代码到暂存区。
```

#### 通关操作：

```csharp
git status  
git add -p  feature.rb  
e  
git diff
git status
```

![50](git-picture\50.png)

![50-3](git-picture\50-3.png)

![50-2](git-picture\50-2.png)



## 51.第51关

####  关卡描述：

```undefined
你一直在一个分支工作，被一个主要问题弄得心烦意乱，并且你忘了这个分支的名字。切换回那个分支。
```

#### 通关操作：

```undefined
git reflog  
git checkout solve_world_hunger 
```

![51](git-picture\51.png)

#### 心得：

git reflog 可以列出所有的操作记录。

## 52.第52关

####  关卡描述：

```undefined
你做了多次提交，但是想要撤销中间的提交。所有的提交已经被推送，你不能改变现存的历史。
```

#### 通关操作：

```bash
git log  
git revert  59f058e  
git log
```

![52-1](git-picture\52-1.png)

![52-2](git-picture\52-2.png)

#### 心得：

与 `reset` 不同的是，revert 只会撤销当前的 commit，而之后的 commit 操作的修改还会保留，但是`reset` 还会将之后的所有 commit 操作的修改全部退回 staging area 或丢弃。

## 53.第53关

####  关卡描述：

```undefined
你决定用 git reset --hard HEAD^ 删除最后一次提交（一个不太明智的决定），然后你又反悔了，想回退到这条命令之前。请恢复被删除的提交。
```

#### 通关操作：

```undefined
git log --pretty=oneline
git reflog  
git reset --hard908efd9
git reflog 
```

![53](git-picture\53.png)

#### 心得：

git reset --hard hash-code：恢复到的当时提交的哈希值。在执行此命令之后，提交日志中会增加一条提交日志，操作日志会自动增加一条 "reset: moving to hash-code" 的日志。

## 54.第54关

####  关卡描述：

```undefined
你要把名为 mybranch 的分支合并到当前分支 master 中，但是可能有些地方的修改会引起冲突。请解决冲突，完成合并。
```

#### 通关操作：

```css
git merge mybranch    
编辑 poem.txt  
git add poem.txt  
git commit -m "add poem.txt"  
```

![54](git-picture\54.png)

#### 心得：

找到冲突文件后，其中7个左尖括号 `<<<<<<<` 和7个右尖括号 `>>>>>>>` 之间的区域是冲突的部分，而中间的7个等号 `=======` 则把有冲突的代码分开，上部分是你的代码（通常是主线代码），下部分是别人的代码（通常是开发分支的代码）。编辑这部分内容，保留你想要的，删除你不要的，保存退出，再单独提交这个文件即可。

## 55.第55关

####  关卡描述：

```undefined
你想把 https://github.com/jackmaney/githug-include-me 这个仓库的代码引入到自己项目的 ./githug-include-me 目录，这个方法不需要克隆第三方仓库，也不需要把第三方仓库的文件复制到你的项目中。
```

#### 通关操作：

```csharp
git submodule add https://github.com/jackmaney/githug-include-me githug-include-me
```

![55](git-picture\55.png)

#### 心得：

如果你想把别人的仓库代码作为自己项目一个库来使用，可以采用模块化的思路，把这个库作为模块进行管理，git submodule add module-url 可以添加指定远程仓库到指定目录。

## 56.第56关

####  关卡描述：

```undefined
这是最后一关，目标是让你在 Github 上提交一个 pull request 贡献。设计本关的目的就是鼓励你向 Githug 提交贡献，而不是测试你使用 pull request 的技能。贡献包括新的关卡、修复BUG和改善文档
```

#### ![56](git-picture\56.png)






