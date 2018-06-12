# VSCode Templates
[![made-for-VSCode](https://img.shields.io/badge/Made%20for-VSCode-1f425f.svg)](https://code.visualstudio.com/)

This repository holds template projects for vscode in various languages. Recommended tools and instructions for building can be found on the README in each folder.

# Basic Usage

The templates in this repository can be used to create a new application through two methods.


## Subversion

This method does not require the repository to be cloned locally. To use this method, [Subversion](https://subversion.apache.org/) must be installed and available through the command line. 

Simply use the following command to download the desired template from GitHub into the specified directory:

```
svn export https://github.com/renanbasilio/vscode-templates.git/trunk/{template} {myproject}
```

This will download the specified {template} into the folder {myproject} without linking it to the original repository.


## Local Copy

Alternatively, clone the repository locally and copy the desired template to your project directory.

```
git clone https://github.com/renanbasilio/vscode-templates.git templates
cp templates/{template} {myproject} -r
```