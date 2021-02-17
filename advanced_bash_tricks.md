##### 1. Copy files verbosely to another dir and log the successfull operation one in success.txt and the errors in error.txt
`$ cp -v * ../newfolder 1> ../success.txt 2> ../error.txt`
##### 2. Change specific part of string
```
names="john elay means danny osman"
echo ${names/danny/ellen}
john elay means ellen osman
echo $names
john elay means danny osman
```
