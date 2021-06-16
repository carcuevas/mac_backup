# Script for Make some Local backup of one user in MacOS/Linux

## Requirements:

### In Mac
Install the following 

```
brew install coreutils gnupg
```

## Why another script for this

Well actually I did it because I wanted some script which will not create any Link, and will not touch the current files and it will just compress as it is, and also since there can be some secrets in the backup, at least to have the possibility to encrypt the tar with `zip` maybe in the future I could use another tools ...

I got inspired by this one: https://github.com/lra/mackup. 


##  File lists to do the backup

## Important  the etc/example_list copy as etc/${USER}_list
```
cp etc/example_list  etc/${USER}_list
```

and then modify `etc/${USER}_list` as needed...

## Configuring files in the `etc/${USER}_list`  

* Every line starting with `!` it means that it would be excluded
* The files/directories not starting with `/` they will be understood as `~/` for example: `.ssh` it will understood as `~/.ssh` but for example `/etc/hosts` will be understood as it is...
* As a help to see what files to be included I recommend to have a look to other similar project https://github.com/lra/mackup/tree/master/mackup/applications  
