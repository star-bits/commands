# misc.

```
# disk usage
du -sh *

# list count
ls | wc -l

rm img_{1..10}.jpg

nvidia-smi -l 1

# process status
ps -ef
kill `PID`
```

# brew

```
brew install miniconda
brew uninstall miniconda
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
conda create --name xcda python=3.8

conda activate xcda
conda deactivate

conda env list

# packages can be installed from anaconda, conda-forge, or pypi (pip).

# requirements.txt equivalent
conda env export --file environment.yml 
conda env create -n xcda -f /path/to/environment.yml
conda env update -n xcda -f /path/to/environment.yml

conda env remove -n xcda
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

# HEAD: points at the working directory
# master: refers to the latest change

git checkout 055d
git checkout master

git reset --hard 624e

git reflog

git branch exp

git tag release/1.0

git remote add origin https://github.com/user/repo.git

git push --set-upstream origin master
git push
```
