cehsi
ceshi

如果出现以下问题：
liqilv@qilv MINGW64 /d/GitHub/Testing (master)
$ git add caogao.docx

liqilv@qilv MINGW64 /d/GitHub/Testing (master)
$ git commit -m "test"
[master 6282967] test
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 caogao.docx

liqilv@qilv MINGW64 /d/GitHub/Testing (master)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 4 commits.
  (use "git push" to publish your local commits)
nothing to commit, working directory clean

liqilv@qilv MINGW64 /d/GitHub/Testing (master)
$ git push origin master
To git@github.com:CharlieLi-CHINA/Testing.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'git@github.com:CharlieLi-CHINA/Testing.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

那么解决方法如下：
liqilv@qilv MINGW64 /d/GitHub/Testing (master)
$ git pull --rebase
remote: Counting objects: 2, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (2/2), done.
From github.com:CharlieLi-CHINA/Testing
   f7b4f21..984a8e4  master     -> origin/master
First, rewinding head to replay your work on top of it...
Applying: readme
Applying: huatu example
Applying: test
Applying: test

#参考 http://weimenlove.blog.163.com/blog/static/17775473201451113233968/
今天更新了一下git，然后出现如下问题：
$ git status -u
# On branch master
# Your branch is ahead of 'origin/master' by 6016 commits.
#

解决方法：
# git pull --rebase
remote: Counting objects: 5304, done.
remote: Compressing objects: 100% (1417/1417), done.
remote: Total 4299 (delta 3122), reused 4043 (delta 2880)
Receiving objects: 100% (4299/4299), 2.19 MiB | 449 KiB/s, done.
Resolving deltas: 100% (3122/3122), completed with 425 local objects.
From git://git.kernel.org/pub/scm/git/git
   8ef2794..bce14aa  maint      -> origin/maint
   16eed7c..bce14aa  master     -> origin/master
 + 68bd821...59f2e5e next       -> origin/next  (forced update)
 + d3a6f81...fa8cfe3 pu         -> origin/pu  (forced update)
   85a4700..aa5f592  todo       -> origin/todo
Current branch master is up to date.

