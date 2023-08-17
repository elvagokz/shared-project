# Создаём всё для git

## Создаём локальный git

1. Устанавливаем git
2. Создаём каталог для проекта и переходим в него
3. Вводим команду ***git init*** для инициализации
4. Создаем нужные файлы и папки
5. Когда всё создали вводим команду ***git add all*** или ***git add*** и далее списко файлов, которые вы хотите поставить в очередь на добавление в коммит.
6. Если решили что все файлы поствленны в очередь вводим команду ***git commit -m "Тут пишем коментарий, что поменялось"***

## Сойдаём github

1. Переходим в [github](https://github.com) и регистрируемся
2. Создаём репозиторий нажав на ***New***. В ***Repository name*** вводим имя нового репозитория. Ставим отметку на ***Public*** и жмём на ***Create repository*** 
3. На локальном сервере вводим команду  чтобы сгенерировать ssh ключи
 
```bash
ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub"
```
4. Копируем ключ из ~/.ssh/id_ed25519.pub 
5. Переходим в github на ***setings-SSH and GPG keys-New SSH key***. Задаём Title и в поле Key вставляем свой ключ. Жмём на ***Add SSH key***
6. В своём репозитории выбрать ***ssh*** и скопировать адрес
7. На локальном компе ввести команду  ***git remote add origin *тут скопированный адрес****
8. Если не вышло ошибки и команда git remote -v показывает список связаных репозиториев, то вводим команду ***git push -u origin main***. для синхронизации локального и удалённого репозитория.
9. В будущем при добавлении файлов достаточно будет команды ***git push***

## Немного о коммитах

### git ведёт лог коммитов. Увидеть его можно набрав ***git log***
### В логе можно увидеть информацию об авторе, дете создания коммита и комментарий.
### У каждого коммита есть свой хэш - информация о коммите в SHA-1 из 40 символов.
### Самый последний коммит имеет статус HEAD. Увидеть более подробную информацию по нему можно в файле ***.git/HEAD***
###
## Статусы файлов

### Все файлы в git имеют статусы ***untracked/tracked, staged и modified***
### ***Untracked*** - это новые добавленные файлы.
### ***Tracked*** - это проиндексированные файлы, готовые к добавлению в коммит
### ***Staged*** - это изменённые но не проиндексированные файлы 
### ***Modified** - это закомиченные файлы.

