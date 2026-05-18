# ModbusTest

**ModbusTest** - консольный стенд для работы с COM-портом и подготовки к диагностике Modbus/POXS-устройств. Текущий snapshot проекта содержит базовый serial logger: приложение открывает выбранный COM-порт, читает входящие строки и пишет их в JSON-lines лог.

## Возможности текущей версии

- Интерактивная настройка COM-порта.
- Выбор `BaudRate`, `DataBits`, `Parity`, `StopBits`, `DTR` и `RTS`.
- Чтение строк из serial-порта.
- Вывод данных в консоль с timestamp.
- Запись событий в `log.json`.

## Запуск

Проект рассчитан на .NET Framework 4.7.2.

```powershell
nuget restore
msbuild SerialPortLogger.csproj /p:Configuration=Release
```

Или откройте проект в Visual Studio и запустите `SerialPortLogger.csproj`.

## Пример лога

```json
{"Timestamp":"2026-01-17T12:00:00","Message":"01 03 00 00 00 02"}
```

## Дальнейшее развитие

- Добавить Modbus RTU-запросы.
- Реализовать перебор адресов и регистров.
- Экспортировать найденную карту адресов в CSV/Excel.
- Добавить профили устройств POXS.

## Стек

- C#
- .NET Framework 4.7.2
- System.IO.Ports
- Newtonsoft.Json

## Лицензия

Проверьте лицензионные условия перед распространением.
