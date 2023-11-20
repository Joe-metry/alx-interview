# Project Overview:


This Python script addresses an interview question about finding the fewest number of coins needed to meet a given total amount. Here's an overview of the code:

1. **Shebang Line:**
   ```python
   #!/usr/bin/python3
   ```
   This line specifies the path to the Python interpreter that should be used to execute the script.

2. **Docstring:**
   ```python
   """
   Interview Question on: fewest number of coins needed to
   meet a given amount total
   """
   ```
   A docstring is a string literal that occurs as the first statement in a module, function, class, or method definition. In this case, it provides a brief description of the purpose of the script, mentioning that it's related to finding the fewest number of coins needed for a given total amount.

3. **Function Definition:**
   ```python
   def makeChange(coins, total):
       """ fewest number of coins needed to meet total """
   ```
   This defines a function named `makeChange` that takes two parameters: `coins` (a list of coin denominations) and `total` (the target total amount). The docstring for the function provides a brief description of its purpose.

4. **Function Implementation:**
   ```python
   if total <= 0:
       return 0
   ```
   If the target total is less than or equal to zero, the function returns 0, indicating that no coins are needed.

   ```python
   coins.sort(reverse=True)
   ```
   The list of coin denominations (`coins`) is sorted in descending order.

   ```python
   change = 0
   for coin in coins:
       if total <= 0:
           break
       temp = total // coin
       change += temp
       total -= (temp * coin)
   ```
   The function then iterates through the sorted list of coin denominations. For each coin, it calculates how many of that coin can fit into the remaining total (`temp`). It updates the `change` variable with the number of coins used and reduces the remaining total accordingly.

   ```python
   if total != 0:
       return -1
   ```
   If the remaining total is not zero after using all available coin denominations, the function returns -1 to indicate that it's not possible to make the exact total with the provided coins.

   ```python
   return change
   ```
   Otherwise, if the total is successfully reduced to zero, the function returns the total number of coins used.

Overall, this script provides a solution to the problem of finding the fewest number of coins needed to reach a given total using a specified set of coin denominations.
