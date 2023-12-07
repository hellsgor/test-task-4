# test task 4

## Задача:

Создайте Angular приложение для отображения данных о npm пакетах со следующим интерфейсом:

* На старте приложение должно отправить запрос для загрузки данных о пакетах (см. раздел API);


* Каждый пакет должен быть представлен в виде карточки:

  * Заголовок должен отображать имя пакета. В случае если имя составное (через /), первая часть должна быть выделена цветом;

  * Тело должно содержать число скачек и зависимостей. В случае если число превышает 1000, оно должно быть округлено вниз до тысяч с буквой «К»;

  * При наведении курсора на карточку её заголовок должен быть подсвечен, а также другим цветом должны быть подсвечены заголовки всех карточек пакетов, находящихся в зависимостях у выделенного пакета (в примере tslib является зависимостью @angular/core);


* Список пакетов должен быть скроллируемым
  Пользователь должен иметь возможность фильтровать пакеты по названию


* Пользователь должен иметь возможность перезагрузить все данные по кнопке или иным способом

## API

Для тестирования используйте API на nodejs: https://github.com/MrCelestis/mock-interview-api
GET /packages – возвращает список всех пакетов:

```
{
id: string;
weeklyDownloads: number;
dependencyCount: number;
}[]
```

GET /packages/:id/dependencies – возвращает список ID пакетов-зависимостей для указанного пакета: `string[]`

## Прочие замечания

* Использование сторонних библиотек разрешено;


* Стиль интерфейса и его проработанность - на усмотрение (сложный интерфейс с анимациями и т.п. не учитывается при оценке).
