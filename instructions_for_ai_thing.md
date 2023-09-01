# AI Code thingy

## Info
This is instructions for [DL-abstract-argumentation](https://github.com/DennisCraandijk/DL-abstract-argumentation)

## Install (Works for linux)

First install this package. Dont know what it is, but it makes everything work..... (Think its just a library)
```bash
sudo apt-get install libffi-dev
sudo apt-get install libbz2-dev
sudo apt-get install liblzma-dev
```

Compile requirements
```bash
sudo apt install ant
sudo apt install maven
```

Next install pyenv to manage python version
```bash
curl https://pyenv.run | bash
```

Next setup bash startup files
```bash
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init -)"' >> ~/.bashrc
```
```bash
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.profile
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.profile
echo 'eval "$(pyenv init -)"' >> ~/.profile
```
```bash
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile
echo 'eval "$(pyenv init -)"' >> ~/.bash_profile
```

Restart Terminal or run
```bash
exec "$SHELL"
```

Install required python version
```bash
pyenv install 3.8.18
```

Change python version of the terminal window
```bash
pyenv shell 3.8.18
```

Create venv in correct location with version 3.8.18
```bash
python -m venv venv
```

Enter venv
```bash
source venv/bin/activate
```

Pip install [pytorch](https://pytorch.org/). I selected stable, linux, pip, python, cpu and that worked for me.

Pip install pytorch geometry
```bash
pip install git+https://github.com/pyg-team/pytorch_geometric.git
```

Pip install requirements file
```bash
pip install -r requirements.txt
```

Pip install torch_sparse
```bash
pip install torch_sparse
pip install torch_scatter
```

## Testing

Run tests
-s runs with sudo privelages
```bash
pytest tests/test_components.py -s
```
Make sure `src/data/solvers/vendor/mu-toksia/mu-toksia_static` is set as an executable file and give permissions. Right click on file, allow execution tickbox.
