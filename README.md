# Vending Machine

**Goal**: Implement a vending machine that minimizes the amount of coins returned.

## Functional requirements
It is assumed that the vending machine has and only accepts coins and not bills.

  - At the beginning, the vending machine randomly generates a sufficiently big number of each coin. 
  - Change will be dispensed using the fewest coins available in the machine.
  - Products can be added to the machine by specifying:
    - Product Name
    - Price (Note: The price must start at ₿100 and should be in increments of ₿10. (E.g.,₿110, ₿120, etc.)
    - Quantity
  - Users can buy products based on the amount they deposit.
  - If the remaining balance is below the cheapest product's price or all products are sold out, the change will be dispensed immediately.
  - The machine should be able to tell the user if an item is sold out and no longer available.
  - If it's impossible to return the full change due to a lack of the appropriate coins, only the amount that can be made up with the available coins will be returned.
  - Any money that can't be returned will be retained by the vending machine.
  - If a user provides an incorrect input value, the machine will generate an error message prefixed with "[ERROR]".
  - After generating the error message, the system will prompt the user to re-enter the input.
  - All interactions (inputs and outputs) with the machine should follow the format given in the example programming execution result provided.

## I/O requirements

**Input**:
Product name, price, and quantity should be separated by commas. Each individual product should be enclosed in square brackets and separated by semicolons.
Example: ```[Cola,₿1500,20];[Soda,₿1000,10]```

**Output**:
Coins held by the vending machine:
```
₿500 - 0
₿100 - 4
₿50 - 1
₿10 - 0
```

Only the coins returned as change will be printed:
```
₿100 - 4
₿50 - 1
```
In case of an exception, an error message must be displayed. However, the error message must start with [ERROR].
[ERROR] The amount must be a number.

**Example of programming execution results**:

_Please enter the amount the vending machine holds:_ $450

_Coins held by the vending machine:_
```
₿500 - 0
₿100 - 4
₿50 - 1
₿10 - 0
```

_Please enter the product name, price, and quantity._ ``[Cola,₿1500,20];[Soda,₿1000,10]``

_Please enter the deposit amount._ ``₿3000``

_Deposited amount:_ ``₿3000``

_Please enter the name of the product you want to purchase:_ ``Cola``

_Deposited amount:_ ``₿1500``

_Please enter the name of the product you want to purchase:_`` Soda``

_Deposited amount:_ ``₿500``

_Change:_
```
₿100 - 4
₿50 - 1
```