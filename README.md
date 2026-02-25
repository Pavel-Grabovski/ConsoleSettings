### Скачивание  Windows terminal
1. Заходим на Microsoft store
2. Скачиваем и устанавливаем Windows terminal

### Автозаполнение команд Git
_Нужно будет проверить работает  ли автозаполнение на данном этапе_
Инструкция находится по адресу:
https://github.com/dahlbyk/posh-git?tab=readme-ov-file

https://git-scm.com/book/ru/v2/%D0%9F%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5-A%3A-Git-%D0%B2-%D0%B4%D1%80%D1%83%D0%B3%D0%B8%D1%85-%D0%BE%D0%BA%D1%80%D1%83%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F%D1%85-Git-%D0%B2-PowerShell

И сайт ohmyposh: https://ohmyposh.dev/docs/installation/windows

1. Выполнить команду `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser`
2. Выполнить команду `Install-Module posh-git -Scope AllUsers -Force`
3. Выполнить команду `Import-Module posh-git`
4. Выполнить команду `Add-PoshGitToProfile -AllHosts`
5. Выполнить команду `winget install JanDeDobbeleer.OhMyPosh -s winget`

### Установка темы
- Установить тему jandedobbeleer.omp.json: `oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\jandedobbeleer.omp.json" | Invoke-Expression`
- _Моя тема устанавливается по команде:_ `oh-my-posh init pwsh --config 'https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/main/themes/unicorn.omp.json' | Invoke-Expression`

Только установленая выше тема исчезнет после перезагрузки. Скрипт должен срабатывать каждый раз при запуске.
 Команду выше записать в profile.ps1, она находится в C:\Users\{USERNAME}\Documents\PowerShell или WindowsPowerShell

Может возникнуть проблема политики выполнения PowerShell. 
- Тогда надо выполнить команду `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser`

Подробнее о политики можно почитать:
https://learn.microsoft.com/ru-ru/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7.5

### Установка fonts, чтобы символы распазнавались. 
1. Скачать шрифты: `oh-my-posh font install meslo`
2. Oткрыть по пути C:\Users\{USERNAME}\AppData\Local\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json
3. Указать свойство profiles согласно инструкции в https://ohmyposh.dev/docs/installation/fonts

После выполнения шрифты должны распознаваться
