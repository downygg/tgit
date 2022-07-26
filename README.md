# Multi-Chain Endpoint
----
## Daftar Chain

- **BSC (Binance SmartChain)**
-       http://chainshub.xyz/api/bsc/mainnet
        http://chainshub.xyz/api/bsc/testnet
- **Matic Polygon**
-       http://chainshub.xyz/api/matic/mainnet
        http://chainshub.xyz/api/matic/testnet
- **Okex Chain**
-       http://chainshub.xyz/api/okt/mainnet
        http://chainshub.xyz/api/okt/testnet
- Fantom Chain
-       http://chainshub.xyz/api/ftm/mainnet
        http://chainshub.xyz/api/ftm/testnet
- Avax Chain
-       http://chainshub.xyz/api/avax/mainnet
        http://chainshub.xyz/api/avax/testnet
- Tomochain
-       http://chainshub.xyz/api/tomo/mainnet
        http://chainshub.xyz/api/tomo/testnet
- Bittorent Chain
-       http://chainshub.xyz/api/bttc/mainnet
        http://chainshub.xyz/api/bttc/testnet
- Solana Chain
-       http://chainshub.xyz/api/solana/mainnet
        http://chainshub.xyz/api/solana/testnet
- Zilliqa Chain
-       http://chainshub.xyz/api/zilliqa/mainnet
        http://chainshub.xyz/api/zilliqa/testnet
- Algorand Chain
-       http://chainshub.xyz/api/algorand/mainnet
        http://chainshub.xyz/api/algorand/testnet

- XRP Chain
-       http://chainshub.xyz/api/xrp/mainnet
        http://chainshub.xyz/api/xrp/testnet
        
- Ethereum Chain
-       http://chainshub.xyz/api/eth/mainnet
        http://chainshub.xyz/api/eth/testnet //rinkedby testnet

## Daftar Token 
- BUSD (SmartChain)
-       http://chainshub.xyz/api/token/busd/mainnet
        http://chainshub.xyz/api/token/busd/testnet
- USDT (SmartChain)
-       http://chainshub.xyz/api/token/usdt/mainnet
        http://chainshub.xyz/api/token/usdt/testnet
- Bittorent (Smartchain)
-       http://chainshub.xyz/api/token/btt/mainnet
        http://chainshub.xyz/api/token/btt/testnet

## Daftar Method
- Generate Address
- Check Balance
- Transfer Coin/Token
---
## Parameter Request
- **_Generate Address_ (GET METHOD)**
    > - All Chain (**{endpoint}/address/generate**)

- **_Check Balance_ (POST METHOD)**
    > - All Chain (**{endpoint}/balance**)
    ```sh
            {
                address: "${address}"
            }
    ```
- **_Transfer Token_ (POST METHOD)**
    > - BSC, MATIC, OKEX, FANTOM, AVAX, TOMO, BITTORENT (**{endpoint}/transfer**)
    ```sh
        {
            "to_address": "0x...",
            "address" : "0x...", //sender address
            "privatekey" : {$privatekey},
            "amount" : 0.001,
            "gas"   : 21000,
            "price" : 5
        }
    ```
    
    > - Solana (**_${endpoint}/transfer_**)
    ```sh
        {
            "from"      : "${from_address}",
            "to"        : "${to_address}",
            "amount"    : 1,
            "secret"    : "${secret key}
        }
    ```
    
    > - Zilliqa (**_${endpoint}/transfer_**)
    ```sh
        {
            "toAddr"        : "${to_address}",
            "amount"        : 1,
            "privatekey"    : "${privatekey}
        }
    ```
    
    > - Algorand (**_${endpoint}/transfer_**)
    ```sh
        {
            "from"      : "${from_address}",
            "to"        : "${to_address}",
            "amount"    : 1,
            "secret"    : "${secret key}
        }
    ```
    
    > - XRP (**_${endpoint}/transfer_**)
    ```sh
        {
            "address"   : "${from_address}",
            "to_address": "${to_address}",
            "amount"    : 1,
            "tag"       : "${secret key}",
            "seed"      : ${account_seed}
        }
    ```
