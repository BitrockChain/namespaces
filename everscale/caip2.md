---
namespace-identifier: everscale-caip2
title: EVERSCALE namespace
author: Lev Antropov(@levantropov), Vitaly Gritsay(@vvismaster)
discussions-to: https://github.com/ChainAgnostic/namespaces/pull/52/
status: Draft
type: Standard
created: 23.01.23
requires (*optional):
replaces (*optional):
---

# CAIP-2

*For context, see the [CAIP-2](https://github.com/ChainAgnostic/CAIPs/blob/master/CAIPs/caip-X.md) specification.*

## Rationale
`Mainnet` - main network of Everscale.

`Devnet` - Evercloud Developer Network runs
the latest stable version of Everscale Blockchain.
The goal of Evercloud Devnet is to provide
stable development environment for application developers.

`Testnet(FLD)` - early network feature testing.

However, the names of these networks
are not used inside queries, they are only names.
To work in a certain network, you only need
to apply for the appropriate route(network endpoint).

## Semantics and Syntax
Based on the above, the syntax for constructing
a namespace is a conditional arrangement,
necessary rather for third-party projects
(for example, WalletConnect, etc).
```
everscale:mainnet
everscale:devnet
```

### Resolution Mechanics
A transaction is the result of a contract execution.

In general, a transaction is generated with one incoming message (external or internal) and can generate several outcoming messages (external or internal) as a result.

The transaction can be successful or aborted.

For example, a simple value transfer consists of 2 transactions
— Sender's transaction which generated
an internal message with a value transfer,
and Recipient's transaction where it received
the message with value and updated its balance.

## Test Cases
```
Get information about balance by wallet address in MAINNET.
curl 'https://dapp01.itgold.io/graphql'
-H 'Accept-Encoding: gzip, deflate, br'
-H 'Content-Type: application/json'
-H 'Accept: application/json'
-H 'Connection: keep-alive'
-H 'DNT: 1'
-H 'Origin: https://dapp01.itgold.io'
--data-binary
    '{"query":"query
        {\n blockchain
            {\n account(address: \"0:b38d96bceaa156c07f22b5596c2374b87e26cc53b1b6d7df43401d671bdea708\")
                {\n info{\n balance\n }\n }
            \n}
        \n}"
    }'
--compressed
```
## References
* [Evercloud](https://docs.evercloud.dev/products/evercloud/get-started) -
starting communication with blockchain Everscale.
* [Tools](https://docs.everscale.network/develop/tools/overview) -
tools that help to work with Everscale blockchain.
* [SDK](https://docs.everos.dev/ever-sdk/) - Core Client Library built on the EVER OS GraphQL API for Everscale DApp development.
## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
