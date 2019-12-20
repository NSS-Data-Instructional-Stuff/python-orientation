# Installations

## Python via Pyenv

### XCode Prerequisite

For `pyenv` to install correctly, you need the Xcode command line tools. Type the following command into your terminal and wait for the installation to complete.

```
xcode-select --install
```

### Install Pyenv

```bash
brew install pyenv
pyenv install 3.7.3
pyenv global 3.7.3
```

Now, when you check the version of Python with the command below, it should return 3.7.3.

```
python --version
```

#### Troubleshooting pyenv


If it still returns a different version, you will need to edit your `~/.zshrc` file. Add the following to the bottom of the file.

```sh
# Configure pyenv
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"

if command -v pyenv 1>/dev/null 2>&1; then
  eval "$(pyenv init -)"
fi
```

## Python Linter

Run the following command to install the linter we will all be using during Python development.

```sh
pip install -U pep8
```

## TablePlus

[TablePlus](https://tableplus.io/) will let you view, query and manage your SQLite databases during the course. Visit their site and click the "Download for Mac" button.

Lastly, setup an alias for TablePlus. Open the `~/.zshrc` initialization file - which is in your home directory - in your favorite code editor, and enter in the following alias.

```sh
alias tableplus="open -a """TablePlus""" "
```

Save the file, and reload your init file with the source command in the terminal.

```sh
source ~/.zshrc
```
