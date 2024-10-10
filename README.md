1. Заходим на Microsoft store
2. Скачиваем и устанавливаем Windows terminal
3. Установить  posh-git, инструкции в ссылке (нужно для автозаполнения команд git)
https://github.com/dahlbyk/posh-git?tab=readme-ov-file
https://git-scm.com/book/ru/v2/%D0%9F%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5-A%3A-Git-%D0%B2-%D0%B4%D1%80%D1%83%D0%B3%D0%B8%D1%85-%D0%BE%D0%BA%D1%80%D1%83%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F%D1%85-Git-%D0%B2-PowerShell
4. Зайти на https://ohmyposh.dev/docs/installation/windows
5. winget install JanDeDobbeleer.OhMyPosh -s winget
6. Перезапустить терминал
7. Можете установить любую тему.
 oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\jandedobbeleer.omp.json" | Invoke-Expression
8. Только установленая выше тема исчезнет после перезагрузки. Скрипт должен срабатывать каждый раз при запуске.
 Команду выше записать в profile.ps1, она находится в C:\Users\{USERNAME}\Documents\PowerShell
9. Установка fonts, чтобы некоторые символы распазнавались. 
oh-my-posh font install meslo
10 открыть по пути C:\Users\{USERNAME}\AppData\Local\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json
Указать свойство profiles согласно инструкции в https://ohmyposh.dev/docs/installation/fonts
