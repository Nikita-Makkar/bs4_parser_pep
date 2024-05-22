### Парсер для документации Python и PEP
## Описание:
Этот парсер на Python предназначен для извлечения информации с различных страниц, связанных с документацией Python и PEP (Python Enhancement Proposals). Он предоставляет функционал для получения данных о новых функциях в Python, последних версиях Python, загрузке ресурсов и статусах PEP.

## Установка

Скачайте репозиторий с помощью команды Git:

```
git clone https://github.com/Nikita-Makkar/bs4_parser_pep
```

Установите зависимости

Перейдите в каталог с загруженным репозиторием и установите зависимости из файла requirements.txt:

```
cd your_repository
pip install -r requirements.txt
```

## Использование
```
python parser.py <mode> [-c] [-o <output_mode>]
```

Аргументы командной строки

Парсер принимает аргументы командной строки для определения режима работы и дополнительных опций. Доступные режимы следующие:

- whats-new: Получить информацию о новых функциях в Python.
- latest-versions: Получить данные о последних версиях Python.
- download: Скачать ресурсы, связанные с документацией Python.
- pep: Извлечь информацию о статусах PEP.
## Дополнительные опции включают:
- --c, --clear-cache: Очистка кеша запросов.
- -o, --output <output_mode>: Дополнительные способы вывода данных. Доступные режимы: pretty (красивый вывод в консоль), file (запись в файл).
- -h, --help: Показать сообщение справки и выйти.

Пример использования:

```
python parser.py whats-new
```
## Функции

Парсер предоставляет следующие функции:

- whats_new(session): Получить информацию о новых функциях в Python.
- latest_versions(session): Получить данные о последних версиях Python.
- download(session): Скачать ресурсы, связанные с документацией Python.
- pep(session): Извлечь информацию о статусах PEP.
## Детали реализации
- Кэширование: Парсер использует requests-cache для кэширования HTTP-ответов, что позволяет снизить количество запросов к серверу.
- Логирование: Логирование реализовано с использованием встроенного модуля logging Python для предоставления информации о выполнении парсера и об ошибках, которые могут возникнуть.
- Парсинг HTML: Парсинг HTML выполняется с помощью BeautifulSoup, что позволяет парсеру навигироваться по структуре HTML и извлекать нужную информацию.
- Интерфейс командной строки: Парсер принимает аргументы командной строки для определения режима работы и дополнительных опций.
- Обработка ошибок: Парсер обрабатывает HTTP-ошибки, отсутствующие элементы и другие исключения корректно, предоставляя информативные сообщения пользователю.
## Лицензия
Этот парсер выпущен под лицензией MIT. Вы можете найти полный текст лицензии в файле LICENSE.


## Автор
[Nikita-Makkar](github.com/Nikita-Makkar)


Благодарности
Отдельное спасибо разработчикам библиотек requests, requests-cache, beautifulsoup4 и tqdm за их отличные библиотеки, использованные в этом парсере.
