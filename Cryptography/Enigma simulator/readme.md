# Enigma simulator

just enjoy it!

```js
input: ["-","h","i","-"] 
output-> zfqz
input: ["h","e","l","l","o"] 
output-> f-wwb
```

```js
input: ["-","h","i","-"] 
output-> hkbh
input: ["h","e","l","l","o"] 
output-> kjccd
```

### contract info


|  Contract  |         Type        |       Bases      |                  |                 |
|:----------:|:-------------------:|:----------------:|:----------------:|:---------------:|
|     â      |  **Function Name**  |  **Visibility**  |  **Mutability**  |  **Modifiers**  |
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
|  ---- |  ---- | 
| 5871c697  |  _design1() | 
| 061696a4  |  _design2() | 
| f8ef05b5  |  _T(string) | 
| 89c19ddb  |  concat(string,string) | 
| b7d84f1b  |  _generate(string[]) | 
| 0201b8fa  |  _pattern_1() | 
| 56acf605  |  _pattern_2() | 
| da17d8d8  |  unMerge(string) | 
| 1940649d  |  generate(string[]) | 
| 04ff4c43  |  table(string) | 
| de95da5c  |  pattern_1() | 
| 19e6753a  |  pattern_2() | 

