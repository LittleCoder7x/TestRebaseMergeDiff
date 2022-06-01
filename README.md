# TestRebaseMergeDiff
测试merge 和 rebase的区别

### master
这是master分支的更新提交
### rebase
这是rebase分支的第一次提交


# Diff
---- 分别 merge 和 rebase 分支上 去合并main分支 
- merge
  - 如果 main 分支 在拉出 merge 分支后， 没有别的提交， 那不会产生多余的 ‘merge ...’ 提交
  - 如果 main 分支 在拉出 merge 分支后， 有别的提交， 有冲突解决后/无冲突，会产生多余‘merge ...’提交
- rebase
  - 如果 main 分支 在拉出 rebase 分支后，没有别的提交， 那么rebase分支提交不会改变
  - 如果 main 分支 在拉出 rebase 分支后，有别的提交， 那么rebase分支会先拉取 main 分支到本分支上， 然后将rebase 分支上的提交放在 main 分支后的提交上， 提交的 hash 值会被改变