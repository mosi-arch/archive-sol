# Factoiral 
- 1. normal solution - `function factorNType1`
- 2. iterate solution - `function factorNType2`
- 3. algorithmic solution - `function factorNType3`

### example of Number! 
- 4! = 1x2x3x4 = 24
- 5! = 5x4x3x2 = 120

! is the symbol of factorial, place after the num => 5!

Enjoy it!

---

the best solution for saving memory in the computing time is "tail recursive'
```py
# tail recursive, factorial
def fi(f, e=1):
    if f == 1 or f == 0:
        return e
    return fi(f-1, e * f)

i = fi(5)
print(i)
```
