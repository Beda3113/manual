# Алгоритм выполнения задания
## №1 Создание локального репозитория

- на рабочем столе выбрать папку предназначенную для локального репозитория (далее ПАПКА), нажмите не неё правой клавишей мыши, выберите Показать дополнительные параметры → GIT Bash here.
- Чтобы прицепить Git к папке — создать локальный репозиторий — нужно выполнить команду git init. После выполнения команды в терминале появится строчка:

  Initialized empty Git repository in .../Desktop/test/.git/

- Чтобы проверить создан ли локальный репозиторий, открыть папку ПАПКА в проводнике на компьютере и найдите там папку .git

## №2 Скринкаст 

  Настройка отслеживания "название файла" (далее ФАИЛ) и создание его снимка
### отслеживания файла
- Чтобы проверить текущее состояние репозитория, введите в терминале команду git status. 
В ответ Git выдаст следующее сообщение, где файл ФАИЛ выделен красным
- Чтобы добавить файл в отслеживаемые, выполнить в терминале команду
git add + ФАИЛ
- Если всё введено верно, то компьютер молча выполнит команду
### Commit (коммит) 
Процедура, при которой делается снимок файла (папки) в текущем состоянии 
- Выполнить команду git commit -m "add ФАИЛ". 
- Выполнить команду git status, чтобы убедиться, что все файлы попалив снимок проекта


# Удалённый репозиторий на GitHub: создание, настройка и отправка проекта

## Создание удалённого репозитория на GitHub и его связь с локальным репозиторием в Git
1. [сылка] (https://github.com/new) 
2. В поле Repository name ввести название удалённого репозитория. 
3. Нажмить на кнопку Create repository
4. ссылка на новый репозиторий. В верхней строке нажмить SSH и на иконку двух квадратов (скопировать сылку) в конце этой строки
5. Открыть терминал для папки
6. Проверить, что к папке ещё не привязан никакой удалённый репозиторий можно
выполнив команду git remote -v. Git ничего не ответит если к папке ничего не привязоно 
7. Создать связь между локальным и удалёнными репозиториями 
git remote add ПАПКА ссылка на папку удалённого репозитория
1. Выполнить команду git remote -v. 
- Если потребуется удалить связь, то можно использовать команду 
git remote remove название связи, которая больше не нужна.  
После этого список связей снова будет пуст

## Отправка проекта в удалённый репозиторий
Чтобы отправить что-то в удалённый репозиторий, нужно воспользоваться командой
git push -u ПАПКА main. Обратите внимание, что мы указываем, по какому пути отправлять
проект — прописываем имя связи ПАПКА