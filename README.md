# Terminal commands cheat sheet

## sh
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
wget https://website_name.com/file_name

# tar: create, view, extract
tar cvf A.tar A
tar tvf A.tar
tar xvf A.tar

# zip
zip -er A.zip A

# history
history
!42

# grep
ls | grep "vi"
history | grep "vi"
```

## vi
```
vi file_name.txt

# switch to Insert Mode
i

# switch to Command Mode
`ESC`

# switch to Last Line Mode
:

# quit (at Last Line Mode)
q
# write and quit (at Last Line Mode)
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
brew install scrcpy
brew install rename
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

## poetry
```
# install poetry
curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python -
source $HOME/.poetry/env

# create pyproject.toml
poetry init

# activate virtual environment
poetry shell

# create poetry.lock
poetry install
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
```
# to check the current kernel in jupyter notebook:
import sys

if hasattr(sys, 'base_prefix'):
    print(f"base: {sys.base_prefix}")

if hasattr(sys, 'real_prefix'):
    print(f"real: {sys.real_prefix}")

if hasattr(sys, 'prefix'):
    print(f"prfx: {sys.prefix}")
```

## tmux
```
apt-get install tmux

tmux new -s session_name

tmux ls

tmux attach -t session_name

tmux kill-session -t session_name
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
git remote add origin https://github.com/user_name/repo_name.git

git push --set-upstream origin master
git push

git fetch
git merge origin/master

# pull = fetch + merge
git pull

git remote -v
git remote rm origin
```
