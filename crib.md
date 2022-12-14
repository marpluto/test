# Шпаргалки по GIT здесь

## Базовые команды:
- git init инициализация локального репозитория
- git status проверяем статус папки
- git add -A добавить все содержимое папки в репозиторий (начать отслеживать)
- git commit -m "<имя коммита>" создать коммит (первый коммит исторически называют "Initial commit")
-  git log --oneline посмотреть историю изменений (коротко, можно посмотреть развереуто без флага --oneline)
- git branch без флагов выводит все существующие ветки нашего локального репозитория
- git branch <имя новой ветки> создать новую ветку
- git branch -a посмотреть все ветки
- git checkout <имя ветки> преключиться на ветку
- git merge <имя ветки, из которой мы забираем изменения> слить ветку в ту, где мы сейчас находимся (обычно main)
- git log --graph – oneline <имя ветки> Просмотр истории ветки в терминале Git
- git checkout -b <имя новой ветки> создать новую ветку и сразу переключиться на нее
- git commit -a -m "<имя коммита>" одновременно добавить все содержимое папки в репозиторий и создать коммит (работает только с уже отслеживаемыми файлами)

## Работа с GIThub:
- git remote -v проверка, есть ли сейчас связь с удаленным репозиторием
- git remote add origin <СкопированныйАдресРепозитория> здесь origin - это ожидаемое имя для первой связки с удаленным репозиторием; последующие связки могут называться как угодно
- git remote remove origin (или другое имя связки с удаленным репозиторием) - удалить связку
- git push -u origin main Отправка локальных файлов в удаленный репозиторий с кодовым именем origin
- git push -u origin <имя ветки> Отправка новой ветки в удаленный репозиторий по связке (алиасу/псевдониму) origin
- git push можно писать коротко, если ветка не новая (уже залита на гитхаб)
- git clone <ссылка на форкнутый репозиторий> - копировать себе на комп репозиторий из гитхаба


## Если не получается залить локальный репозиторий на гитхаб:
- …or create a new repository on the command line
- echo "# testtest" >> README.md
- git init
- git add README.md
- git commit -m "first commit"
- git branch -M main
- git remote add origin git@github.com:marpluto/testtest.git
- git push -u origin main

- …or push an existing repository from the command line
- git remote add origin git@github.com:marpluto/testtest.git
- git branch -M main
- git push -u origin main