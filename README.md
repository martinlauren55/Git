# Git
Instructions for working with Git


# Команды по работе с Git

**git --version** - Узнать версию git</br>

**git init** - Инициализировать пустой репозиторий</br>

**git add {file}** - Добавить файл {file} в будущий коммит</br>

**git status** - Просмотр измененные файлы которые еще не добавлены в коммит</br>

**git commit -m "commit_text"** - Создание коммита **commit_text** текст коммита</br>

**git log** - Отображает все созданные коммиты</br>

**git rm --cached {file}** - Удаляем файл из отслеживания</br>
**git rm {file}** - Удаляем файл из отслеживания Но так-же и с компьютера</br>

**git mv {old.name} {new.name}** - Позволяет переименновывать файл</br>

**git add -p {file}** - Добовление файла частично, т.е. только изменения в файле (**-p** - partial )</br>

Опции:
- y -  Добавить целиком этот фрагмент
- n - Не добавлять этот фрагмент
- q - Выйти из этой команды и не добавлять ничего
- a - Поместить этот фрагмент и все последующие фрагменты в файл
- d - Не размещайть этот фрагмент или любой другой, если более поздние фрагменты в файле
- s - Разделить текущий фрагмент на более мелкие части и добавить маленькими частями
- e - Отредактируйте текущий кусок вручную
- ? - Напечатать справку</br>

**.gitignore** - Файл в котором описано что не нужно отслеживать </br>

**git show** - Отображает последний созданный коммит</br>

**git diff {hash}** - Отображает изменения в коммитах (Предварительно выполнить команду git log и узнать hash коммита)</br>

**git diff HEAD~{1}** - Отображает изменения в коммита (Самый последний коммит имеет цифру 1)</br>

**git diff HEAD~{1} HEAD~{2}** - Отображает изменения между коммитами</br>

**git diff {file}** - Отображает изменения в файле который еще не закомичен и не добавен в индекс</br>

**git diff --name--only {hash}** - Отображает какие были файлы задействованы в этом коммите</br>

**git restore {file}** - Отменить изменения в файле (вернуть до состояния после коммита)</br>

**git restore --staged {file}** - Отменяет добовление файла в индекс (git add file)</br>

**git commit --amend** - Позволяет изменить имя коммита, добавить описание  и берет индекс в рабочей дерриктории и добавляет в последний коммит</br>

**git revert {hash}** - Отменить коммит (Делает новый коммит и удаляет изменения которые были в коммите)</br>

**git reset --hard {hash}** - Удаляет все новые коммиты после коммита с **hash** </br>

**git reset --hard** - Удаляет изменения и возвращают к состоянию последнего коммита</br>

**git reset --soft** - Удаляет изменения и возвращает все срезанные коммиты в index (отслеживание) либо **git reset**</br>

**git commit -a -m "commit_text"** - Добавляет в коммит все изменения</br>

**git fetch** - Принимает изменения с удаленного сервера но не сливает их, позволяет сравнить разницу в версиях</br>

**git diff master..origin/dev** - Отобразятся изменения в ветке master **origin** - имя репозитория **dev** - имя ветки</br>

**git pull** - Зальются все изменения с сервера в проект</br>

**git push** - Загрузить изменения на сервер</br>

**git push -u origin {name_branch}** - Загрузить изменения в конкретную ветку. **origin** - имя репозитория</br>

**git checkout -b {new_brench}** - Создание новой ветки</br>

**git branch -m {old_branch_name} {new_branch_name}** - Переименнование ветки</br>

**git branch -l** - Список всех веток в проекте</br>

**git branch -d {branch_to_delete}** - Удалить ветку по её названию (удаляет локально)</br>

**git push --delete origin {branch_to_delete}** - Удалить ветку по её названию (удаляет c сервера) **origin** - имя репозитория **{branch_to_delete}** - имя репозитория для удаления</br>

**git checkout {exist_brench}** - Переключение на другую ветку</br>

**git remote** - Список всех удаленных серверов</br>

**git remote -v** - Список адрессов удаленных серверов</br>

## Слияние и разрешение конфликтов

**git merge {name_branch}** - Слияние веток в одну (перейти на нужную ветку main и слить в нее изменения из dev)</br>