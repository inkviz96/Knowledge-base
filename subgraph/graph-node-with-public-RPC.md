## Запуск graph-node c публичным RPC JSON

- Загружаешь проект [graph-node](https://github.com/graphprotocol/graph-node).
- В папке docker, правишь docker-compose.yml, изменяя graph-node -> environment -> ethereum прописываешь RPC JSON URL соотвествующей блокчейн сети.
- Запускаешь docker-compose up.

[Список RPC JSON для разных сетей](Rpc-json-endpoints.md)

**Плюсы:**

- Подсоединиться можно к любой сети.

**Минусы:**

- Публичные RPC JSON не стабильные.
