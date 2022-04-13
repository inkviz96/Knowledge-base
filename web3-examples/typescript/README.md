# Примеры для Web3

- [Подключение к ноде](#%D0%BF%D0%BE%D0%B4%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BA-%D0%BD%D0%BE%D0%B4%D0%B5)
- [Получение баланса кошелька](#%D0%BF%D0%BE%D0%BB%D1%83%D1%87%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B1%D0%B0%D0%BB%D0%B0%D0%BD%D1%81%D0%B0-%D0%BA%D0%BE%D1%88%D0%B5%D0%BB%D1%8C%D0%BA%D0%B0)
- [Получение текущего адреса пользователя](#%D0%BF%D0%BE%D0%BB%D1%83%D1%87%D0%B5%D0%BD%D0%B8%D0%B5-%D1%82%D0%B5%D0%BA%D1%83%D1%89%D0%B5%D0%B3%D0%BE-%D0%B0%D0%B4%D1%80%D0%B5%D1%81%D0%B0-%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8F)
- [Отправка транзакции](#%D0%BE%D1%82%D0%BF%D1%80%D0%B0%D0%B2%D0%BA%D0%B0-%D1%82%D1%80%D0%B0%D0%BD%D0%B7%D0%B0%D0%BA%D1%86%D0%B8%D0%B8)
- [Оценка FEE транзакции](#%D0%BE%D1%86%D0%B5%D0%BD%D0%BA%D0%B0-fee-%D1%82%D1%80%D0%B0%D0%BD%D0%B7%D0%B0%D0%BA%D1%86%D0%B8%D0%B8)
- [Получение инстанса контракта](#%D0%BF%D0%BE%D0%BB%D1%83%D1%87%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B8%D0%BD%D1%81%D1%82%D0%B0%D0%BD%D1%81%D0%B0-%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%B0%D0%BA%D1%82%D0%B0)
- [Подписка на событие смены адреса пользователя](#%D0%BF%D0%BE%D0%B4%D0%BF%D0%B8%D1%81%D0%BA%D0%B0-%D0%BD%D0%B0-%D1%81%D0%BE%D0%B1%D1%8B%D1%82%D0%B8%D0%B5-%D1%81%D0%BC%D0%B5%D0%BD%D1%8B-%D0%B0%D0%B4%D1%80%D0%B5%D1%81%D0%B0-%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8F)
- [Выполнение метода контракта](#%D0%B2%D1%8B%D0%BF%D0%BE%D0%BB%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BC%D0%B5%D1%82%D0%BE%D0%B4%D0%B0-%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%B0%D0%BA%D1%82%D0%B0)
- [Выполнение нескольких одновременных запросов к методам контракта](#%D0%B2%D1%8B%D0%BF%D0%BE%D0%BB%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BD%D0%B5%D1%81%D0%BA%D0%BE%D0%BB%D1%8C%D0%BA%D0%B8%D1%85-%D0%BE%D0%B4%D0%BD%D0%BE%D0%B2%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%BD%D1%8B%D1%85-%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81%D0%BE%D0%B2-%D0%BA-%D0%BC%D0%B5%D1%82%D0%BE%D0%B4%D0%B0%D0%BC-%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%B0%D0%BA%D1%82%D0%B0)
- [Смена сети на кастомную](#%D1%81%D0%BC%D0%B5%D0%BD%D0%B0-%D1%81%D0%B5%D1%82%D0%B8-%D0%BD%D0%B0-%D0%BA%D0%B0%D1%81%D1%82%D0%BE%D0%BC%D0%BD%D1%83%D1%8E)
- [Подписка на эвенты контракта](#%D0%BF%D0%BE%D0%B4%D0%BF%D0%B8%D1%81%D0%BA%D0%B0-%D0%BD%D0%B0-%D1%8D%D0%B2%D0%B5%D0%BD%D1%82%D1%8B-%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%B0%D0%BA%D1%82%D0%B0)
- [Добавление токена](#%D0%B4%D0%BE%D0%B1%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D1%82%D0%BE%D0%BA%D0%B5%D0%BD%D0%B0)
- [Использование в react-native](../react-native/web3-connection-guide/README.md)

## TypeScript
Пример простого приложения с метамаск для e2e тестов - [https://metamask.github.io/test-dapp/](https://metamask.github.io/test-dapp/)

## Подключение к ноде

Если в браузере установлен Metamask, то в качестве провайдера выступает `Web3.givenProvider`, в противном случае можно воспользоваться сервисом Infura или нодой, развернутой на сервере.

```typescript
import Web3 from 'web3';

// URL от ноды или infura
const PROVIDER_URL = 'https://...';

export const web3 = new Web3(Web3.givenProvider || PROVIDER_URL);
``` 

## Получение баланса кошелька

```typescript
const getBalance = async (address: string) => {
    return await web3.eth.getBalance(address);
}
```

## Получение текущего адреса пользователя

```typescript
// для начала нам нужно авторизоваться
const authorize = async () => {
  await web3.currentProvider.request({ method: 'eth_requestAccounts' });
}
// потом мы сможем получить адрес пользователя
const getCurrentAddressUser = () => {
    return web3.currentProvider.selectedAddress;
}
```

## Отправка транзакции

Перевод `value` токенов с `memo` в качестве значения.

```typescript

const transfer = async ({ 
  from, 
  to, 
  value, 
  memo, 
  privateKey, 
  gasLimit = 44000 
}) => {
    const nonce = await web3.eth.getTransactionCount(from);
    const gasPrice = await web3.eth.getGasPrice();
    
    const rawTx = {
      from,
      to,
      value: web3.utils.toHex(Web3.utils.toWei(value, 'ether')),
      gasLimit: web3.utils.toHex(gasLimit),
      gasPrice: web3.utils.toHex(gasPrice),
      nonce: web3.utils.toHex(nonce),
      data: memo,
    };
    
    const privateKeyBuffer = EthUtil.toBuffer(privateKey);
    
    const tx = new Transaction(rawTx);
    
    tx.sign(privateKeyBuffer);
    const serializedTx = tx.serialize();
    
    return this.web3.eth.sendSignedTransaction(
      `0x${serializedTx.toString('hex')}`
    );
}
```

## Оценка FEE транзакции

Используется в случаях, если нужно снять с пользователя точную сумму и добавить к ней сверху fee на проведение
этой транзакции.

```typescript
import { web3 } from '.';

const estimateFee = async ({
    from,
    to,
    value,
    memo,
}) => {
    const gasPrice = await web3.eth.getGasPrice();
    const gasLimit = await web3.eth.estimateGas({
      from,
      to,
      value: web3.utils.toHex(web3.utils.toWei(value, 'ether')),
      data: web3.utils.asciiToHex(memo),
    }).call();
    
    return web3.utils.fromWei(
      BigInt(gasPrice.toString())
        .multiply(BigInt(gasLimit.toString()))
        .toString()
    );
}
```

## Получение инстанса контракта
Удобно реализовать функцию для переиспользования в приложении. Пример:

```typescript
import { Contract } from 'web3-eth-contract';
import { web3 } from '.';

const getContract = (abi: object, address?: string): Contract => {
  const abiFromJson = JSON.parse(JSON.stringify(abi));
  return new web3.eth.Contract(abiFromJson, address);
};

export default getContract;
```

## Подписка на событие смены адреса пользователя

```typescript
import { web3 } from '.';

web3.currentProvider.on('accountsChanged', callback);
```


## Выполнение метода контракта

Предисловие: у контрактов есть 2 типа методов: **read** и **write**. Что бы посмотреть какие методы есть у контракта, нужно перейти на страницу контракта в [https://etherscan.io/ ETH](https://etherscan.io/token/0xdac17f958d2ee523a2206206994597c13d831ec7#readContract) или на другой сервис.

Отличие у них в том, что **read** - методы не требуют газа (комиссия за вызов метода), а **write** методы требуют, поэтому и **write** методы требуют подтверждения со стороны пользователя. Так же есть различия в вызове методов.

Для того чтобы вызвать **write** метод, должен быть подключен плагин с кошельком пользователя (к примеру **Metamask**) и пользователь должен быть авторизован в кошельке, либо открыть приложение через приложение кошелька на телефоне, либо иным способом.

Для того чтобы вызвать **read** метод, нужен либо установленный плагин кошелька в браузере, либо нода, либо подключить **Infura**.

<details>
    <summary>Пример для Metamask (без приватного ключа)</summary>

```typescript
// Смотри пример выше
import { getContract } from '.';

// ABI контракта
const CONTRACT_ABI = { /* ... */ };
 // Адрес контракта
const CONTRACT_ADDRESS = '0xdea164f67df4dbfe675d5271c9d404e0260f33bb';

export const executeContractMethod = async ({}) => {
  // Для того что бы вызвать метод контракта, нам сначала нужно получить сам контракт
  const contract = getContract(CONTRACT_ABI, CONTRACT_ADDRESS);
  
  // Вызываем write метод
  try {
    // Авторизация
    await web3.currentProvider.request({ method: 'eth_requestAccounts' });
    // Получаем адрес кошелька пользователя
    const addressUser = web3.currentProvider.selectedAddress;
    // Вызываем метод контракта "store" - write метод
    // В "send", нужно обязательно передавать объект с ключем "from", иначе не придет запрос на подтверждение транзакции в кошелек
    await contract.methods.store(0, 'Parameter').send({
      from: addressUser,
    });
  } catch (e) {
    throw new Error(e);
  }
  
  // Вызываем read метод
  try {
    // метод так же может, что то возвращать
    const result = await contract.methods.retrieve().call();
  } catch (e) {
    throw new Error(e);
  }
}
```
</details>

<details>
    <summary>Пример для nodejs / react-native (с приватным ключом)</summary>

```typescript
// Смотри пример выше
import { getContract } from '.';

// ABI контракта
const CONTRACT_ABI = { /* ... */ };
// Адрес контракта
const CONTRACT_ADDRESS = '0xdea164f67df4dbfe675d5271c9d404e0260f33bb';
// Для того что бы вызвать метод контракта, нам сначала нужно получить сам контракт
const contract = getContract(CONTRACT_ABI, CONTRACT_ADDRESS);
// Приватный ключ аккаунта
const privateKey = '...';

// Write-метод требует приватного ключа для подписи
const executeContractMethod = async (val: number) => {
    const transaction = contract.methods.store(val);
    const account = web3.eth.accounts.privateKeyToAccount(privateKey);
    const options = {
      to: CONTRACT_ADDRESS,
      data: transaction.encodeABI(),
      gas: await transaction.estimateGas({ from: account.address }),
      gasPrice: await web3.eth.getGasPrice(),
    };
    const signed = await web3.eth.accounts.signTransaction(
      options,
      privateKey,
    );
    await web3.eth.sendSignedTransaction(signed.rawTransaction!);
};
```
</details>

## Выполнение нескольких одновременных запросов к методам контракта

```typescript
/*
  Функция принимает массив запросов к методам контракта
  Возвращает массив промисов
 
  Пример:
  const requests = [
   contract.method.balanceOf().call,
   contract.method.getStaked().call
  ]

  const result = await makeBatchRequest(request);

  *web3 получаем либо из import { getWeb3NoAccount } from "./web3"; 
  or 
  import Web3 from "web3";
  // URL от ноды или infura
  const PROVIDER_URL = "https://...";
  export const web3 = new Web3(Web3.givenProvider || PROVIDER_URL);
*/

const makeBatchRequest = (calls: any[]) => {
  try {
    const web3 = getWeb3NoAccount();
    const batch = new web3.BatchRequest();

    const promises = calls.map((call) => {
      return new Promise((resolve, reject) => {
        batch.add(
          call.request({}, (err, result) => {
            if (err) {
              reject(err);
            } else {
              resolve(result);
            }
          })
        );
      });
    });

    batch.execute();

    return Promise.all(promises);
  } catch {
    return null;
  }
};

export default makeBatchRequest;
```

## Смена сети на кастомную

Определяем chainId, чтобы понять, где мы:
```typescript
const getChainID = async () => {
    return ethereum.request({ method: 'eth_chainId' })
}
```

Просим кошелёк поменять сеть:
```typescript
try {
  await window.ethereum.request({
    method: 'wallet_switchEthereumChain',
    params: [{ chainId: '0x03' }],
  });
} catch (switchError) {
  // This error code indicates that the chain has not been added to MetaMask.
  if (error.code === 4902) {
    try {
      await window.ethereum.request({
        method: 'wallet_addEthereumChain',
        params: [{ 
          chainId: '0x03', // ropsten chainID (3) в hex
          chainName: 'Ropsten Test Network', 
          nativeCurrency: { 
              name: 'ETH', // название валюты
              symbol: 'ETH', // символ валюты 
              decimals: 18  // название валюты
          }, 
          rpcUrls: ['https://ropsten.infura.io/v3/9aa3d95b3bc440fa88ea12eaa4456161'], 
          blockExplorerUrls: ['https://ropsten.etherscan.io'] 
        }] ,
      });
    } catch (addError) {
      // handle "add" error
    }
  }
  // handle other "switch" errors
}
```

Слушаем событие на изменение сети
```typescript
ethereum.on('chainChanged', handler: (chainId: string) => void);
```

## Подписка на эвенты контракта

Существуют несколько способов получать события контрактов. Для всех способов нужен инстанс web3, и контракт:
```typescript
  import Web3 from 'web3';
  const web3 = new Web3('YOUR_RPC_ENDPOINT_HERE');
  const ABI = 'YOUR ABI HERE';
  const CONTRACT_ADDRESS = 'YOUR CONTRACT ADDRESS HERE';
  const myContract = new Web3.Contract(ABI, CONTRACT_ADDRESS);
```

### Реализация подписки на событие на конкретном примере
Метод подписки на событие **RegisterUser (регистрация пользователя)** в реферальной программе

```typescript
referralProgramContract.events
  .RegisterUser()
  .on('connected', (subscriptionId: string) => {
    console.log(`| UserRegistered | events | ${subscriptionId}`);
  })
  .on(
    'data',
    async (event: {
      removed: boolean;
      returnValues: RegisterUserResponseInterface;
    }) => {
      try {
        if (event.removed) {
          return;
        }
        const { user, referrer } = event.returnValues;
        console.log(user, referrer);
      } catch (e) {
        console.log(`| ONCE | ${e}`);
      }
    },
  )
  .on('error', (error: ErrnoException) => {
    console.log(error);
  });
```

### Автоматически сгенерированные в экземпляре контракта.

Например, слушаем событие "Transfer":
```typescript
  let options = {
    filter: {
        value: [],
    },
    fromBlock: 0
  };

  myContract.events.Transfer(options)
    .on('data', event => console.log(event))
    .on('changed', changed => console.log(changed))
    .on('error', err => throw err)
    .on('connected', str => console.log(str))
```

### Общий метод Subscribe
Универальный метод подписки на события, c фильтром по заданным параметрам.

```typescript
  let options = {
    fromBlock: 0,
    address: ['address-1', 'address-2'],    //Only get events from specific addresses
    topics: []                              //What topics to subscribe to
  };

  let subscription = ('logs', options, (err,event) => {
      if (!err)
      console.log(event)
  });

  subscription.on('data', event => console.log(event))
  subscription.on('changed', changed => console.log(changed))
  subscription.on('error', err => { throw err })
  subscription.on('connected', nr => console.log(nr))
```


### Получение истории событий

Например, слушаем событие "Transfer":
```typescript 
  //example options(optional)
  let options = {
    filter: {
        value: ['1000', '1337']    //Only get events where transfer value was 1000 or 1337
    },
    fromBlock: 0,                  //Number || "earliest" || "pending" || "latest"
    toBlock: 'latest'
  };

  myContract.getPastEvents('Transfer', options)
    .then(results => console.log(results))
    .catch(err => throw err);

```

подробнее про [subscribe](https://web3js.readthedocs.io/en/v1.2.11/web3-eth-subscribe.html#)

## Добавление токена
```typesctipt

window.ethereum
  .request({
    method: 'wallet_watchAsset',
    params: {
      type: 'ERC20',
      options: {
        address: '0xb60e8dd61c5d32be8058bb8eb970870f07233155',
        symbol: 'FOO',
        decimals: 18,
        image: 'https://foo.io/token-image.svg',
      },
    },
  })
  .then((success) => {
    if (success) {
      console.log('FOO successfully added to wallet!')
    } else {
      throw new Error('Something went wrong.')
    }
  })
  .catch(console.error)
  ```
