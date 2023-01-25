# Python

## TypeGuards

TypeGuards are Python functions that helps determine the actual type of a Python
object.

```python
from typing import Literal, TypeGuard, Any

MagicString = Literal['foo', 'bar']

def is_magic_string(object: Any) -> TypeGuard[MagicString]:
    return object in ('foo', 'bar')

def consume_magic_string(value: MagicString):
    pass

foo: str = 'foo'

if is_magic_string(foo):
    # Here the type checker trusts `foo` to be a valid MagicString
    consume_magic_string(foo)

# This will trigger a typing error, as `foo` is a string:
consume_magic_string(foo)
```

Reference:
[PEP 647 – User-Defined Type Guards](https://peps.python.org/pep-0647/)

Note: similar to
[TypeScript's type predicates](https://www.typescriptlang.org/docs/handbook/2/narrowing.html#using-type-predicates)

## Static call graph

```bash
pyan3 $(readlink -f path/to/parent/dir)/*.py --svg
```

Notes:

1. Used pyan3 1.2.0
2. Need to apply [this patch](https://github.com/Technologicat/pyan/pull/65/files)
3. Need to pass it absolute paths as of 2023-01-24 to avoid
   [issue 70](https://github.com/Technologicat/pyan/issues/70)
