Readme my dear friends  
HEAD -- это голова.  
Коммит -- это всему голова.  
Статусы файлов:  

```mermaid
  erDiagram;
    Untracked ----add the file----> Staged;
    Staged ---Commit---> Unmodified;
    Unmodified --Remove the file--> Untracked;
    Unmodified --Edit the file--> Modified;
    Modified --Stage the file--> Staged;
```
git commit --amend --no-edit *Исправить коммит*  
git commit --amend -m "" *Исправить коммит и название*  
git restore --staged <file> *Убрать файл из коммита*  
git reset --hard <commit hash> *Откатить коммит до hash*  
git restore <file> *Изменить файл*  
