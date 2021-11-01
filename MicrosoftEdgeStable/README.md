# Microsoft Edge Stable no Linux baseado em Debian
##### Válido apenas para Debian, Ubuntu, Linux Mint, ElementaryOS, ZorinOS, Arch Linux, entre ouros.

Como instalar:
> Antes de tudo: Abra o terminal com o **CTRL** + **Shift** + **T**

> Certifique de que tenha o Curl instalado!

>Para isso, digite:
```Terminal
$ curl --version
```
> Se der uma mensagem semelhante a essa abaixo, está tudo ok e então podemos continuar:
```Terminal
curl 7.68.0 (x86_64-pc-linux-gnu) libcurl/7.68.0 OpenSSL/1.1.1f zlib/1.2.11 brotli/1.0.7 libidn2/2.2.0 libpsl/0.21.0 (+libidn2/2.2.0) libssh/0.9.3/openssl/zlib nghttp2/1.40.0 librtmp/2.3
Release-Date: 2020-01-08
Protocols: dict file ftp ftps gopher http https imap imaps ldap ldaps pop3 pop3s rtmp rtsp scp sftp smb smbs smtp smtps telnet tftp 
Features: AsynchDNS brotli GSS-API HTTP2 HTTPS-proxy IDN IPv6 Kerberos Largefile libz NTLM NTLM_WB PSL SPNEGO SSL TLS-SRP UnixSockets
```
> Continuando: Execute este primeiro comando:
```Terminal
$ curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
```

> depois para este comando:
```Terminal
$ sudo install -o root -g root -m 644 microsoft.gpg /etc/apt/trusted.gpg.d/
```

> depois para este comando:
```Terminal
$ sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/edge stable main" > /etc/apt/sources.list.d/microsoft-edge-beta.list'
```

> depois para este comando:
```Terminal
$ sudo rm microsoft.gpg
```

> Depois para este comando:
```Terminal
$ sudo apt update
```

> E, por fim, execute este comando:
```Terminal
$ sudo apt install microsoft-edge-stable
```

##### Pronto!