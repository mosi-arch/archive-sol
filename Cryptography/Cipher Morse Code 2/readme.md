# Cipher Morse Code | example usecase
- in this example run `Test` contract.
- send a Letter & an Address by using `sendMsg` function.
- receive and decode message by using the recipient address in`receiveMsg` function.

Enjoy it!

### contract info

|  Contract  |         Type        |       Bases      |                  |                 |
|:----------:|:-------------------:|:----------------:|:----------------:|:---------------:|
|     â      |  **Function Name**  |  **Visibility**  |  **Mutability**  |  **Modifiers**  |
||||||
| **Cipher** | Implementation |  |||
| â | compare | Internal ð |   | |
| â | morse_to_char | Internal ð |   | |
| â | char_to_morse | Internal ð |   | |
| â | hash | Internal ð |   | |
| â | dehash | Internal ð |   | |
||||||
| **Test** | Implementation | Cipher |||
| â | receiveMsg | Public âï¸ |   |NOâï¸ |
| â | sendMsg | Public âï¸ |   |NOâï¸ |
||||||
| **TestWord** | Implementation | Cipher |||
| â | concat | Internal ð |   | |
| â | morse | Public âï¸ |   |NOâï¸ |
||||||
| **Cipher** | Implementation |  |||
| â | compare | Internal ð |   | |
| â | char_to_morse_code | Internal ð |   | |
||||||
| **Test** | Implementation | Cipher |||
| â | morse | Public âï¸ |   |NOâï¸ |
||||||
| **Cipher** | Implementation |  |||
| â | <Constructor> | Public âï¸ | ð  |NOâï¸ |
| â | _design1 | Internal ð | ð  | |
| â | _design2 | Internal ð | ð  | |
| â | _T | Internal ð |   | |
| â | concat | Internal ð |   | |
| â | _generate | Internal ð |   | |
| â | _pattern_1 | Internal ð | ð  | |
| â | _pattern_2 | Internal ð | ð  | |
||||||
| **TestWord** | Implementation | Cipher |||
| â | unMerge | Public âï¸ |   |NOâï¸ |
| â | generate | Public âï¸ |   |NOâï¸ |
| â | table | Public âï¸ |   |NOâï¸ |
| â | pattern_1 | Public âï¸ | ð  |NOâï¸ |
| â | pattern_2 | Public âï¸ | ð  |NOâï¸ |
||||||
| **Cipher** | Implementation |  |||
| â | <Constructor> | Public âï¸ | ð  |NOâï¸ |
| â | _design | Private ð | ð  | |
| â | _T | Internal ð |   | |
| â | concat | Internal ð |   | |
| â | _generate | Internal ð |   | |
||||||
| **TestWord** | Implementation | Cipher |||
| â | generate | Public âï¸ |   |NOâï¸ |
| â | table | Public âï¸ |   |NOâï¸ |
||||||
| **Cipher** | Implementation |  |||
| â | compare | Internal ð |   | |
| â | _T | Internal ð |   | |
| â | T | Public âï¸ |   |NOâï¸ |
| â | isValid | Public âï¸ |   |NOâï¸ |


 Legend

|  Symbol  |  Meaning  |
|:--------:|-----------|
|    ð    | Function can modify state |
|    ðµ    | Function is payable |

### signature hash

| Sighash   |   Function Signature | 
| ---- | ---- |
| 3a96fdd7  |  compare(string,string) | 
| 73cb57f8  |  morse_to_char(string) | 
| 7d6fb494  |  char_to_morse(string) | 
| 436d4ff5  |  hash(string,address) | 
| 03b34a23  |  dehash(bytes) | 
| b746078a  |  receiveMsg(bytes) | 
| 4996c0ef  |  sendMsg(string,address) | 
