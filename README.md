# Содержание
1. [**Системные требования**](https://github.com/AutoDealerRu/acat-online-example#Системные-требования)
2. [**Настройки**](https://github.com/AutoDealerRu/acat-online-example#Настройки)
3. [**Запуск**](https://github.com/AutoDealerRu/acat-online-example#Запуск)
4. [**Обновления**](https://github.com/AutoDealerRu/acat-online-example#Обновления)


# Системные требования 

- **apache** >= 2.2
- **composer**
- **php** >= 5.5


# Настройки

- **Установите пакеты используя один из вариантов**
    - ```php composer.phar install```
    - ```composer install```
- **Выполните  1 из вариантов** (создание файла с настройками)
    - через командную строку ```cp src/settings_example.php src/settings.php```
    - в ручную скопируте файл в папке ```src``` с именем ```settings_example.php``` в эту же папку и переименуйте в ```settings.php```
- **Укажите в файле настроек ```src/settings.php``` в 11 строке ваш API Token**
- Если каталог расположен не в корневой директории, а например по адресу **http://example.com/catalog** добавьте в файле настроек [src/settings.php](https://github.com/AutoDealerRu/acat-online-example/blob/master/src/settings.php#L13) ```catalog/``` чтобы ссылки работали корректно
- **Важно!** Если сайт индексируется поисковиками, настройте индексацию каталога так, чтобы избежать блокировки по лимитам (**используя файл robots.txt**)


# Запуск

## Используя composer (один из вариантов): 
- ```php composer.phar start```
- ```composer start```

## Используя php
- ```php -S 0.0.0.0:80 -t public public/index.php```

## Используя docker:

### Доп. требования:

- **docker**
- **docker-compose**
- **возможность использования docker (при размещении сайта на "общей" хостинг-площадке)**

### Для запуска введите:

```docker-compose up -d```


# Обновления

## 29.11.2017
### Исправлено:
- Поиск по номерам (актикулам) для марок **Mercedes Benz | Smart** (будет доступен 30.11.17)

## 28.11.2017
### Добавлено:
- Предварительный поиск по номерам (актикулам) для марок **Mercedes Benz | Smart**
### Исправлено:
- Ссылки и названия на уровне групп для марок **Mercedes Benz | Smart**

## 27.11.2017
### Добавлено:
- Поиск по номерам (актикулам) для марок **Abarth | Alfa Romeo | Lancia | Fiat**
- Поиск по номерам (актикулам) для марок **Audi | Seat | Skoda | Volkswagen**
- Поиск по номерам (актикулам) для марок **BMW | Mini | Rolls-Royce**
- Поиск по номерам (актикулам) для марок **Hyundai | Kia**
- Поиск по номерам (актикулам) для марок **Infinity | Nissan**
- Поиск по номерам (актикулам) для марок **Dacia | Renault**
- Поиск по номерам (актикулам) для марок **Toyota | Lexus**

## 26.11.2017
### Добавлено:
- Поиск по номерам (актикулам) и названиям запчастей для каталога a2d ([список типов и марок](https://github.com/AutoDealerRu/catalog-api-documentation/blob/master/a2d/README.md))

## 24.11.2017
### Добавлено:
- Типы ```get``` тепеменных в ```src/routes.php```
- Поиск по модели/марке/vin/frame
#### BMW | Mini | Rolls-Royce
- Серии
- Модели
- Группы
- Подгруппы
- Номера (артикулы) запчастей
#### Kia | Hyundai
- Страны и семейства
- Модели
- Модификации
- Группы
- Подгруппы
- Номера (артикулы) запчастей
### Исправлено:
- Вывод даты окончания производства

## 22.11.2017
### Добавлено:
#### Toyota | Lexus
- Модели
- Комплектации
- Группы
- Илюстрация и номера (артикулы) запчастей
#### Audi | Seat | Skoda | Volkswagen
- Модели
- Группы и сервисные группы
- Подгруппы
- Сервисные подгруппы
- Номера (артикулы) запчастей
- Сервисные номера (артикулы) запчастей

## 21.11.2017
### Добавлено:
- Вывод ошибки об отсутствии токена 
- Дополнена инструкция по установке 
#### Abarth | Alfa Romeo | Lancia | Fiat
- Модели
- Модификации
- Группы
- Подгруппы
- Номера (артикулы) каталога
#### Mercedes Benz | Smart
- Страны и агрегаты
- Модельный ряд
- Группы
- Номера (артикулы) каталога
#### Ssangyong
- Модельный ряд каталога
- Группы
- Номера (артикулы) каталога
### Исправлено:
- Параметры запуска в файле ```composer.json```

## 20.11.2017
### Добавлено:
#### Renault | Dacia
- Модельный ряд каталога
- Модификации каталога
- Группы
- Подгруппы
- Номера (артикулы) каталога
- Подномера (аналоги) каталога
#### Mercedes Benz | Smart
- Страны и аггрегаты каталога
- Добавлены все URL адреса (routing) каталога 
- Добавлены все представления (view) каталога (пока без содержимого) 

## 17.11.2017
### Добавлено:
#### Nissan | Infinity
- Модельный ряд каталога 
- Модификации каталога
- Группы
- Подгруппы
- Номера (артикулы) каталога
### Исправлено:
- Вывод даты актуальности запчасти (в информации по артикулу)

## 14.11.2017
### Добавлено:
- Главная страница с типами и марками
- Модельный ряд каталога a2d ([список типов и марок](https://github.com/AutoDealerRu/catalog-api-documentation/blob/master/a2d/README.md))
- Группы каталога a2d ([список типов и марок](https://github.com/AutoDealerRu/catalog-api-documentation/blob/master/a2d/README.md))
- Конечная страница номеров с изображением (точки, увеличение, уменьшение, движение изображения)