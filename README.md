# Установка имени и email (обязательно для коммитов)
git config --global user.name "Ваше Имя"
git config --global user.email "ваша@почта.com"

# Настройка редактора по умолчанию (например, VS Code)
git config --global core.editor "code --wait"

# Просмотр всех настроек
git config --list

# Инициализация локального репозитория
git init

# Клонирование удаленного репозитория
git clone https://github.com/username/repo.git

# Проверить статус репозитория (изменения, новые файлы)
git status

# Добавить файлы в индекс (подготовка к коммиту)
git add file.txt          # Добавить конкретный файл
git add .                 # Добавить все изменения

# Создать коммит
git commit -m "Сообщение коммита"

# Просмотр истории коммитов
git log
git log --oneline         # Краткий вывод
git log --graph           # Визуализация веток

# Создать новую ветку
git branch feature-branch

# Переключиться на ветку
git checkout feature-branch
# Или (в новых версиях Git):
git switch feature-branch

# Создать и переключиться на новую ветку
git checkout -b new-feature

# Удалить ветку
git branch -d old-branch

# Слияние веток (из ветки, куда вливаете изменения)
git merge feature-branch

# Переименовать текущую ветку
git branch -m new-name

# Добавить удаленный репозиторий
git remote add origin https://github.com/username/repo.git

# Отправить изменения в удаленный репозиторий
git push -u origin main    # Первый пуш (устанавливает связь)
git push                   # Последующие пуши

# Получить изменения из удаленного репозитория
git pull origin main

# Просмотр списка удаленных репозиториев
git remote -v

# Удалить связь с удаленным репозиторием
git remote remove origin

# Отменить изменения в файле (до добавления в индекс)
git restore file.txt

# Убрать файл из индекса (перед коммитом)
git reset file.txt

# Исправить последний коммит (изменить сообщение или добавить файлы)
git commit --amend

# Откатить коммит (создает новый коммит с отменой)
git revert хэш_коммита

# Откатить к предыдущему коммиту (осторожно: удалит историю!)
git reset --hard HEAD~1

# Показать разницу между рабочим каталогом и индексом
git diff

# Показать разницу между индексом и последним коммитом
git diff --staged

# Показать изменения в конкретном коммите
git show хэш_коммита

# Создать легковесный тег
git tag v1.0

# Создать аннотированный тег
git tag -a v1.1 -m "Версия 1.1"

# Отправить теги на удаленный репозиторий
git push --tags

# Сгенерировать SSH-ключ
ssh-keygen -t ed25519 -C "ваша@почта.com"

# Добавить ключ в ssh-agent (Linux/Mac)
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

# Скопировать публичный ключ (для GitHub/GitLab)
cat ~/.ssh/id_ed25519.pub

git log -S "текст"   # Поиск по изменениям
git grep "текст"     # Поиск в текущих файлах

# Справка по команде
git help <команда>
git <команда> --help

# Официальная документация: https://git-scm.com/doc

