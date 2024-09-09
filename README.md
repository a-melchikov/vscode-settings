# Резервная копия настроек VS Code

Этот репозиторий содержит мои личные настройки Visual Studio Code и список установленных расширений для удобной синхронизации между разными компьютерами.

## Как создать резервную копию настроек VS Code

- Настройки пользователя хранятся в файле `settings.json`, бинды в `keybindings.json`. Эти файлы можно найти по следующим путям:

  - **Windows**: `C:\Users\<username>\AppData\Roaming\Code\User\`
  - **Linux**: `/home/<username>/.config/Code/User/`

- Чтобы сохранить список установленных расширений, выполните команду в терминале VS Code:

  ```bash
  code --list-extensions > extensions.txt
  ```
- Это создаст файл extensions.txt, содержащий список всех установленных расширений.

## Как восстановить настройки на другом компьютере

- Клонируйте репозиторий с настройками:

  ```bash
  git clone https://github.com/<ваш-username>/vscode-settings.git
  ```
- Скопируйте файлы настроек в нужную директорию:

  - **Windows**: `C:\Users\<username>\AppData\Roaming\Code\User\`
  - **Linux**: `/home/<username>/.config/Code/User/`

- Установите расширения из файла extensions.txt:

  ```bash
  cat extensions.txt | xargs -n 1 code --install-extension
  ```
  
