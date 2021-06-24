# Full Scale Service with TLS Certificate

## 1. Install OpenSSL on window

Help Link: https://tecadmin.net/install-openssl-on-windows

##

Create Certificate :

```bash
openssl req -x509 -newkey rsa:4096 -sha256 -keyout tls.key -out tls.crt -days 365
```

Access Locally Add ip with host name in

1. linux/ubuntu/mac : /etc/hosts
2. window: C:\Windows\System32\drivers\etc
