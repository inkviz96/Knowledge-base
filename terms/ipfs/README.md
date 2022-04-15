### Содержание
- [Что такое IPFS](#IPFS)
- [Как работает](#как-работает)
- [Как запустить](#как-запустить)
- [IPFS и блокчейн](#ipfs-и-блокчейн)
- [Примеры загрузки файлов в сеть](#примеры-загрузки-файлов-в-сеть)
- [Примеры получения файлов из сети](#примеры-получения-файлов-из-сети)

### IPFS
IPFS (InterPlanetary File System, «межпланетная файловая система») — это гипермедийный протокол связи с открытым кодом, с помощью которого одноранговые узлы хранят и распространяют данные в единой распределенной файловой системе. [Сайт проекта](https://ipfs.io/)
  
### Как работает?
В IPFS, как и в BitTorrent, данные непосредственно хранятся на системах участников, которые обмениваются информацией в режиме P2P, без привязки к централизованным узлам. Для получения файла с нужным содержимым система находит участников, у которых имеется данный файл и отдаёт его с их систем частями в несколько потоков. После загрузки файла на свою систему участник автоматически становится одной из точек по его раздаче. Для определения участников сети на узлах которых присутствует интересующий контент используется распределённая хэш таблица (DHT).

При этом при загрузке информации в IPFS адрес для доступа к файлу формируется с привязкой не к серверу, а к его уникальному криптографическому хешу-идентификатору(Content Identifier, CID). В связи с чем адрес файла невозможно произвольно переименовать, он может измениться только после изменения содержимого. Аналогично невозможно внести изменение в файл без изменения адреса(старый вариант останется на прежнем адресе, а новый будет доступен через другой адрес, так как хэш от содержимого файла изменится).

### Как запустить?
- Самый простой способ начать использовать - [IPFS Desktop](https://docs.ipfs.io/install/ipfs-desktop/), официальный программный пакет от Protocol Labs. Он доступен для Windows, Mac и Ubuntu и позволяет вам устанавливать и управлять собственным узлом, чтобы добавлять собственные файлы в сеть.
 
- Также можно использовать [IPFS Companion](https://docs.ipfs.io/install/ipfs-companion/#install) - это надстройка веб-браузера, доступная для Chrome, Edge, Brave, Firefox и Opera. Он позволяет взаимодействовать с рабочим столом IPFS и установленным узлом IPFS прямо из браузера, добавляя поддержку адресов ipfs://

- Кроме того, получить доступ к содержимому IPFS можно используя общедоступный шлюз, например https://ipfs.io или https://cloudflare-ipfs.com. Шлюз автоматически перенаправит к содержимому IPFS.

- Для любителей консоли или для установки на удаленный сервер можно использовать консольный клиент. Подробный процесс установки - [Установка клиента](https://docs.ipfs.io/install/command-line/)

**Пример загрузки файла в сеть**
```bash
$ ipfs add mytextfile.txt
added QmZtmD2qt6fJot32nabSP3CUjicnypEBz7bHVDhPQt9aAy mytextfile.txt
```
```QmZtmD2qt...``` - хэш содержимого, а не сам файл. При изменении файла — изменится (присвоится новый) и хэш файла в сети.
Если же содержимое файла не изменится, то и хэш останется прежним.

**Пример получения файла из сети IPFS**<br/>
Как было сказано ранее, при загрузке файла в сеть ipfs - ему присваивается уникальный кэш.
По хэшу можно прочитать файл, и если необходимо, записать его содержимое:

```bash
$ ipfs cat QmTudJSaoKxtbEnTddJ9vh8hbN84ZLVvD5pNpUaSbxwGoa > mytextfile.txt
```
 
### IPFS и блокчейн
IPFS органически связан с технологией блокчейн. Используя IPFS внутри транзакции блокчейна, можно размещать ссылки на файлы в сети ipfs, без необходимости их реального хранения в самом блокчейне, что приводит к уменьшению вздутия цепочки блоков. При этом обе системы являются immutable, что обеспечивает безопасность и гарантирует состояние содержимого.

Ярким пример такой сингулярности сервис - [Pinata](https://www.pinata.cloud/) это служба хостинга NFT, которая использует IPFS для резервного копирования криптографических предметов коллекционирования для таких партнеров, как Rarible и Sorare.

Документация по сервису и примеры javascript - [https://docs.pinata.cloud/](https://docs.pinata.cloud/)

Другой популярный сервис - [https://infura.io/](https://infura.io/)

### Примеры загрузки файлов в сеть

#### Typescript
Простой пример загрузки файла в сеть
```typescript
/* import the ipfs-http-client library */
import { create } from 'ipfs-http-client'

/* Create an instance of the client */
const client = create({
  url: 'https://ipfs.infura.io:5001/api/v0'
})

function App() {
  const [fileUrl, updateFileUrl] = useState(``)
  async function onChange(e) {
    const file = e.target.files[0]
    try {
      /* upload the file */
      const added = await client.add(file)
      const url = `https://ipfs.infura.io/ipfs/${added.path}`
      updateFileUrl(url)
    } catch (error) {
      console.log('Error uploading file: ', error)
    } 
}
```

### Примеры получения файлов из сети

#### Typescript
Простой пример получения файла из сети
```typescript
/* import the ipfs-http-client library */
import { create } from 'ipfs-http-client'

/* Create an instance of the client */
const client = create({
  url: 'https://ipfs.infura.io:5001/api/v0'
});

function App() {
  async function onChange(e) {
    /* Identifer file (ipfsPath) */
    const path = 'QmQEbM3FmeoLNuv4snyadi3noV7s6oy4JEEpVJvAWXfMu7'
    
    try {
      /* return AsyncIterable<Uint8Array> */
      const file = await client.get(path)

      for await (const item of file) {
        /* Buffer bytes */
        console.log(item)
      }
    } catch (error) {
      console.log('Error downloading file: ', error)
    } 
}
```

