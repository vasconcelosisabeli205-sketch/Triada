# --- 1. Подготовка локальной среды ---

# Выберите имя для вашего проекта (например, enhanced-repo-setup)
PROJECT_NAME="enhanced-repo-setup" 

# Создание и переход в новую директорию
mkdir $PROJECT_NAME
cd $PROJECT_NAME

# Инициализация Git
git init

# --- 2. Добавление основных файлов для улучшения качества репозитория ---

# Создание README.md
echo "# $PROJECT_NAME" > README.md
echo "" >> README.md
echo "Это улучшенный репозиторий, созданный с полным комплектом метаданных (README, .gitignore, LICENSE)." >> README.md
echo "## Начать работу" >> README.md
echo "Для клонирования используйте: \`git clone <URL>\`" >> README.md

# Создание .gitignore для игнорирования файлов Python и временных файлов
echo "# Игнорируем файлы Python" > .gitignore
echo "__pycache__/" >> .gitignore
echo "*.pyc" >> .gitignore
echo "*.log" >> .gitignore
echo ".DS_Store" >> .gitignore
echo "# Игнорируем файлы IDE (VS Code)" >> .gitignore
echo ".vscode/" >> .gitignore

# Добавление файла лицензии (MIT)
echo "MIT License" > LICENSE
echo "" >> LICENSE
echo "Copyright (c) 2025 <ВАШЕ_ИМЯ_ПОЛЬЗОВАТЕЛЯ>" >> LICENSE
# (В реальном проекте здесь нужно добавить полный текст выбранной лицензии)

# --- 3. Коммит и отправка на GitHub ---

# Добавление всех трех файлов к следующему коммиту
git add README.md .gitignore LICENSE

# Создание первого коммита
git commit -m "feat: Initial setup with README, MIT License, and .gitignore"

# Установка главной ветки
git branch -M main

# Привязка к удаленному репозиторию на GitHub
# !!! ОБЯЗАТЕЛЬНО ЗАМЕНИТЕ ЭТУ СТРОКУ !!!
# Замените <ВАШЕ_ИМЯ_ПОЛЬЗОВАТЕЛЯ> и project-name на свои значения
git remote add origin https://github.com/<ВАШЕ_ИМЯ_ПОЛЬЗОВАТЕЛЯ>/$PROJECT_NAME.git

# Отправка кода на GitHub
git push -u origin main
