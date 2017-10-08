##2a
```
x = 1
function(x) {x} (5)
print x
```

**static:** prints 1

**dynamic:** prints 5

When this code executes, binds the value 1 to x in the environment, then it calls the function which just returns x. when static the value for x is set to one in the environment using big step semantics we know that it will return the value initially bound to x. When we are using dynamic scoping, we know that it will substitute the value 5 in when calling the function using small-step semantics.

##2d
The evaluation order is deterministic if the operation is small-step because every operation is broken down into individual steps.


##3
For e1 + e2 the evaluation order is left to right. To change this we would need to change the search rule so that it evaluates e1 instead of e2.

##4a
```
x || y
```
This is evaluated as "if X then true else y" which is nice because we don't actually have to look at y unless x is not true. This prevents unnecessary function calls when evaluating statements, saving time. 

##4b

Yes, e1 && e2 has a short-circuit because there are rules to handle cases when only one value is evaluated, such as DoAndFalse.