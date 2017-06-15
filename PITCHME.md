## Solidity
### (Smart Contract)
## Quick Course

---

```
contract Multiplication {

    int _multiplier;

    function Multiplication(int multiplier) {
        _multiplier = multiplier;
    }

    function multiply(int a) returns (int r) {
       r = a * _multiplier;
       return r;
    }
}
```
@[1]
@[9-12]
@[5-7]
@[3]
@[1-13]


---

```
contract Multiplication {

    int _multiplier;
    event Multiplied(int indexed a,
        address indexed sender, int result );

    function Multiplication(int multiplier) {
        _multiplier = multiplier;
    }

    function multiply(int a) returns (int r) {
       r = a * _multiplier;
       Multiplied(a, msg.sender, r);
       return r;
    }
}
```
@[1]
@[4-5]
@[13]
@[1-16]

---?gist=6c2b4f9679c0fc55b7b1ef614a9d81ee

---
## Nick Zsabo
![Nick Zsabo](http://static2.businessinsider.com/image/54634903ecad04f514a12570-840-479/bitcoin-23.png)

---
## Smart Contract

Smart contracts go beyond the vending machine in proposing to embed contracts in all sorts of property that is valuable and controlled by digital means. Smart contracts reference that property in a dynamic, often proactively enforced form, and provide much better observation and verification where proactive measures must fall short.

---
## Vitalik Buterin
![Vitalik Buterin](http://www.coinfox.info/images/buteriiin.jpg)

---
## Ethereum
![Ethereum](imgs/VitalikButerin_Ethereum.jpg)

---
## Ethereum Blockchain
![Ethereum Blockchain](https://raw.githubusercontent.com/ethereumbuilders/GitBook/master/en/vitalik-diagrams/apply_block_diagram.png)

---
## Ethereum Blockchain (cont.)
![State Transition](https://raw.githubusercontent.com/ethereumbuilders/GitBook/master/en/vitalik-diagrams/ethertransition.png)

---
## Bitcoin's Script

Bitcoin uses a scripting system for transactions. Forth-like, Script is simple, stack-based, and processed from left to right. It is purposefully not Turing-complete, with no loops.

references:
* [BitcoinWiki / Script][https://en.bitcoin.it/wiki/Script]
* [Example Script][https://bitcoin.org/en/developer-guide#p2pkh-script-validation]

---

## Q & A


[nick-zsabo]: http://static2.businessinsider.com/image/54634903ecad04f514a12570-840-479/bitcoin-23.png "Nick Zsabo, from: https://alchetron.com/Nick-Szabo-842137-W"
[buterin]: http://www.coinfox.info/images/buteriiin.jpg "Vitalik Buterin, from http://www.coinfox.info/news/video/5460-vitalik-buterin-o-blokchejne-i-nadezhnosti-ethereum-2"
[buterin-eth]: imgs/VitalikButerin_Ethereum.jpg "Buterin founder of Ethereum"

[eth-block]: https://raw.githubusercontent.com/ethereumbuilders/GitBook/master/en/vitalik-diagrams/apply_block_diagram.png "Ethereum Blockchain, source: https://github.com/ethereum/wiki/wiki/White-Paper"
[state-fn]: https://raw.githubusercontent.com/ethereumbuilders/GitBook/master/en/vitalik-diagrams/ethertransition.png "State Transition Function, source: https://github.com/ethereum/wiki/wiki/White-Paper"
