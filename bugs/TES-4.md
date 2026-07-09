# [Console] Видеоплагин reloadSourceOnError регистрируется дважды — дублирующая ошибка в консоли при авторизации

## Описание
В DevTools во вкладке console обнаружено предупреждение дублирующегося включения плагина reloadSourceOnError

## Предусловие
Открыт браузер Google Chrome с включёнными DevTools (F12 → Console).
Пользователь находится на странице demoblaze.com

## Шаги воспроизведения
1. Открыть https://demoblaze.com
2. Открыть DevTools → вкладка console
3. Нажать кнопку "Log in" в шапке сайта

## Ожидаемый результат
Форма авторизации не содержит ошибок, предупреждений, не дублируется включение плагина 

## Фактический результат
В DevTools → Console появляется предупреждение:
`VIDEOJS: WARN: A plugin named "reloadSourceOnError" already exists.` You may want to avoid re-registering plugins!
Плагин регистрируется дважды — скрипт videojs-contrib-hls.min.js подключён на странице повторно

## Среда
- ОС: Windows 10, 64bit
- Браузер: Google Chrome 149.0.7827.201 (64 бит)
- Страница: https://demoblaze.com

## Приоритет
Low

## Severity
Minor
