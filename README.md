# Неофициальный SDK для Tinkoff Invest APIv2 для nodejs

Tinkoff Invest API — это интерфейс для взаимодействия с торговой платформой [Тинькофф Инвестиции](https://www.tinkoff.ru/invest/).

# Почему lazy?

В SDK заранее не используется предгенерации классов из proto-файлов и описания статичных объектов и методов. 

Генерация объектов поисходит каждый раз в момент подключения класса.

Минус в производительности, так же как и не рекомендуется многократно создавать экземпляр объекта в своем коде. 

Плюсом является простота обновления SDK и легкая адаптация под любой другой сервис.

Для обновления SDK под новую версию достаточно загрузить новые proto-файлы в папку proto


# Функциональные возможности
* автоматическая генерация SDK на основе proto-файлов
* поддержка Unary-request
* поддержка Bidirectional streaming RPC
* поддержка callback
* поддержка promise (для unary-request)

# Об API и протоколе
API реализован на быстром, удобном и функциональном протоколе [gRPC](https://grpc.io/docs/).

[Документация для разработчиков](https://tinkoff.github.io/investAPI/)


# Как работать с этим репозитарием

* В [Issues](https://github.com/Tinkoff/investAPI/issues) вы можете задать вопрос или найти ответ касаемый сервиса Тинькоф - инвестиций.
* В данном репозитории рекомендуется задвать вопросы по конкретно данному SDK

* Если вы встретили неточность или хотели бы что-то дополнить или исправить, то буду рад принять от вас pull request.


# Примеры работы

* Примеры находятся в папке example
* node example/unaryPromise.js token

# Особенности использования 

Для того чтобы использовать Promise к названию объекта необходимо прибавить постфикс "Promise". 

Например объект api.InstrumentServicePromise.ShareBy(json) это версия с promise, а api.InstrumentService.ShareBy(json, callback) это версия с callback.

Список объектов и методов удобно смотреть через kreya (https://tinkoff.github.io/investAPI/grpc/), оттуда так же можно копировать примеры JSON запросов и проводить debug протокола либо через swagger https://tinkoff.github.io/investAPI/swagger-ui/#/

# Установка

* Копируете репозиторий в папку с проектом
* В папке репозитория npm install
* Актуальные proto-контракты https://github.com/Tinkoff/investAPI/tree/main/src/docs/contracts


# Сообщество

[Telegram-чат](https://t.me/joinchat/VaW05CDzcSdsPULM)
