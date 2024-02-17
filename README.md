Readme my dear friends
flowchart TB
  Untracked ----add the file----> Staged;
  Staged ---Commit---> Unmodified;
  Unmodified --Remove the file--> Untracked;
  Unmodified --Edit the file--> Modified;
  Modified --Stage the file--> Staged;

