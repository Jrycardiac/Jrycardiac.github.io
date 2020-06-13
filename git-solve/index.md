# 初学git的踩坑之路


# 初学git之路问题总结

当我下定不学会不罢休的决心学习git的时候出现了一个又一个的错误

下面是我亲手解决之后的总结

-------

# 我究竟遇到了那些错误?

* 对git常用语法不熟悉导致的低级错误
    *  对于几乎不使用命令行的我来说简直是死亡一般的灾难
    *  之后花了点时间大致读了一下git--help，才避免了这些低级错误
* 出现错误提示
```javascript
    error: src refspec master does not match any.

    error: failed to push some refs to 
```

   常见原因：

  1.本地git仓库目录下为空
    
   2.本地仓库add后未commit

   3.git init错误
        
   4.在GitHub上面添加了README.MD文件之后，需要重新进行更新

   解决办法：

   1.控制面板打开文件夹选项  打开隐藏文件和文件夹显示

   2.到本地仓库目录下查看是否有.git文件夹——无 则git init

   3.看.git文件夹下是否有之前提交的文件——若无 则重新 git commit 
        (如果之前git add过的话 没有就要重新 add commit)
        
   4.在git-push 之前添加 git-pull 操作之后，重新进行push操作
* git commit 时，出现错误
```javascript
    error: Error building trees  
```
解决办法：
        
   执行命令 git reset --mixed  
        
   （查资料得出的解决办法，原因不是很明白，但确实能解决问题） 
* 出现错误
```javascript
error:  nothing added to commit but untracked files present.
```
   原因：

   git没有把提交的文件加载进来，但是把需要提交的文件都列出来了
        
   解决办法：

   用git add XXX(文件名) 把需要提交的文件加上 ，然后git commit -m "xx",
        

再git push -u origin master重新提交就可以了

## 注意
上面列举为出现次数最为频繁的问题，一些自己很快能够解决的就没贴出来。

（当然绝对不是因为我懒）

##              欢迎指正呀
