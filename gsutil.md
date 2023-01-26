# gsutil

## Locate the configuration file

```bash
gsutil version -l | grep '^config path' | cut -d: -f2
```

## Use a proxy

1. Locate and edit its configuration file

   ```bash
   vim $(gsutil version -l | grep '^config path' | cut -d: -f2)
   ```

2. Add a `[Boto]` section with the proxy settings

   ```ini
   [Boto]
   proxy = $HOST
   proxy_port = $PORT
   proxy_type = socks5
   ```
