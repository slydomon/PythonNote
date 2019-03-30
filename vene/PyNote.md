# Python Note

## Indentation
```1. The same code block should have same indentation such as one space or one tab```

```2. Using colon(:) for For/While/if code block ```

## Variable and Scope
```1. Assignment operator should be seen as "set this symbol to xxx" rather than "this symbol is equal to xxx"```

```2. Base on 1., there is no need to declare a variable name since such name is not bounded with any specification such as type.```

```3.Python does not have different variable scope for/while/if/etc... code block and therefore, the variable used outside those blocks will be effect by variable inside the block if they have the same name. ```

ex:

i = 10

print(i) //print 10

if i == 10:

    i = "happy"
    print(i) ; //will print happy

print(i) //will also print happy

```4. Python resolves the symbol with innermost order, thus variable is bounded with state first in the same scope and then the next outer layer.```

ex:

def function_a():

    i = 7 ;
    print (i) ; //print 7
    

def function_b():

    print(i) ; //print 10
    function_a() ;
    print(i) ; //print 10 since it is sensitive to function block and therefore "i" won't be affected.

i = 10

function_b()


## Type and Data Structure 

### Operator
```1. "//" is divided and truncate to integer whereas "/" does not truncate.```
```2. In Python, * is a valid operator to string.```
```3. "and", "or", "not" is for bool value whereas "==", "!=", etc... is for normal values.```
```4. Provide Bitwise operator, shift is arithmetic right shift.```

### Data Structure
```1. In Python, -1 can represent the last element, -2 is the second last, and so on.```
```2. Slice:[x:y] represents range from x(inclusive) to y(exclusive).```
```2.1 Slice takes three arguments [begin:end:step] => begin to step*end(exclusive), and default value of end is begin+1```
```2.2 [:] = entire list, [:5]([0:5]) the first five elements, [5:] from 5th to end, [:-1] without the last, [:-2] without the last two elements.  ```
```3.List is a mutable array of (different types)elements whereas tuple is an immutable one.```
```3.1 Both of them are arbitrarily nestable: [1, [1,2,3], [a,[b]]]```

