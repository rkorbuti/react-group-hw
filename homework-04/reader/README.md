# Читатель публикаций

Необходимо усовершенствовать
[гаджет читателя публикаций](../../homework-02/reader), добавив функционал
хранения номера текущей публикации в `URL`. Компонент `Reader` должен парсить
строку запроса из `URL`. Для парса можно использовать пакет
[query-string](https://www.npmjs.com/package/query-string) или
[qs](https://www.npmjs.com/package/qs).

Например, если пользователь находится на четвертой публикации, то `URL` выглядит
так:

```bash
имя_хоста/reader?item=4
```

- При переходе между публикациями должно изменяться значение параметра `item`.
- Если пользователь зашел по адресу в котором нету параметра `item`, то есть
  `имя_хоста/reader`, его должно перенаправить на `имя_хоста/reader?item=1`.
- Если пользователь зашел по любому другому адресу, например
  `имя_хоста/someroute`, его необходимо перенаправить на `имя_хоста/reader`. Для
  такого перехода будет удобно использовать компонент `Redirect` от
  `react-router`.