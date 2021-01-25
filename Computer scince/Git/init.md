# Git команды.

## Создание  папки  .git 

Это начальная команда. С ее помощью мы говорим что нужно следить за этой директорией.

```
git init
```



## Проверка статуса

Для проверки состояния файлов используем команду:

```
git status
```

Она покажет новые файлы и модифицированные. В таком виде:

```Git
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   "Computer scince/\320\241omputer science.md"
        new file:   English/ENG.md
        new file:   Main.md
        new file:   Math/Math.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   "Computer scince/\320\241omputer science.md"
        modified:   Main.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Computer scince/Git/
```



## Добавление в индекс

Для того чтобы начать отслеживать файл нужно  написать следующую команду:

```
git add <имя_файла>
```

Но можно сохранить сразу все файлы набрав команду

```
git add .
```

Тогда все файлы в директории будут добавлены в индекс 



## Отличии версий

```
git diff
```

Эта команда покажет разницу между двумя деревьями. 

между рабочей директорией и индексом `git diff`
или между индексом и послюним коммитом `git diff --staged`
или между двумя любыми коммитами `git diff master branchB`



## Создание слепка

Для создания "Слепка" нужно набрать команду:

```
git commmit 
```

Эта команда берет все данные в индексе и создает слепок.
Она откроет текстовый редактор для создания коммита.
Чтобы не открывать редактор можно набрать команду `-m`

Для того чтобы подписать коммит есть команда `-S`



## Push

Для того чтобы запушить на ГитХаб или куда-нибудь еще.
Надо сначала добавить сервер в который хотим пушить с список удаленных серверов.

```
git remote add origin <адресс самого сервера>
```

Origin это название сервера. Можно выбрать любое.

Проверить добавился сервер или нет можно с помощью команды:

```
git remote -v
```





## Проверка коммитов





