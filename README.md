[![Telegram channel](https://img.shields.io/endpoint?url=https://runkit.io/damiankrawczyk/telegram-badge/branches/master?url=https://t.me/XardMoney)](https://t.me/XardMoney)
[![PyPI supported Python versions](https://img.shields.io/pypi/pyversions/better-automation.svg)](https://www.python.org/downloads/release/python-3116/)
# Общая информация
Данный софт поможет вам в прогреве аккаунтов для получения дропа в сетях ZkSync и Base. Он автоматизирует транзакции различного типа, а так же имеет гибкую настройку под ваши нужды.

## 💡Основные особенности  
+ _Рандомизация действий и задержек_
+ _Поддержка и проверка html/socks proxy_
+ _Защита от price impact на всех DEX_
+ _Обратные свапы_
+ _Логирование внутри GUI и в текстовый файл_
+ _Сбор неотработавших аккаунтов в текстовые файлы_
+ _Сохранение последних выставленных настроек_

## Подготовка Python для запуска софта
### 1. Установка Python  
Переходим по ссылке `https://www.python.org/downloads/release/python-3116/` и скачиваем версию под своё устройство. Далее запускаем установщик, **ОБЯЗАТЕЛЬНО** нажимаем на галочку `Add Python x.x to PATH`.  
### 2. Установка репозитория  
Нажимаем на `Code -> Download ZIP`, после скачивания разархивируем архив в любое место на вашем устройстве. Важно **НЕ ИМЕТЬ** пробелов и кириллицы в пути до папки.  
### 3. Установка необходимых библиотек  
Переходим в командную строку и пишем `cd ПолныйПутьДоПапки` (например, cd C:\Xard-Progrev-Python), после чего пишем `pip install -r requirements.txt` и ждем окончания установки.  
### 4. Запуск софта  
В той же консоли пишем `python filename.py`, где filename - название файла. В данном случае пишем `python main.py`. Готово!  
Также можно работать в интерпретаторе, гайдов на ютубе полно.

## 🧩 DApps
    1.  Grape           ZkSync и Base | (Покупка дешевых лотерейных билетов)                             
    2.  Dmail           ZkSync и Base | (Отправка зашифрованных электронных писем)
    3.  ZkStars         ZkSync и Base | (Минт NFT)
    4.  Izumi           ZkSync и Base | (Свап в stablecoin и обратно)
    5.  WooFi           ZkSync и Base | (Свап в stablecoin и обратно)
    6.  Maverick        ZkSync и Base | (Свап в stablecoin и обратно)
    7.  SyncSwap        ZkSync | (Свап в stablecoin и обратно)
    8.  SpaceFi         ZkSync | (Свап в stablecoin и обратно)
    9.  Uniswap         Base | (Свап в stablecoin и обратно)
    10. PancakeSwap     Base | (Свап в stablecoin и обратно)

## ⚙️ Настройки
После скачивания открываем файл `xard progrev.exe`, после чего переходим к настройке софта через GUI:
+ `Путь до аккаунтов` - путь до файла .txt, в котором хранятся приватные ключи (_поддерживаются оба формата, с "0x" в начале и без_).
+ `Обзор...` - выбрать файл .txt, в котором хранятся приватные ключи через проводник.
+ `Количество транзакций` - количество транзакций, которое будет сделано на **КАЖДОМ** выбранном DApp (_можно указать как число (например - 1), так и диапазон (например, 1-10), во втором случае значение будет каждый раз выбираться рандомно_). Ограничений нет.
+ `Процент от баланса в свапе` - процент от баланса ETH, который будет использоваться при свапе (_можно указать как число (например - 10), так и диапазон (например, 10-40), во втором случае значение будет каждый раз выбираться рандомно_). В обратных свапах будут задействованы **ВСЕ** stablecoin'ы. Ограничения: минимум - 0.1, максимум - 80. Введенные значения вне данных рамок будут округлены до граничных (например, 95 округлится до 80, 0-95 округлится до 0.1-80).
+ `Билетов в GrapeDraw` - количество лотерейных билетов, которое будет куплено за одну транзакцию (_можно указать как число (например - 1), так и диапазон (например, 1-10), во втором случае значение будет каждый раз выбираться рандомно_). Ограничения: минимум - 1. Введенные значения вне данных рамок будут округлены до граничных (например, 0 округлится до 1).
+ `Максимальный price impact` - максимально допустимый price impact при свапе, при его привышении транзакция не будет выполнена. Slippage не входит в этот процент. (_можно указать только число (например - 2)_). Ограничения: минимум - 0.1, максимум - 100. Введенные значения вне данных рамок будут округлены до граничных (например, 0 округлится до 0.1).
+ `Секунд между транзакциями` - задержка между выполнением транзакций (_можно указать как число (например - 10), так и диапазон (например, 10-30), во втором случае значение будет каждый раз выбираться рандомно_). Ограничения: минимум - 5. Введенные значения вне данных рамок будут округлены до граничных (например, 1 округлится до 5).
+ `Секунд между аккаунтами` - задержка между прокруткой аккаунтов (_можно указать как число (например - 10), так и диапазон (например, 10-30), во втором случае значение будет каждый раз выбираться рандомно_). Ограничения: минимум - 5. Введенные значения вне данных рамок будут округлены до граничных (например, 1 округлится до 5).
+ `Перемешивать аккаунты` - перемешивать аккаунты или же идти по порядку.
+ `Использовать proxy` - использовать прокси (выбираться будут рандомно) или же нет.

Ниже в GUI представлен выбор DApps для каждой сети, которые вы хотите использовать во время прокрутки.

После выполненной настройки нажмите на кнопку `Начать работу скрипта` и наслаждайтесь результатом :)

## 🗂️ Файлы
+ `abi` - эту папку **НЕ ТРОГАТЬ**, там хранится код контрактов всех DApps.
+ `files/config.json` - последние выставленные настройки, лучше **НЕ ТРОГАТЬ**.
+ `files/log.txt` - логи за всю историю работы софта.
+ `files/private_keys.txt` - создан для вашего удобства, можете поместить сюда ваши приватные ключи и выбрать этот файл при настройке.
+ `files/proxy_list.txt` - прокси, которые будут использоваться, если выставить соотвествующую галочку при настройке.

Следующих файлов не будет при скачивании, но они будут созданы при необходимости:
+ `files/failed_zksync.txt` - приватные ключи аккаунтов, на которых не проходили транзакции в сети ZkSync.
+ `files/failed_base.txt` - приватные ключи аккаунтов, на которых не проходили транзакции в сети Base.
+ `files/invalid_private_keys.txt` - некорректные приватные ключи.
+ `files/no_working_proxies.txt` - приватные ключи аккаунтов, при прокрутке которых не было рабочих прокси (при соответсвующей настройке).

# DONATE (_any EVM_) - 0x34810639cCCef6E5e0501bdda08D59E284d0Aa70
