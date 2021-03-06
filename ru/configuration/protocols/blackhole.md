# Backhole

[![Английский](../../resources/english.svg)](https://www.v2ray.com/en/configuration/protocols/blackhole.html) [![Китайский](../../resources/chinese.svg)](https://www.v2ray.com/chapter_02/protocols/blackhole.html) [![Немецкий](../../resources/german.svg)](https://www.v2ray.com/de/configuration/protocols/blackhole.html) [![Русский](../../resources/russian.svg)](https://www.v2ray.com/ru/configuration/protocols/blackhole.html)

Backhole - это протокол для исходящих соединений. Он блокирует все соединения предопределёнными ответами. В сочетании с [Маршрутизацией](../routing.md), он может быть использован для блокировки доступа к определённым веб-сайтам.

* Название: blackhole
* Тип: исходящий
* Конфигурация:

```javascript
{
  "response": {
    "type": "none"
  }
}
```

Где:

* `response`: Предопределённый ответ на входящий запрос. Если задан, Backhole немедленно отправит его в ответ на запрос и закроет соединение. 
  * `type`: Тип ответа, доступные параметры: 
    * `"none"`: Значение по умолчанию. Пустой ответ.
    * ` "HTTP" `: Ответ кодом состояния HTTP 403 Forbidden.