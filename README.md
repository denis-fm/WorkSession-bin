# Рабочий режим / WorkSession

Небольшая Windows-утилита: при входе в систему спрашивает, запускать ли набор рабочих приложений. Список программ настраивается в окне: добавление, удаление, включение и перетаскивание ярлыков.

A small Windows app that asks at logon whether to start your work applications. The list is managed in a window: add, remove, enable/disable, and drag-and-drop shortcuts.

---

# Русский

## Возможности

- Список рабочих программ с включением и выключением
- Добавление приложений и ярлыков, в том числе перетаскиванием
- Вопрос «Сегодня работа?» при входе в Windows, с таймером
- Запуск только отмеченных программ, уже запущенные пропускаются
- Установка для текущего пользователя или для всех, удаление через «Параметры → Приложения»

## Как пользоваться

1. Скачайте установщик из [Releases](https://github.com/denis-fm/WorkSession-bin/releases/latest).
2. Запустите `WorkSession-Setup-1.0.1.exe`.
3. Выберите установку только для себя или для всех пользователей, при желании включите ярлык на рабочем столе и вопрос при входе в Windows.
4. Откройте программу, добавьте нужные ярлыки и включите те, которые должны стартовать.

Windows 10/11, нужен [.NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework/net48) (обычно уже установлен).

Исходный код в этом репозитории не публикуется.

### SHA256 (v1.0.1)

`WorkSession-Setup-1.0.1.exe`

```
A3BA8FAFDDB03D15FF1C224FEF66739552205B767E5A887885E4D933AC8F321E
```

Проверка в PowerShell:

```powershell
Get-FileHash .\WorkSession-Setup-1.0.1.exe -Algorithm SHA256
```

## Если Windows блокирует запуск

Файл не подписан сертификатом, SmartScreen может показать «Windows защитила ваш компьютер».

**Подробнее** → **Выполнить в любом случае**.

## Приватность

Нет телеметрии и скрытых запросов в сеть. Список программ хранится локально в `%AppData%\WorkSession`.

---

# English

## Features

- Enable or disable each work app
- Add programs and shortcuts, including drag-and-drop
- Optional “Is this a work day?” prompt at Windows logon, with a timeout
- Starts only checked apps and skips ones that are already running
- Per-user or all-users install; uninstall from Settings → Apps

## How to use

1. Download the installer from [Releases](https://github.com/denis-fm/WorkSession-bin/releases/latest).
2. Run `WorkSession-Setup-1.0.1.exe`.
3. Choose current-user or all-users install. Optionally create a desktop shortcut and enable the logon prompt.
4. Open the app, add shortcuts, and check the ones that should start.

Windows 10/11, requires [.NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework/net48) (usually already installed).

Source code is not published in this repository.

### SHA256 (v1.0.1)

`WorkSession-Setup-1.0.1.exe`

```
A3BA8FAFDDB03D15FF1C224FEF66739552205B767E5A887885E4D933AC8F321E
```

```powershell
Get-FileHash .\WorkSession-Setup-1.0.1.exe -Algorithm SHA256
```

## If Windows blocks the app

The executable is not code-signed. SmartScreen may show “Windows protected your PC”.

**More info** → **Run anyway**.

## Privacy

No telemetry and no background network calls. Settings are stored locally in `%AppData%\WorkSession`.
