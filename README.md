# Commands

## misc.

```
# disk usage
du -sh *

# disk free
df -h

# list count
ls | wc -l

# list size descending order
ls -lSh

rm img_{1..10}.jpg

nvidia-smi -l 1

# process status
ps -ef
kill PID

# hidden files
ls -al

# shell restart
source ~/.bashrc

# download
wget url

# tar
tar cvf A.tar A
tar tvf A.tar
tar xvf A.tar
```

## brew

```
brew install miniconda
brew uninstall miniconda
```

## venv

```
python3 -m venv xvnv

source xvnv/bin/activate
deactivate

pip freeze

nano ~/.zshrc
  cd ~/x
  source xvnv/bin/activate
source ~/.zshrc
```

## conda

```
conda create --name xcda python=3.8

conda activate xcda
conda deactivate

conda config --set auto_activate_base false

conda env list

# packages can be installed from anaconda, conda-forge, or pypi (pip).

# requirements.txt equivalent
conda env export --file environment.yml 
conda env create -n xcda -f /path/to/environment.yml
conda env update -n xcda -f /path/to/environment.yml

conda env remove -n xcda
```

## git

```
git init

git status

git add .
git add work1.txt
git commit -m "work1 msg"

git commit -a -m "work2 msg"

git log
git log --oneline
git log --oneline --all --graph

git commit --amend -m "msg ammended"

# HEAD: where you are right now
# master: refers to the latest change
# detached HEAD state: HEAD is not pointing at master

# checkout은 HEAD를 움직인다
git checkout 055d
git checkout master

# reset은 HEAD가 가리키는 branch를 움직인다 (e.g. master branch 자체를 움직임)
git reset --hard 624e

git reflog

# create a branch at where HEAD is
git branch exp

git tag release/1.0

# add remote and give it a name 'origin'
git remote add origin https://github.com/user/repo.git

git push --set-upstream origin master
git push

git fetch
git merge origin/master

# pull = fetch + merge
git pull

git remote -v
git remote rm origin
```
