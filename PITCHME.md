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

## Q & A