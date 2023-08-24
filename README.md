# Python template repo

This repo is designed around developing Python AWS CDK projects in VS Code but could be used for other types of Python projects.

## Formatting and linting

In requirements-dev.txt there are a 3 packages that are used for formatting and linting. These are:

- flake8 - Linting
- isort - Formatter just for sorting imports
- black - General formatter

With the recommended extensions installed (listed in .vscode/extensions.json) VS Code will use flake8 to lint the code and provide hinting in the editor, and isort + black to format the code on save. The settings for these are in .vscode/settings.json. 

The settings are mostly default but black is given the --line-length=100 override (default is 88).

If you want to run the linters and formatters manually or on entire directories you can run them from the command line once they are installed from requirements-dev.txt. Examples:

```bash
black --line-length=100 .

isort .

flake8 .
```