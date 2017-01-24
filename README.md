# sandbox4chainer
chainer トレーニング

## Install
### pyenv
```
brew install pyenv
brew install pyenv-virtualenv
echo 'export PYENV_ROOT="${HOME}/.pyenv"' >> ~/.bash_profile
echo 'export PATH="${PYENV_ROOT}/bin:$PATH"' >> ~/.bash_profile
echo 'eval "$(pyenv init -)"' >> ~/.bash_profile
```

### tools
```
pyenv exec pip install pip-tools
pyenv exec pip install pip-review
pyenv exec pip install pipdeptree
pyenv exec pip install wheel
```

## Setup Requirements
### load & save
```
pyenv exec pip-compile requirements/dev.in
pyenv exec pip install -r requirements/*.txt --use-wheel --no-index --find-links=tmp/wheelhouse
```

### update
```
pyenv exec pip list --outdated
# or
# pyenv exec pip-review

pyenv exec pip-review -i
```

### compile
```
pyenv exec pip wheel --wheel-dir=tmp/wheelhouse -r requirements/dev.txt
```

## Activate Vitrualenv
```
source activate venv
source deactivate
```
