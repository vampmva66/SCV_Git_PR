![gitlogo](Git-Icon-1788C.png)
# Работа с Git и GitHub
## 1. Проверка наличия установленного Git
В терминале выполнить команду 
```
git version
```
Если Git установлен появится сообщение о версии программы, иначе будет сообщение об ошибке
## 2. Установка Git
Загружаем последнюю версию Git с [Официального сайта](https://git-scm.com/downloads).
Устанавливаем с настройками по умолчанию.
## 3. Настройка Git
При первом использовании Git необходимо представиться.
Для этого нужно ввести в терминале 2 команды:
```
git config --global user.name "Ваше имя английскими буквами"
git config --global user.email "Ваша почта"
```
## 4. Инициализация репозитория
В терминале переходим в папки, в которой хотим создать репозиторий. Выполняем команду :
```
git init
```
## 5. Запись изменений в репозиторий
После внесения изменений в файл их необходимо записать в репозиторий.
Сделать это можно при помощи команд :
```
git status - Для проверки наличия изменений которые можно записать.
git add "Название файла" - Для подготовки файла к записи.
git commit -m "Комментарий к коммиту" - Для того чтобы записать изменения.
``` 
## 6. Просмотр истории коммитов
Также в Git можно посмотреть историю всех коммитов. 
Команды для этого:
```
git log - для получения полной информации о коммите 
git log --oneline - для получения сокращенной информации
```
## 7. Перемещение между сохранениями
Для просмотра прошлых версий файла можно обратится к команде :
```
git checkout (номер сохранения)
git switch (номер сохранения)
```
## 8. Игнорирование файлов
Для того, чтобы исключить из отслеживания в репозитории определенного файла или папки, необходимо создать там файл 
***.gitignore*** и записать в него их названия или шаблоны, соответствующие этим файлам или папкам. 
## 9. Создание веток в Git
По умолчанию, имя основной ветки в Git - *main*. 
Создать ветку можно командой :
```
git branch <Название новой ветки>
```
Для того чтобы создать новую ветку и сразу перейти в неё используется команда:
```
git checkout -b <Название новой ветки>
```
Список веток в репозитории можно посмотреть с помощью команды :
```
git branch
``` 
Текущая ветка будет отмечена звездочкой:
* __main__
## 10. Слияние веток и разрешение конфликтов
Для слияния выбранной ветки к текущей нужно выполнить команду :
```
git merge <название выбранной ветки>
```
Если была изменена одна и та же часть файла в обеих ветках, то может возникнуть конфликт который потребует участия пользователя.
VSCode предлагает варианты разрешения.
Чтобы разрешить конфликт, нужно выбрать один из вариантов, либо объединить содержимое по своему.
После разрешения конфликта нужно выполнить коммит слияния
## 11. Удаление веток
Для удаления выбранной ветки можно использовать команду:
```
git branch -d <Название ветки>
```
Для принудительного удаления не объединённой ветки можно использовать команду:
```
git branch -D <Название ветки>
```
## 12. Работа с удалённым репозиторием
* Для начала нужно зарегестрироваться на [GitHub](https://github.com/)
* Создать локальный репозиторий
* Создать удалённый репозиторий(Если требуется)
* Связать удалённый репозиторий с локальным . Для этого используется команда:
```
git remote add <Имя репозитория> <url удалённого репозитория>
```
Для проверки наличия удалённого репозитория используется команда :
```
git remote
git remote -v для просмотра подробной информации
```
Далее нужно переименовать ветку master в main командой :
```
git branch -m main
```
Отправляем изменения в удалённый репозиторий командой :
```
git push -u <Имя репозитория> main
```
Если делает это впервые, то нужно авторизоваться на GitHub
Для получения и слияния изменений из удалённого репозитория используется команда :
```
git pull
```
## 13. Работа с чужим репозиторием
Для начала работы с чужим репозиторием нужно найти на GitHub функцию *fork* - которая позволяет скопировать репозиторий на свой аккаунт.
Когда вы перенесли репозиторий на свой аккаунт нужно клонировать его на локальный компьютер, сделать это можно с помощью команды :
```
git clone
```
Далее следует создать новую ветку, в которой и будет вестись работа.

После завершения работы необходимо отправить PullRequest