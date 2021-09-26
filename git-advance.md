### 1 Show git logs in a efficient way
```
git config --global alias.sla 'log --oneline --decorate --graph --all'
git sla 
```
### 2 Custom Log Format
```
git log --pretty=format:'%h - %an [%ar] %s'
```
Here is the
```
Placeholder	Value
%h	Abbreviated commit hash
%an	Author name
%ar	Commit authored on date, relative (e.g. "3 days ago")
%s	Commit subject (first line of the commit message)
```
 ### 3 Searching the Logs by Commit Message
 ```
git log -E -i --grep 'change' #searching commits contains change
 ```
