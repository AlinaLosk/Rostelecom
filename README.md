# Roctelecom
Проект тестирования и автоматизации веб-сайта Ростелеком.
Тест-кейсы и баг-репорты расположены по ссылке:
https://docs.google.com/spreadsheets/d/1LUgb-yImSOMoXu1G-LeVTSACovr-bdqX0Ud8tIAeOnQ/edit?usp=sharing

Для тестирования сайта были разработаны как ручные, так и автоматизырованные тест-кейсы. 
Применены различные классы эквивалентности, анализ граничных значений в тестировании полей при регистрации и аутентификации пользователя.
Тест-кейсы созданы как позитивные, так и негативные.
Зафиксированы баг-репорты.

При работе с сайтом были использованы различные инструменты, а именно:
- сервис проверки названий багов bugred.ru;
- плагин для исследовательского тестирования bug magnet;
- попарное тестирование pairwise testing;
- расширение Xpath Helper;
- для создания и проектирования автотестов была использована платформа IDE PyCharm;
- для определения локаторов использовалась панель инструментов разработчика DevTools;
- библиотеки selenium версии 4.9.0 и pytest.

Для запуска автотестов необходимо установить библиотеки:
selenium 4.9.0
pytest 7.4.4
Также необходимо скачать драйвер для управления браузером под свою версию технических характеристик ПО и версию браузера.
Автотесты запускать через терминал с указанием пути до файла chromdriver.exe командой
python -m pytest -v --driver Chrome --driver-path <Путь до файла>/chromedriver.exe <название воспроизводимого файла>.py

В ходе работы по тестированию сайта столкнулась с проблемой, в виде белого окна и долгого ожидания ответа от сервера при подтверждении аутентификации 
по смс коду с невалидными данными.
https://disk.yandex.ru/d/c-fobg-lyQMKTA
При тестировании сайта часто блокировали (что является плюсом для пользователя), долгое ожидание кодов при повторном запрашивании. 
Приходилось возвращаться через определенное время к отладке автотестов из-за блокировки, что затягивато процесс.
