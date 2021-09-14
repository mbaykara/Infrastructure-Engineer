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
#### Chech a speficif prefix
```
 if [ -n "$(echo $SEEKED_NAME | grep -lE 'feature|release|main')" ]; then echo  "VALID BRANCH NAME"; else echo -e "\033[4;31m USE ONLY ALLOWED PREFIXES AS BRANCH NAME see '$ALLOWED_PREFIXES' "; exit 1; fi;
 ```
#### Delete a dir recusively
```
find . -type d -iname <DirName> -exec rm -rf "{}" \;
```
