![Logo](Git-Logo-1788C.png)
# Работа с Git и GitHub
## 1. Проверка наличия установленного Git
В терминале выполнить команду: 
```
git version (git --version)
```
Если Git установлен, появится сообщение о версии программы, иначе появится сообщение об ошибке.
## 2. Установка Git
Загружаем последнюю версию Git с сайта [Установка Git](https://git-scm.com/downloads). 
Устанавливаем с настройками по умолчанию.
## 3. Настройка Git
При первом использовании Git необходимо представиться.
Для этого нужно ввести в терминале 2 команды:
```
git config --global user.name «Ваше имя английскими буквами»
git config --global user.email ваша почта@example.com
```
## 4. Инициализация репозитория
В терминале переходим к папке, в которой хотим создать репозиторий. Выполняем команду:
```
 git init 
 ```
 ## 5. Запись изменений в репозиторий
 * Если Вы хотите посмотреть текущее состояние Git, есть ли изменения, которые нужно сохранить, то воспользуйтесь командой:
 ```
 git status
 ```
 * Для того, чтобы начать отслеживать добавленную информацию, воспользуйтесь командой: 
 ```
 git add FileName.FileExtension
 ```
Писать название файла целиком не обязательно: воспользуйтесь клавишей `Tab` и терминал дозаполнит данные автоматически.

Если нужно добавить изменения из всех файлов или у вас всего один файл, то можно воспользоваться:
```
git add .  или  git add --all
 ```
 * Чтобы зафиксировать (сохранить) изменения, нужно вспользоваться командой:
 ```
 git commit -m "A comment".
 ```
 *Существует общая функция для команд `git add` и `git commit`, позволяющая одновременно добавлять содержимое всех файлов и сохранять их:*
 ```
 git commit -a -m "A comment"
 ```
 * Чтобы показать разницу между текущим файлом и сохраненным, воспользуйтесь командой:
 ```
 git diff
 ```
 ## 6. Просмотр истории коммитов  
 ```
 git log
 ```
 Если нет необходимости подробно показывать историю коммитов, то можно вспользоваться командой:
 ```
 git log --oneline
 ```
 ## 7. Перемещение между сохранениями 
 ```
 git checkout CommitNumber
 ```
 *Достаточно первых 4-5 символов номера коммита.*

 Для работы нужно указать не только интересующий вас коммит, то и вернуться в тот, где работаете, при помощи команды:
 ```
 git checkout master
 ```
 ## 8. Игнорирование файлов 
 Для того, чтобы исключить из отслеживания в репозитории определённые файлы или папки,  необходимо создать там файл  ***.gitignore*** и записать в него их названия или шаблоны, соответветствующие таким файлам или папкам. 

 ## 9. Создание веток в Git
 По умолчанию имя основной ветки в Git - *master*. 
 Создать ветку можно командой:
 ```
 git branch <название для новой ветки>
 ```
 Список веток в репозитории можно посмотреть с помощью команды: 
 ```
 git branch
 ```
 Текущая ветка будет отмечена звездочкой: **\* master**.

## 10. Слияние веток и разрешение конфликтов
Для слияния выбранной ветки с текущей нужно выполнить команду:
```
git merge <название выбранной ветки>
```
Если была изменена одна и та же часть файла в обеих ветках, то может возникнуть конфликт, который потребует участия пользователя.
VSCode предлагает варианты разрешения.
Чтобы разрешить конфликт, нужно выбрать один из вариантов либо объединить содержимое по-своему. 

После разрешения конфликта нужно выполнить коммит слияния.

## 11. Удаление веток
Если созданная ветка больше не нужна, то её можно удалить с помощью команды: 
```
git branch -d <название выбранной папки>
```

## 12. Визуализация всех веток 
Чтобы отобразить коммиты в виде дерева, нужно выполнить команду:
```
git log --graph
```
Если нет необходимости показывать подробно всю историю коммитов, то можно воспользоваться уже знакомой командой:
```
git log --graph --oneline
```