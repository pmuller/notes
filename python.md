# Python

## Static call graph

```bash
pyan3 $(readlink -f path/to/parent/dir)/*.py --svg
```

Notes:

1. Used pyan3 1.2.0
2. Need to apply [this patch](https://github.com/Technologicat/pyan/pull/65/files)
3. Need to pass it absolute paths as of 2023-01-24 to avoid
   [issue 70](https://github.com/Technologicat/pyan/issues/70)
