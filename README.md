# sandbox4chainer
chainer トレーニング

## Install
### pyenv
```
brew install pyenv
echo 'export PYENV_ROOT="${HOME}/.pyenv"' >> ~/.bash_profile
echo 'export PATH="${PYENV_ROOT}/bin:$PATH"' >> ~/.bash_profile
echo 'eval "$(pyenv init -)"' >> ~/.bash_profile
```

### pip-tools
```
pyenv exec pip install pip-tools
pyenv exec pip install pip-review
pyenv exec pip install pipdeptree
```

## Setup Requirements
### load & save
```
pyenv exec pip-compile requirements/dev.in
pyenv exec pip install -r requirements/*.txt
```

### update
```
pyenv exec pip list --outdated
 or
pyenv exec pip-review

pyenv exec pip-review -i
```
