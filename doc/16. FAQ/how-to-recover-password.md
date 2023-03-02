# How to recover password

##### [Order now](https://puqcloud.com/index.php?rp=/store/puqvpn) | [Download](https://download.puqcloud.com/cp/puqvpncp/)| [FAQ](https://faq.puqcloud.com/)

**Problem:** Username or password were lost

**Solution:**

In order to restore the default account, you must

- delete directory with accounts(**All system access accounts will be deleted**)

```shell
rm -R /usr/local/puqvpncp/users
```

- Restart the **puqvpncp** service

```shell
service puqvpncp restart
```

after these steps, the system creates a default user  
**Username:** admin  
**Password:** admin
