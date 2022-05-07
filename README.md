# misc.

```
# size of items
du -sh *

# number of items
ls | wc -l

rm img_{1..10}.jpg

nvidia-smi -l 1

ps -ef
kill `PID`
```

# venv

```
python3 -m venv ~/x/xvnv

nano ~/.zshrc

cd ~/x
source xvnv/bin/activate

source ~/.zshrc
```

# conda

```
```

# git

```
git status

git add work1.txt
git commit -m "work1 msg"

git commit -a -m "work2 msg"

git log
git log --oneline
git log --oneline --all --graph

git commit --amend -m "msg ammended"

# HEAD: points at working directory
# master: refers to the latest change

git checkout 055d
git checkout master

git reset --hard 624e

git reflog

git branch exp
git checkout -b exp

git tag release/1.0

git remote add origin https://github.com/user/repo.git

git push --set-upstream origin master
git push
```
