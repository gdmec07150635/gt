### Git demo

#### Git base

1. Create a git repo.
2. Use `markdown` to write the README.md.
3. Create a private repo.
```ruby
git checkout -b yang
```

#### Use private repo
1. Commit to the private repo.
2. Merge to the master repo.
3. Push to master.
```ruby
git checkout -b yang # 创建yang本地分支
git branch # yang 查看当前分支
vim demo.rb
# bala bala
git add demo.rb
git commit
git checkout master # 切换到master分支
git branch # 查看本地分支
git merge yang # 合并yang到当前分支，这里是master
git branch -d yang # 删除yang本地分支
git branch -r # 查看远程分支
git branch -a # 查看所有分支

git checkout -b feature # 创建本地分支, 当前分支是那个，那么该分支就是基于那个创建的
# bala bala
git add .
git commit
git push origin feature # 把本地分支推送到远程
```


```ruby
git push origin branch_name:remote_branch_name # 把分支推送到远程, 通常本地分支的名字和远程分支相同
git checkout -b branch_name origin/remote_branch_name # or git checkout --track origin/remote_branch_name
git push origin :branch_name # 删除远程分支
git branch -d branch_name # 删除本地分支
```

#### Tag

```ruby
git tag # 查看标签
git tag -l 'v1.4.2.*'

git tag -a v1.5 -m "add v 1.5 tag" # 含附注的标签
git show v1.5

git tag v1.6-light # 轻量级标签

git push origin v1.5 # 分享标签, release is from here
git push origin --tags # 一次性推送所有标签
```

#### Checkout remote branch

```ruby
git fetch origin
git checkout yang
git branch -a
git checkout -b yang origin/yang
```

#### Checkout remote tag
```ruby
git fetch --tags
git checkout tags/tag_name
```

#### Rebase

```ruby
git rebase master # rebase vs master
```

