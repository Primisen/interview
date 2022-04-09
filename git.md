#### 1. Merge vs Rebase
Обе комманды предназначены для внесения изменений из одной ветки в другую, но делают они это по-разному.
 Итак 
Git merge: 
![alt-текст](https://github.com/Primisen/interview/blob/master/pictures/git-merge.png "merge")

Git rebase: 
(P.S. из ветки feature сделан rebase ветки main)
![alt-текст](https://github.com/Primisen/interview/blob/master/pictures/git-rebase.png "rebase")

Еще про rebase.
Как делать не надо (из ветки main сделан rebase ветки feature):
![alt-текст](https://github.com/Primisen/interview/blob/master/pictures/git-rebase-BAD-practice.png "так делать не надо")


#### 2. cherry-peak
Позволяет забрать коммит из одной ветку и вставить ее в текущую. 

#### 3. Как из нескольких коммитов сделать одни? 
`git squash`

#### 4. Состояния файлов
изменён (__modified__), индексирован (__staged__) и зафиксирован (__committed__)

#### 5. Жизненный цикл файлов
Unmodified -> Modified -> (git add) -> Staged -> (git commit) -> Unmodified

#### 6. interactive rabse
Инструмент для исправления коммитов.

#### 7. `git stash` и `git stash applye`
`git stash` - откладывает изменения
`git stash applye` - возвращает отложенные изменения
