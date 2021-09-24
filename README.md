# HowManyCoins_Python
Python code that calculates the smallest number of coins needed to make the amount of money. Type the amount of money in pennies and it will tell you the number of coins you need for each type.

```python
#Check if only numbers were typed 
while True:
    try:
        amount = int(input("Type the amount of money in pennies.\n"))
        break
    except:
        pass
    print("Type only numbers.\n")

coins = (200, 100, 50, 20, 10, 5, 2, 1)
coinInWord = ("£2", "£1", "50p", "20p", "10p", "5p", "2p", "1p")

for x in range(8):
    numberOfCoins = int(amount / coins[x])
    #Don't show the coin if you don't need it
    if numberOfCoins > 0:
        print("{} {} coin(s)".format(numberOfCoins, coinInWord[x]))
        amount = amount % coins[x]
```
