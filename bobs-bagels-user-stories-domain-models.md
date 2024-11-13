# Bob's Bagels User Stories and Domain Models

![Bob's Bagels](./images/bagels.jpg)

## Requirement 1: A customer can add an item to a basket

### User Story 1

```text
As a customer  
I want to be able to add an item to a basket  
So that I can keep track of what I am buying
```

### Domain Model 1

| Objects | Properties                 | Messages          | Outputs |
| ------- | -------------------------- | ----------------- | ------- |
| Basket  | basketItems @Array[@Items] | addItem(@Item)    | @Void   |
| Item    | id @String                 |                   |         |

### Test Cases 1 (just this one to get you started!)

- [ ]  Add item to basket using addItem and expect array (basketItems) has increased in length by 1
- [ ]  Test that item passed to addItem is actually added to the basket
- [ ]  An item without an id property is not added to the basket
- [ ]  You are able to add to a basket with existing items
- [ ]  Item with null is not added to the basket

---

## Requirement 2: A customer can remove an item from a basket

### User Story 2

```text
As a customer  
I want to be able to remove an item from a basket  
So that I can change my mind about what I am buying
```

### Domain Model 2

| Objects | Properties                 | Messages          | Outputs |
| ------- | -------------------------- | ----------------- | ------- |
| Basket  | basketItems @Array[@Items] | removeItem(@Item) | @Void   |
| Item    |                            |                   |         |

### Test Cases 2

???

---

## Requirement 3: A customer is able to see when the basket is at maximum capacity

### User Story 3

```text
As a customer  
I want to be able to see when the basket is at maximum capacity  
So that I know when I can't add any more items
```

### Domain Model 3

| Objects | Properties                 | Messages                           | Outputs  |
| ------- | -------------------------- | ---------------------------------- | -------- |
| Basket  | basketItems @Array[@Items] | isBasketFull()                     | @Boolean |
|         | basketCapacity @Integer    |                                    |          |

### Test Cases 3

???

---

## Requirement 4: A manager can create baskets with a larger capacity

### User Story 4

```text
As a manager  
I want to be able to create baskets with a larger capacity  
So that I can cater for customers who want to buy more items
```

### Domain Model 4

| Objects | Properties                 | Messages                           | Outputs  |
| ------- | -------------------------- | ---------------------------------- | -------- |
| Basket  | basketCapacity @Integer    |                                    |          |
|         |                            | increaseBasketCapacityTo(@Integer) | @Void    |

### Test Cases 4

???

---

## Requirement 5: A customer is not able to remove an item that is not in a basket

### User Story 5

```text
As a customer  
I want to be unable to remove an item that is not in my basket  
So that I don't accidentally remove something I haven't added
```

### Domain Model 5

| Objects | Properties                 | Messages                           | Outputs  |
| ------- | -------------------------- | ---------------------------------- | -------- |
| Basket  | basketItems @Array[@Items] | itemExists(@Item)                  | @Boolean |
| Item    | id @String                 | getId()                            | @String  |

### Test Cases 5

???

---

## DEFINITION OF DONE

- [ ]  For each User Story above, you need to satisfy the following:
- [ ]  User Stories Decomposed to single function
- [ ]  Domain model created and checked
- [ ]  Tests written for all functionality
- [ ]  All tests pass
- [ ]  Functionality Coded
- [ ]  Code Review Passed
