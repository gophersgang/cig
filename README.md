<h1 align="center">cig</h1>

<p align="center">
  <a href="https://github.com/stevenjack/cig/releases" target="_blank"><img src="https://img.shields.io/github/release/stevenjack/cig.svg"></a>
  </p>

<p align="center">
	Can I go? CLI app for checking the state of your git repositories.
</p>

![cig](https://cloud.githubusercontent.com/assets/527874/7220202/faaedf0c-e6b6-11e4-9cb8-bf62295f4128.png)

### Installation

To install cig follow the instructions for your os below:

#### OSX/Linux

##### One line install

You can run the following that downloads the binary and changes the execute
permission on it:

```bash
curl -L http://bit.ly/1Hm2Llh | sudo bash
```

##### Manual install

```bash
curl -L https://github.com/stevenjack/cig/releases/download/v0.1.0/cig_`uname -s`_`uname -m` > /usr/local/bin/cig
chmod +x /usr/local/bin/cig
```

### Windows

Download the following binary:

* [32bit](https://github.com/stevenjack/cig/releases/download/v0.1.0/cig_windows_386.exe)
* [64bit](https://github.com/stevenjack/cig/releases/download/v0.1.0/cig_windows_amd64.exe)

then run it in a cmd prompt:

```
C: cig_windows_amd64.exe
```

### Setup

First create the following yaml file in your home directory:

> ~/.cig.yaml

```yaml
work: /path/to/work/repos
personal: /path/to/personal/repos
```

this is a list of the different folders that contain your repos you want to check.

### Usage

Simply run:

`$: cig`

and all repos will be checked and the following will show up:

* Repos that need pushing up to the origin (P)
* Repos that have new, unstaged and staged changes (M(10))

#### Filters

If you just want to check your 'work' repos for changes:

`$: cig -t work`

To filter them based on a certain string such as 'steve':

`$: cig -f steve`

You can also combine them, so to only show 'work' repos with 'steve' 
in the path:

`$: cig -t work -f steve`
