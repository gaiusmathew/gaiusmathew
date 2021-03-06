<!-- Zero width character is used to put extra blank lines before and after code -->

<h3>
    
```python
​
from dataclasses import dataclass
from typing import Tuple
from developer import full-stack-developer


class FullStack(type):
    def __new__(cls, name, bases, attrs):
        for attr in attrs:
            if not attr.startswith("_"):
                __annotations__[attr] = Tuple[str, ...]
        attrs["__annotations__"] = __annotations__
        new_cls = super().__new__(cls, name, bases, attrs)
        new_cls = dataclass(new_cls)
        return new_cls


class Stack(metaclass=FullStack):
    languages   = ("NodeJs", "Python", "Php")
    frontend    = ("Angular", "Vue", "React")
    frameworks  = ("Express", "Loopback", "NestJs")
    databases   = ("PostgreSQL", "Mongo", "Redis")
    misc        = ("Docker", "AWS")
    ongoing     = ("PostgreSQL", "GraphQL", "Vendure")
    
​
```
</h3>
