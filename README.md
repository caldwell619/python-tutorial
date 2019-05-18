# Python Quick Start Guide

This guide is meant for people who know programming concepts, and need or want to learn Python without all the intro filler a lot of tutorials have. 

The focus is mostly on implementation and syntax.

## Running Scripts

To execute a Python script, run `python FILE_NAME`, after having Python installed.

The cleanest way I've found to install it ( clean meaning minimal effort ), is to `brew install python`. 

I installed it with `brew install awscli`, but I needed the AWS CLI anyway, so it worked out.

## Editor

It's an interpreted language, so you don't need an IDE. VSCode has some cool extensions for linting, and that's my default editor anyhow.

 You can right click and run the scripts from VSCode, if that's your thing.

## Conditionals

Support truthy and falsey values. 

### Falsey

- Empty String
- 0
- 0.0

### If

Python does not have curly braces, `{}`, it instead uses white space and indentation to determine execution

Format:

```
if condition operator second_condition
  # execute for true
# Code executed after completion
```

Example: 

```
if 1 == 1:
  print('duh')
print('out of condition')
```

Python does not compare data types, so `==` is for comparison

### Else

Use a `:` to the end of the else

```
if 1 == 1:
  print('duh')
else:
  print('inside false condition)
print('out of condition')
```


### Elif

This is the `else if`. 

```
elif a < 3:
  print('do sumn')
```







## Iterating

### While

#### Syntax

```
while CONDITION:
  # do stuff that eventually turns condition false
```

### For

#### Syntax

```
for i in iterable
  print('I did stuff ' + str(i) + ' times')
```

Or the non insane way, using [string interpolation](https://www.python.org/dev/peps/pep-0498/)

```
for i in iterable
  printf('I did it ${i} times')
```



#### Terms

##### Range Data Type

`range(start, end, step)`

`end` is treated like an index position, but not start. So `range(1,5)` will go from `1-4` 


## Functions

### Terms

#### Module
  - Built in library of functionaly that needs to be imported to be used
  `import random` <-- almost too easy, right?
 
Modules are accessed with dot notation, so to call a function on `random`, you'd write `random.randint(args)`

You can pull specific functions out of certain modules.

If you're familiar with JS, it's essentially destructuring.

```
from random import WHATEVER_YOU_WANT
```

You can also import several things, comma separated.

```
import one, two, three, four
```


