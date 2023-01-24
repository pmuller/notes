# pulumi

## Use a socks proxy

```bash
ssh -ND42424 bastion&
NO_PROXY=127.0.0.1,localhost,10.0.0.0/8,.pulumi.com,api.github.com \
HTTPS_PROXY=socks5://localhost:42424 \
pulumi ...
```
