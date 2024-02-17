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

