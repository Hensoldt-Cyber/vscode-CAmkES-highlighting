# Visual Studio Code plugin for CAmkES syntax hihlighting

* written in a REGEX dialect called tmLanguage [tmLanguage](https://macromates.com/manual/en/language_grammars)
* Work in progress: If you encounter a bug please send me a screenshot -> maybe it could be published to the vscode extension market place when mature
* This reuses some parts of the official [Microsoft C syntax extension](https://github.com/microsoft/vscode/tree/main/extensions/cpp) which is published under the MIT License -> though only some parts are copied, a distribution under MIT might be ?neccessary?


## Installation

### Prepackaged version


Download the prepackaged package [camkes-syntax-highlighting-0.0,7.vsix](https://wiki.hensoldt-cyber.systems/download/attachments/14844307/camkes-syntax-highlighting-0.0.7.vsix?version=1&modificationDate=1637335449603&api=v2)


``` 
code --install-extension camkes-syntax-highlighting-0.0.*.vsix
```



### Package it yourself


Nodejs  version 14.0.0 or higher is required to package the extension. The apt repositories are currently only supporting version v10.0.0 but we can update it over the npm package manager.

```
sudo apt install nodejs npm
sudo npm cahe -clean -f
sudo npm install -g n
sudo n stable
```



To package we need the vsce package

```
sudo npm install vsce
```



We then need to clone the repo and package it

```
git clone ssh://git@bitbucket.hensoldt-cyber.systems:7999/hc/vscode-camkes-syntax-highlighting.git
cd vscode-camkes-syntax-highlighting
vsce package
```



install the package

```
code --install-extension camkes-syntax-highlighting-0.0.*.vsix
```

