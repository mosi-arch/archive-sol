# Defi Safe Percentage
in defi protocoles we need al mathmatical functions work as well and trust...

### example:
- function `setPercentageFee` a number between 1 to 9999 --> 7500 = 75%
- function `test` show the current input number percentage fee

```
0:uint256: percentageFee 1500
1:uint256: total 500
```
---

### review code
```solidity
percentageFee = (amount.mul(percentage)).div(10000);
total = amount.sub(percentageFee);
```

- 1- `(amount * percentage) / 10000`
- 2- `amount - percentageFe`

> choose good word, make good world!
