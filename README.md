# sandbox4notebook

<img src="https://avatars1.githubusercontent.com/u/7388996?v=3&s=400" width="200px;">

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

## Activate Venv
```
source activate venv
source deactivate
```

## Launch Jupyter Notebook
```
jupyter contrib nbextension install --user
jupyter notebook
```

## Contribution
1. Fork it ( https://github.com/zdogma/sandbox4notebook/fork )
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create new Pull Request

## Author
<img src="https://avatars3.githubusercontent.com/u/1973683?v=3&s=460" width="45px;" style="margin-right: 10px;">
[zdogma](https://github.com/zdogma/)
