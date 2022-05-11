# git_practice

新規でリモートリポジトリ作った後に、ローカルファイルと纏めてmergeする手順

```
github> git init
Initialized empty Git repository in C:/path/to/your/github/.git/
```

```
ithub> git remote add origin https://github.com/enginearn/git_practice.git
```

```
github> New-Item sample.txt
```

```
github> git pull origin main
From https://github.com/enginearn/git_practice
* branch            main       -> FETCH_HEAD
```

```
github> git branch
* master
```

```
github> dir

    Directory: C:\path\to\your\github

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a---          2022/05/11    15:29             14 README.md
-a---          2022/05/11    15:25            993 sample.txt
```

```
github> New-Item .gitignore
```

```
ithub> git add .
```

```
github> git commit -m "git command手順確認"
```

```
github> git status
On branch master
nothing to commit, working tree clean
```

```
github> git branch
* master
```

```
github> git push --set-upstream origin master
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 859 bytes | 859.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/enginearn/git_practice/pull/new/master
remote:
To https://github.com/enginearn/git_practice.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.
```

ここまで出来たら、github上で```Pull request```から```merge```して一旦おしまい。

今、READ.mdをgithub上で編集してるので、
次回ローカルから```git pull origin main```から始めれば、すっきり操作できる
