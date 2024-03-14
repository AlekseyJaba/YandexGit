Readme my dear friends  
HEAD -- это голова.  
Коммит -- это всему голова.  
Статусы файлов:  
mkdir - *создание directory*  
touch - *создание файла*  
rm - *удаление файла*  
cat - *чтение файла*  
```mermaid
  erDiagram;
    Untracked ----add the file----> Staged;
    Staged ---Commit---> Unmodified;
    Unmodified --Remove the file--> Untracked;
    Unmodified --Edit the file--> Modified;
    Modified --Stage the file--> Staged;
```
git diff - *Показывает что изменилось внутри файлов*  
git diff --staged - *Покажет изменения на этапе staged*  
git log oneline - *все коммиты в сокр виде*  
git commit --amend --no-edit *Исправить коммит*  
git commit --amend -m "" *Исправить коммит и название*  
git restore --staged <file> *Убрать файл из коммита*  
git reset --hard <commit hash> *Откатить коммит до hash*  
git restore <file> *Изменить файл*  
git clone <SSH> - *Скопировать репозиторий*  
git branch - *список веток в проекте*  
git branch <Название веток> - *создаёт ветку*  
git checkout <название ветк> - *переход в новую ветку*  
git merge <ветку которую нужно срастить с текущей> - *Слияние веток*  
git branch -D <имя_ветки> - *Удаление ветки*  
git pull - *залить с удалённого репозитория*  
git push - *залить на репозиторий (если ветка только создана то будет ссылка для pull request)*  
git remote rm origin - *Удаление текущего origin*  
---  
### Погружаемся  
#### **FAST-FORWARD**  
**Ситуация FAST-FORWARD**  
![image](https://github.com/AlekseyJaba/YandexGit/assets/113855518/19ea1154-ede8-4dba-9172-b02995065ba1)  
**результат merge fast-forward**  
![image](https://github.com/AlekseyJaba/YandexGit/assets/113855518/2435433f-7d06-43d5-a3cf-fe9f15369c40)  
git merge --no-edit --no-ff add-docs - *merge без fast-forward*
*--no-edit - отключает сообщение для merge commit*  
*--no-ff - отключает fast foreward*  
git log --graph --oneline - *графически в консоди отображает все commitы*  
**А ЭТО РЕЗУЛЬТАТ БЕЗ FAST-FORWARD**  
![image](https://github.com/AlekseyJaba/YandexGit/assets/113855518/479b6f14-a401-4bba-8c27-a40934f1fff3)  
---  
#### **NON FAST-FORWARD**  
**Ситуация**  
![image](https://github.com/AlekseyJaba/YandexGit/assets/113855518/b284c40d-f0e0-40fe-865d-92a450a0185e)  
git merge --no-edit add-docs  
**результат**  
![image](https://github.com/AlekseyJaba/YandexGit/assets/113855518/ade9c893-024f-4d62-b6fe-1e15846ed874)  
---  
#### **Подход к ведению проекта в GIT**  
*Feature branch workflow* — `простой и самый популярный вариант.  
Если коротко, в нём для каждого нового изменения создаётся новая ветка,  
которая позже вливается в main с помощью git merge.`  
*Git flow* — `более сложный вариант. Подход похож на feature branch workflow,  
но в нём создаётся больше веток, а изменения (коммиты) делят на разные типы:  
исправление, новая функциональность и так далее. Разные типы коммитов попадают в разные ветки.`  
**LGTM (англ. Looks Good To Me — «на мой взгляд, всё хорошо»). `иногда вместо кнопки Approve используют комент при pull-request`**  



