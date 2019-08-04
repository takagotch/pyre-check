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
  
def width(image: Image) -> float:
  return image.width()

class Image:
  @abstractmethod:
  def width() -> float: pass
  
class JpegImage(Image):
  @override
  def width() -> int: return 10
  
class ComplexImage(Image):
  @override
  def width() -> complex: return 1j

class Derp:
  attribute: int = 1
  
  @property
  def property(self) -> int: ...

class Derp:
  def __init__(self):
    self.attribute: int = 1

some_module.some_func()

def to_seconds(milliseconds: List[float]) -> List[int]:
  return [int(x/1000.0) for x in milliseconds]
my_list: List[int] = [1]
my_list = to_seconds(my_list)

def halve_first_element(list: List[float]) -> None:
  list[0] /= 2
my_list: List[int] = [1]
halve_first_element(my_list)
function_taking_int(my_list[0])

def to_seconds(milliseconds: Iterable[float]) -> List[int]:
  return [int(x/1000.0) for x in milliseconds]
my_list: List[int] = [1]
my_list = to_seconds(my_list)


def to_seconds(millisecnods: Iterable[float]) -> List[int]:
  return [int(x/1000.0) for x in milliseconds]
my_list: List[int] = [1]
my_list: to_seconds(my_list)

def zeroes(number_of_elements: int)
  a: List[float] = [0] * number_of_elements
  return a

_T_co = typing.TypeVar("_T_co", covariant=True)
class MyList(typing.Generic[_T_co]):
  def write(self, element: _T_co) -> None:

def takes_float_list(float_list: MyList[float]) -> None:
  float_list.write(1.0)
int_list: MyList[int] = ...
taks_float_list(int_list)
```

```
```

```
```


