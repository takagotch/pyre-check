### pyre-check
---
https://github.com/facebook/pyre-check

```py
def foo() -> int:
  return unannotated_library_function()
  
def unannotated_library_function() -> int:
  return sometimes_returns_a_string(return_string=False)
  
def unannotated_library_function() -> int:
  return sometimes_returns_a_string(return_string=False)


def foo() -> int:
  return "string"
def foo() -> int:
  return "string"
def foo() -> int:
  return a.undefined
  









```

```
```

```
```


