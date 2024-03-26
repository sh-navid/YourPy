# PyN
An engine to append some simple features to the default python interface

## File
Simple example of PyN

```python
# pyn:compile

print("PyN")
```

## Tasks
- [ ] Create custom syntax highlighting for vscode
- [ ] TextMate ??

## Features

### 1. Module Import
```python
# pyn:compile

from dir.sub1.sub2.name import Name

# or

with name import Name

```

___


### 2. Block
```python
# pyn:compile

for x in [1,2,3]:
  print(x)

# or

for x in [1,2,3]{
  print(x)
}
```

___


### 3. Dict Access
```python
# pyn:compile

words = {
    "w1": "word1",
    "w2": "word2",
    "w3": "word3",
    "w4": "word4",
}

print(words["w1"])

# or

words = @{
    w1: "word1",
    w2: "word2",
    w3: "word3",
    w4: "word4",
}

print(words.w1)
```

___


### 4. Interface
***PyN***
```python
# pyn:compile

interface IFactory:
    show(str)->str
    make(int,int,str)->bool

class Factory with IFactory:
    def show(self, a:str)->str:    
        pass

    def make(self, a:int, b:int, c:str)->bool:    
        pass
```

___


### 5. Function
```python
# pyn:compile

func = lambda a: print(a)

func = lambda a, b: print(a, b)

# or

func = a: print(a)

func = a, b: print(a, b)
```

___


### 6. Ternary

```python
a = "low" if True else "high"

# or 

a = True ? "low" : "high"

a = if True "low" else "high"
```

___


### 7. Multiple Condition
***Python***
```python
if 1:
    a = "One"
elif 2:
    a = "Two"
elif 2:
    a = "Three"
else:
    a = "Other"

```

***PyN***
```python
a = ? 1 : "One", 2 : "Two", 3 : "Three", "Other"
```

___


### 8. Callback
***python***
```python
def event(callback):
    print("Event")
    callback("data")

def callback(data):
    print("Callback:",data)

event(callback)
```

***PyN***
```python
def event(callback):
    print("Event")
    callback("data")

event(data):
    print("Callback:",data)
```

___

### 9. Property
***python***
```python
@property
def [NAME](self):
    return self._[NAME]

@[NAME].setter
def [NAME](self, [NAME]):
    self._[NAME] = [NAME]
```

***PyN***
```python
prop [NAME] = "default value"
```

___

### 10. HTML
***PyN***
```python
def test():
    return "Test"

def view():
    return  <>
                <body>
                    <center>
                        {test()}
                    <center>
                </body>
            <>
```

___

### 11. Increment, Decrement
***PyN***
```python
x = 1
x++
x--
```