
Regular recursion can fail if stack frames are finite. You can trigger a buffer overflow.

```java 
public int factorial (int x)
{
  if (x == 1)
  {
    return 1;  //base case
  }

  else  /*recursive case*/
   return factorial(x-1) * x;
}
```

```
factorial (4) ;
return factorial(3) * 4;
return factorial(2) * 3;
return factorial(1) * 2;
return 1;
```

**each function call has to be made in order to evaluate the result** 

if we opt in for tail recursion, we can carry the result of our evaluation by overriding an argument


```python
def factorial(i, current_factorial=1):
  if i == 1:
    return current_factorial
  else:
    return factorial(i - 1, current_factorial * i)
```

```
factorial(4, 1)
return factorial (3,  1 * 4 ) //i == 4
return factorial (2,  4 *3 ) //i == 3
return factorial (1,  12 *2 ) //i == 2
return 24  //i == 1
```
