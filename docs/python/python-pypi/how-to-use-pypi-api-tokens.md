# How to Use PyPI API Tokens

## Using The Token

To use the PyPI API token:
```
Set your username to __token__
Set your password to the token value, including the pypi- prefix
```

For example, if you are using Twine to upload your projects to PyPI, set up your $HOME/.pypirc file like this:
```
[testpypi]
  username = __token__
  password = <token_value>
```

For further instructions on how to use this token, visit the PyPI help page.

***

*Updated on 1 August 2025*
