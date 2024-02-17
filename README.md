Readme my dear friends
```mermaid
flowchart TB
  A[Untracked] ----add the file----> D[Staged];
  D ---Commit---> B[Unmodified];
  B --Remove the file--> A;
  B --Edit the file--> C[Modified];
  C --Stage the file--> D;
```
