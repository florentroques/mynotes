## Install composer
ref: http://stackoverflow.com/a/29436655/1152843

```bash
cd ~
mkdir bin
mkdir bin/composer
curl -sS https://getcomposer.org/installer | php
mv composer.phar bin/composer
```

We need to determine the location of php-cli (needed later on).  
On 1and1 shared web hosting, there's no php-cli but phpX.X-cli commands  
We are going to use /usr/bin/php5.5-cli

edit ~/.bashrc and make sure this line is at the top, adding it if it is not:
```bash
[ -z "$PS1" ] && return
```
and then add some aliases:
```bash
alias php-cli="/usr/bin/php5.5-cli"
alias composer="php-cli ~/bin/composer/composer.phar"
```

Finish with these commands:

```bash
source ~/.bashrc
composer --version
```


##  Load aliases every SSH connection
ref: http://www.joshstaiger.org/archives/2005/07/bash_profile_vs.html
- Create a .bash_profile file
- insert following code to load the .bashrc file at every SSH connection
```bash
if [ -f ~/.bashrc ]; then
   source ~/.bashrc
fi
```
