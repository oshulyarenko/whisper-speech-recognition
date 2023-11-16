### Set up virtual environment
```bash
# if you don't have pyenv, install pyenv
brew install pyenv
brew install pyenv-virtualenv
# if you do, update pyenv
brew upgrade pyenv
```

If this is the first time working with pyenv, the following
needs to be added to `~/.bash_profile`:

```bash
# pyenv and virtualenv
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

Now we can set up the virtual environment:

```bash
# this needs to happen if you've changed the ~/.bash_profile file
source ~/.bash_profile
# install the python version 3.9.9 needed for this repo
pyenv install 3.9.9
# go to the project folder
cd whisper-speech-recognition
# and create a virtual environment
pyenv virtualenv 3.9.9 whisper-speech-recognition
# then activate it.
pyenv activate whisper-speech-recognition
```

### Set up poetry
```bash
# if you don't have poetry, install poetry
brew install poetry
poetry install
```


### Run the speech recognition
Go to `whisper_speech_recognition` folder and run 
``` bash
# Go to 'whisper_speech_recognition' folder
cd whisper_speech_recognition
python transcribe_demo.py
```