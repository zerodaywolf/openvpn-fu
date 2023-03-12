# OpenVPN-fu 

1. Read credentials from file:

```
auth-user-pass /home/$USER/Downloads/vpn-login.conf
```

- Sample `vpn-login.conf`

```
foo@bar.com
FooBarRocksX100
```

2. Disable reauthorization/renegotation:

```
reneg-sec 0
```

3. Don't cache username/passwords in virtual memory:

```
auth-nocache
```

- Causes openvpn to forget credentials immediately after they are used
- Will prompt for username/passwords multiple times during an OpenVPN session.

4. Do not close the connection if it is inactive:

```
inactive 0
```
