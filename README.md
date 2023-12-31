# ez-pre-commit

A simple bash script to manage your pre-commit hooks in a Git repository. This script creates a pre-commit hook file in your `.git/hooks` directory that checks for the existence of a `pre-commit.sh` script in the root of your repository. If the script exists and is executable, it runs it before each commit. Otherwise it yells for dear life. The `pre-commit.sh` script skeleton is placed upon installation so use that one and don't delete it.

## Features

- Installs a new pre-commit hook, backs up existing one if present
- Installs the `pre-commit.sh` script skeleton in the root of your repository
- Uninstalls the pre-commit hook and restores backup if available
- Logs every damn thing

## Installation

Run the following one-liner to download the script and make it executable in `~/bin`. Make sure `~/bin` is in your `PATH`.

```bash
curl -O https://raw.githubusercontent.com/psyb0t/ez-pre-commit/master/ez-pre-commit && chmod +x ez-pre-commit && mv ez-pre-commit ~/bin/
```

### Check if `~/bin` is in your `PATH`

Run the command:

```bash
echo $PATH | grep -q "~/bin" && echo "You're good" || echo "Add ~/bin to your PATH"
```

### Adding `~/bin` to your `PATH`

If `~/bin` isn't already in your `PATH`, add the following line to your `.bashrc`, `.zshrc`, or whatever shell config you use:

```bash
export PATH="$PATH:$HOME/bin"
```

After adding, run `source ~/.bashrc` or `source ~/.zshrc` to update the current session.

## Usage

### Install the pre-commit hook

```bash
ez-pre-commit install
```

### Uninstall the pre-commit hook

```bash
ez-pre-commit uninstall
```
