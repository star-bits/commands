# Terminal commands cheat sheet

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
kill `PID`

# hidden files
ls -al

# shell restart
source ~/.bashrc
# or 
. ~/.bashrc

# current shell
echo $SHELL

# enable shell
bash

# download
wget https://url_example.com/file_name

# tar: create, view, extract
tar cvf A.tar A
tar tvf A.tar
tar xvf A.tar
```

## vi
```
vi file_name.txt

# Switch to Insert mode
i

# Switch to Command mode
`ESC`

# Switch to Last Line mode
:

# quit (at Last Line mode)
q
# write and quit (at Last Line mode)
wq
```

## venv
```
python3 -m venv xvnv

source xvnv/bin/activate
deactivate

pip freeze

# to activate xvnv automatically:
nano ~/.zshrc
# and write following two lines:
cd ~/x
source xvnv/bin/activate
# restart zsh by:
source ~/.zshrc
```

## virtualenv
```
virtualenv --python=python3 xvlv

source xvlv/bin/activate
deactivate

pip freeze
```

## brew
```
brew install miniconda
brew uninstall miniconda
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

## jupyter
```
# http://localhost:8888/tree
jupyter notebook

# http://localhost:8888/lab
jupyter lab

# http://localhost:8888/voila
voila
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
