# Accounts

##### [Order now](https://panel.puqcloud.com/index.php?rp=/store/puqvpn) | [Download](https://download.puqcloud.com/cp/puqvpncp/)| [FAQ](https://faq.puqcloud.com)

## Accounts LIST

**Request Structure:** `https://<puqvpnvp>/api/v1/account`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Example:**

```shell
curl \
-b "access_hash=eda121857897bcf0e4cdf5a3eaf957f35ccb62d39d5bc0bfbfb6d31644eee3cd7f8365e71ad94a60" \
-X GET https://dev.softkeel.com/api/v1/account
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : [
      {
         "allowed_IPs" : "10.0.110.4",
         "b_download" : "12",
         "b_upload" : "12",
         "mangle" : "322",
         "name" : "ruslan_dom_pc",
         "password" : "FE*37#L2WC",
         "private_key" : "UN75r5fizeA5jaCAzF7/nOTTynu67ngsm4jxfiHaHGI=",
         "public_key" : "sdxzHEBOdgm9ZzRn2tw2bzdnU1v7mUp1plpAU+craSo=",
         "status" : "enable",
         "username" : "user_217",
         "wg_name" : "77_87_125_209"
      },
      {
         "allowed_IPs" : "10.0.110.3",
         "b_download" : "12",
         "b_upload" : "12",
         "mangle" : "286",
         "name" : "ruslan_pc",
         "password" : "78gYA%!!9X",
         "private_key" : "GOLitV1C3WT6Pn2rNS8QtgOLRMiJ385DYoDcfnrRbXY=",
         "public_key" : "VeQE3cIzmo58otUUzpfkEDWqk1jscoO9KRAKNtIW1QY=",
         "status" : "enable",
         "username" : "user_181",
         "wg_name" : "77_87_125_209"
      },
      {
         "allowed_IPs" : "10.0.110.17",
         "b_download" : "12",
         "b_upload" : "12",
         "mangle" : "131",
         "name" : "ruslan_telefon",
         "password" : "jvPdmqqTmRV9",
         "private_key" : "MEZAzrlpzqNJCT8k9JWLkBL2+TPe/LZQp3RAWEqffko=",
         "public_key" : "GA2IQFgC+SVYwoIetUNQPSR1ytiet4xxXXAJ+P+IlUY=",
         "status" : "enable",
         "username" : "user_32",
         "wg_name" : "77_87_125_209"
      } 
   ],
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
```

- - - - - -

## Account DETAIL

**Request Structure:** `https://<puqvpnvp>/api/v1/account/<NAME>`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Example:**

```shell
curl \
-b "access_hash=eda121857897bcf0e4cdf5a3eaf957f35ccb62d39d5bc0bfbfb6d31644eee3cd7f8365e71ad94a60" \
-X GET https://dev.softkeel.com/api/v1/account/peer_10
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "allowed_IPs" : "10.0.105.18",
      "b_download" : "20",
      "b_upload" : "20",
      "mangle" : "109",
      "name" : "peer_10",
      "password" : "dH4%%2M2%B",
      "private_key" : "GNuP0siryMimPSuF7Hnmw0D7gY7FXzoY6IgUmt1uuXc=",
      "public_key" : "7C5u5vZk051iA5W2zfbxjlZDgAdm7HdRFRgarI8nBw4=",
      "status" : "enable",
      "username" : "user_10",
      "wg_name" : "Default_106"
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
-Account not found
```

- - - - - -

## Account ADD

**Request Structure:** `https://<puqvpnvp>/api/v1/account`

**Cookie: `access_hash=<access_hash>`**

**Method: `POST`**

**POST data:**

 **Required:**

```JSON
"wg_name" = "WG_NAME"
"allowed_IPs" = "CIDR format"
```

 **Not required:**

```JSON
"b_download" = "0-10000"
"b_upload" = "0-10000"
"name" = "NAME"
"password" = "PASSWORD"
"private_key" = "private_key"
"public_key" = "public_key"
"status" = "enable|disable"
"username" = "USERNAME"
```

<p class="callout info">**If any parameter is not specified during creation, the system will create, if possible, with a unique parameter.**</p>

**Example:**

```shell
curl \
-b "access_hash=eda121857897bcf0e4cdf5a3eaf957f35ccb62d39d5bc0bfbfb6d31644eee3cd7f8365e71ad94a60" \
-d "wg_name=77_87_125_209&\
allowed_IPs=10.0.110.52&\
b_download=100&\
b_upload=100&\
name=NAME111&\
password=PASSWORD&\
status=disable&\
username=USERNAME111" \
-X POST https://dev.softkeel.com/api/v1/account
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "allowed_IPs" : "10.0.110.52",
      "b_download" : "12",
      "b_upload" : "12",
      "mangle" : "100",
      "name" : "NAME111",
      "password" : "PASSWORD",
      "private_key" : "kC8n0NGFxwqvwIfI8xJg2ZzRtp950ltC4ugPHlPxsm0=",
      "public_key" : "p3i2VHZRHwVk3uk+Yo4oKoeQ6gLF+jF33P+pnKai3iE=",
      "status" : "disable",
      "username" : "USERNAME111",
      "wg_name" : "77_87_125_209"
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
-Account not found
-VPN account limit exceeded
-Wireguard server not valid
-Wrong name (only letters, numbers and '_', '-')
-The name is already in use
-The username is already in use
-Wrong Username (only letters, numbers and '_', '-')
-Wireguard server not valid
-Wrong IP format
-IP address already in use
-The IP address is not within the range of the wireguard server
-Keys are invalid
```

- - - - - -

## Account EDIT

**Request Structure:** `https://<puqvpnvp>/api/v1/account/<NAME>`

**Cookie: `access_hash=<access_hash>`**

**Method: `PUT`**

**PUT data:**

 **Not required:**

```JSON
"b_download" = "0-10000"
"b_upload" = "0-10000"
"password" = "PASSWORD"
"status" = "enable|disable"
```

**Example:**

```shell
curl \
-b "access_hash=eda121857897bcf0e4cdf5a3eaf957f35ccb62d39d5bc0bfbfb6d31644eee3cd7f8365e71ad94a60" \
-d "allowed_IPs=10.0.110.60&\
b_download=11&\
b_upload=11&\
password=PASSWORD111122223333&\
status=enable" \
-X PUT https://dev.softkeel.com/api/v1/account/NAME111
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "allowed_IPs" : "10.0.110.60",
      "b_download" : "11",
      "b_upload" : "11",
      "mangle" : "100",
      "name" : "NAME111",
      "password" : "PASSWORD111122223333",
      "private_key" : "kC8n0NGFxwqvwIfI8xJg2ZzRtp950ltC4ugPHlPxsm0=",
      "public_key" : "p3i2VHZRHwVk3uk+Yo4oKoeQ6gLF+jF33P+pnKai3iE=",
      "status" : "enable",
      "username" : "USERNAME111",
      "wg_name" : "77_87_125_209"
   },
   "status" : "success"
}

```

**Errors:**

```
-Not authorized
-Account not found
-Wireguard server not valid
-Wrong external IP format
-IP address already in use
-The IP address is not within the range of the wireguard server
```

- - - - - -

## Account DELETE

**Request Structure:** `https://<puqvpnvp>/api/v1/account/<NAME>`

**Cookie: `access_hash=<access_hash>`**

**Method: `DELETE`**

**Example:**

```shell
curl \
-b "access_hash=eda121857897bcf0e4cdf5a3eaf957f35ccb62d39d5bc0bfbfb6d31644eee3cd7f8365e71ad94a60" \
-X DELETE https://dev.softkeel.com/api/v1/account/NAME111
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : "success",
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
-Account not found
```

- - - - - -

## Account Config Text

**Request Structure:** `https://<puqvpnvp>/api/v1/account/<NAME>/config_text`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Example:**

```shell
curl \
-b "access_hash=eda121857897bcf0e4cdf5a3eaf957f35ccb62d39d5bc0bfbfb6d31644eee3cd7f8365e71ad94a60" \
-X GET https://dev.softkeel.com/api/v1/account/peer_10/config_text
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : "[Interface]\tAddress = 10.0.105.18/24\n\tDNS = 8.8.8.8,1.1.1.1\n\tPrivateKey = GNuP0siryMimPSuF7Hnmw0D7gY7FXzoY6IgUmt1uuXc=\n\t\n[Peer]\n\tAllowedIPs = 0.0.0.0/0\n\tEndpoint = 77.87.125.200:51926\n\tPublicKey = Hkldth2Pdu/jnJ0NH4cjSlsun2pFdIUZXt0h5qaNzmA=",
   "status" : "success"
}

```

**Errors:**

```
-Not authorized
-Account not found
```

- - - - - -

## Account Config QR

**Request Structure:** `https://<puqvpnvp>/api/v1/account/<NAME>/config_qr`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Output:** data:image/png;base64

**Example:**

```shell
curl \
-b "access_hash=eda121857897bcf0e4cdf5a3eaf957f35ccb62d39d5bc0bfbfb6d31644eee3cd7f8365e71ad94a60" \
-X GET https://dev.softkeel.com/api/v1/account/peer_10/config_qr
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : "iVBORw0KGgoAAAANSUhEUgAAAfQAAAH0AQMAAADxGE3JAAAABlBMVEX///8AAABVwtN+AAAGTUlEQVR42uydP9arMA7F5UNBmSWwFC/NXhpLYQmUFBw0R/fKJuR900wDycjFO3kJPxrbsv5c65MYMWLEiBEjxv80RsVIh3+q/Hqai8igutp/9Bi2ly65lqS7A8H/CL/Zv/aDyGuRovbBeftxUq3J+HWaRYznK4N/Cv9SnYukfVxfS1aVYbcX2ayLyMsXh41c7e3jaq8M/lk8NuYqUuphvNpKSLYSJp3LITKu9ib7Mfgn8oJHMO2gFhGY2VWyYiFgTRTdJfgf42G/RcxE28dk2CLZHoH9nuVI6mczVtJf9j/4u/jmP/GILb7Fl1w17eP2WvJcrj/+F/8r+Ft4H5jhddIKt3edzH5jcy9Zqx6DrnCuzLj/OYK/iTf7O2c9EvzfrO7/Cu0vf+R3k1ZJZn/NOdbgf4WXac5Vkm4W9YgI/a+stv97/GofMna9nb84r4N/Ai+jHbZqj/CITR6/iiaf/6p9wH4vOK+DfwZvgeksicHqLOIvgtXeEP8InCvzkjXtMO5Zg38KP6rOUg7bvzxisUUXKfamzXZt5Y/0mobttWCbB/8rPIKdg7kmpn/5yDFsI8y22QTkfxHcciUF/xDetriardYVyV7/amYmAimJ5OdvLWk3myC5SvDP4EddzX8iL5hiPGLYzoO4eJiLTwOyE+/5h+Dv5JnPg9WlsysMUfGmEc/K0ZJLhSHNkjX4H+E9RZg8RSHFU4SZwarSf95bcXXQ7XXxn4O/l/esg8WvnGLO/6QW9Wzc9sxO6Vzw3WuR9/UT/K38iBILXVyZ5tKn+C25pAfqb3NpmaT3/FHwt/IMYLuLa88OmOKqyeYf/lNTLaBM84//FfxX8y9scfuwdokDnj3aE4fAuJMaP/Mfwd/Kj7pkSBxgyavwsOXDo/vUZtxPQ75c5j/4m3nYb+3OLrymxfV/G0syB6ou6uIkf3nwT+BZf4H9Rf4P569M1B+5c0yrCyUgn/qIX4L/Xt7z/wxRJ63lGFBIh4vF5IaLe11/5MWd4B/CI8QplDgwazjY/PsRS3HhQTe7npkoCf4hPDemF9sQ4tgRO9mbUHWZPX+E+Xdx0rV+GvztvMLrfaky//s6K95mbA8oGaZZCourl/xv8F/Nw1eeBVoHPAJPrOs/oX84miFQXLO4rJ/g7+WbiVbknyDRHehIu/6zJycUySnq7y/5x+Bv5Ec4S5h/odjTSyyYfyyOdqcpa0VyePqs3wV/J98GEnue/1PtJ7Hkmpj/1dq+yyrB/wYvrvoUlzjA2TL/uXJNNf0nywTQn9mBHfxT+M/84TXEafr7jeIkOlfLh340+Ht5llgEV1xw6xDBDjUNlO0yE1Gq7tKdq+CfwDPF58IilLh3+k9FdB+p3+TmpswM5++7/Q7+6/mZxRq/P6peP2+rJjdxUq6FkdDysX6Cv49v+Qfvn1GFV9ROiTXnf+vFOXkt0/X+YfD38j2Q9RQvd7JAv9C7ZrTeKIMvjuCfwZ/37zGQInL9H+4/sLgGcVn7CnqV4H+GR/6QZTekCBn1nLFqTW7Jm7jwY/0EfyfvKfousXb/OZuzxJRUz98XVcavF/1h8HfyHqwy/hHoF3bxrO95bfTM36t+1N+Cv5Xv/YvYf+H9/tLB5FJm/wWBuMHvvxQN/jf4rj/zYnkPcdTzhxkOGM5f1bQPXdwd/CN46I/6xaQqrn9Q9L/h+dvu/6J/kb88+GfwLJHWs0SqniKq/fzt9Rdcn4AStAb/GB7xyJGoXyi9fw308+f9JVzkZnLwqj8J/qv5VqJpKYpC/2uipBD2G8091e/vD4yJgn8O7x4y6zfVux67JWdIRHGEf0L+UIJ/Bu/6sVYi9V9Q/5bB75/ppTnrn/qz4O/j1VV/a2v75ld8GdK0/gtYCV2/GfyP8K3/49Ek2mdLnPP47c1xUnfOgn8G/9Z/FSU2GmtIBNPe5Q/enKzIv/2vg7+X978fcLhq5aq/1tas8f3+/mf/x+Bv5dvfD2h71PvP9/6pOH99/ltK+K+/PxD8F/OJV4SxxZnil1N/dPi171LTPmyf+pfgH8H7D7w/cbb4QyPA9/zvR//O4O/mW2MTZYqht5jvnVibEHQuvMm0/JM/DP4+/u3vBzB/1FrCtV41Wo/2J7HYP/Xa/y34r+ZjxIgRI0aM/7fxnwAAAP//JkrrMBYUTS4AAAAASUVORK5CYII=",
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
-Account not found
```

- - - - - -

## Account IKEv2 Profile

**Request Structure:** `https://<puqvpnvp>/api/v1/account/<NAME>/ikev2_profile`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Example:**

```shell
curl \
-b "access_hash=4a1eaf3a9f086baa452bac3c4e92eb60e34755d23f36190f44720b9b43700c23543aabb2794eda15" \
-X GET https://dev.softkeel.com/api/v1/account/peer_10/ikev2_profile
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : "{\n\t\t\"uuid\": \"da7782cd-d00c-4114-9250-6c798585a441\",\n\t\t\"name\": \"dev.softkeel.com\",\n\t\t\"type\": \"ikev2-eap\",\n\t\t\"remote\": {\n\t\t  \"addr\": \"dev.softkeel.com\",\n\t\t  \"id\": \"dev.softkeel.com\",\n\t\t  \"cert\": \"-----BEGIN CERTIFICATE-----\rMIIFfDCCA2SgAwIBAgIIMYZL3xAvgfwwDQYJKoZIhvcNAQEMBQAwXDEQMA4GA1UE\rAxMHUFVRIFZQTjEXMBUGA1UEChMOUFVRIHNwLiB6IG8uby4xEDAOBgNVBAsTB1BV\rUSBWUE4xEDAOBgNVBAcTB1dhcnN6YXcxCzAJBgNVBAYTAlBMMB4XDTIyMTIwNTEx\rMzIzOFoXDTMyMTIwMjExMzIzOFowXDEQMA4GA1UEAxMHUFVRIFZQTjEXMBUGA1UE\rChMOUFVRIHNwLiB6IG8uby4xEDAOBgNVBAsTB1BVUSBWUE4xEDAOBgNVBAcTB1dh\rcnN6YXcxCzAJBgNVBAYTAlBMMIICIjANBgkqhkiG9w0BAQEFAAOCAg8AMIICCgKC\rAgEA1nYVzVwZxckXMsCeR3AnoPgvRHubvIslIPvp4lCFnSXZJhTXC5mmicZauPm1\rL0mpclc9umNOM1LxSHV4pcFYP+M1bDUYMef3iaufeQO3cU4R4UrJLsCC/WGwvw1o\rIqYDCxUtB0ePxZHNsBXDxu2/F0eVjX5SiPnCDxyY/tKsouJnX+bTGB5r0byeon6h\rA7V9mVrKJfKrIXhzKPtle28nFa9c6aRu+ROq3KotcradPSdzzzzFhCSCXChbI7+y\rdfnSiJ3rARREHljMpv0rWM/9NyCPHUIJaR+XJ8JQMDdQxMP8oN0fKB8y66foLiFD\roXWLvtGIFPkEnHbX2T7N//ly5xkA97upoQvo7wxtWV4xOIe1nfLesSZVCl/UL50d\r+LVf6NbguDda2HE15AuX6MjnOtX18Yn6VQNUo8R5rr+3dpuZnUYVzfdbnaVmmSuc\rISsQEUTZMzwTzCffpUwPzp8MMWB2K1pSOMTtC7o7cEjnv2BV8IuKhgK1V66lRapx\rcCWF/L1bHRasaqr5JCebGIVZNsd2qYJyuD6p0xP+VVo3PoboqusASKvbQ9PcoMdx\rm8GJHzNnJsuUQhapP2PpDpdht58p0xstWyPnANDsfbqooFWpwAJWhHlkl7JhQWuY\repEWKs78B3C2LYT6UeU4nJmRYNmsuclOUj9HpSJEMZ/nPnECAwEAAaNCMEAwDwYD\rVR0TAQH/BAUwAwEB/zAOBgNVHQ8BAf8EBAMCAQYwHQYDVR0OBBYEFFbCzI+j1Md8\rNjG1pCPq+ksO0MhgMA0GCSqGSIb3DQEBDAUAA4ICAQBpmyQRfUF/BiuF76vEcwci\rOuuiBaoPcEOwQIueje84KtaEwA0a+QKX4sPGHE4Eoxv7JHEJhBfoeKABTgpIv+qF\rnWdEO+sMTowLhrcoB1VPTw50w3mOYDLG+aqcC3e7UrXoMx+MWmPM3u3/zUkp5j/f\rAsIZL4YdXBtwqmmoj13zg6URslhXhlPeqw+OiqevfpPZE1a1IgXTEY0Xnba1B5o6\reRUCLcUO4dYjv3Eg55WKKN4uPkmm0u1JiWZp8g13FBK1hss/g1qkh3ZW5nMVDjTP\rGFGrY+eHLzEgM8RRieJpU+Jq9mmezp/r0pC0EqoDILxOUz05qm/c892D8ZZVqvKP\rTQnuHppAyYATGcPBIOHURi4ufCfiEzbaOjK6KLLJMRtGZEuMgTTz77HSvfuGP0/C\r+OVNxvSWcXf26AUhQHXS5wjFo6eLTWsfyi4ZegT9rTOUfwJ/x3hYCnxfGFsofgdh\rbL6jLJkygi+tjQAiJzNmmgRddDpun195Emc9yPYWQT5gz6qwy6ExhAmyfZ6fnIIr\rzWIYcS+oUh+mffeqjBHSUAPfFSlOiWfeshx+XN1oun0SiPaeA9YAb/eiKF+l/0Fl\rwX59Ea2Mr559mRB0Dg9OHMRMqG5K52gYy3V3tXg2/ZZNKeXML0OVbctf+hSkdsT4\rCZwL60LmJPQCBkNr6XOfBA==\r-----END CERTIFICATE-----\r\"\n\t\t},\n\t\t\"local\": {\n\t\t  \"eap_id\": \"user_104\"\n\t\t}\n\t  }",
   "status" : "success"
}

```

**Errors:**

```
-Not authorized
-Account not found
```

- - - - - -

## Account One-time link

**Request Structure:** `https://<puqvpnvp>/api/v1/account/<NAME>/otl`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Output:** url

**Example:**

```shell
curl \
-b "access_hash=eda121857897bcf0e4cdf5a3eaf957f35ccb62d39d5bc0bfbfb6d31644eee3cd7f8365e71ad94a60" \
-X GET https://dev.softkeel.com/api/v1/account/peer_10/otl
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : "https://dev.softkeel.com/otl/941baf43c2fd01e87e98db922c7d4aeb81ed27e1e88d6f3204c99dfae2f622b2433651f031cb461a",
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
-Account not found
```

- - - - - -

## Account Firewall mangle rules

**Request Structure:** `https://<puqvpnvp>/api/v1/account/<NAME>/firewall_mangle_rules`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Example:**

```shell
curl \
-b "access_hash=eda121857897bcf0e4cdf5a3eaf957f35ccb62d39d5bc0bfbfb6d31644eee3cd7f8365e71ad94a60" \
-X GET https://dev.softkeel.com/api/v1/account/peer_10/firewall_mangle_rules
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : "0.0.0.0/0 -> 10.0.105.18 MARK 0x6d Pkt:0 Bytes:0\n10.0.105.18 -> 0.0.0.0/0 MARK 0x6d Pkt:0 Bytes:0\n",
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
-Account not found
```

- - - - - -

## Account Traffic Control

**Request Structure:** `https://<puqvpnvp>/api/v1/account/<NAME>/traffic_control`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Example:**

```shell
curl \
-b "access_hash=eda121857897bcf0e4cdf5a3eaf957f35ccb62d39d5bc0bfbfb6d31644eee3cd7f8365e71ad94a60" \
-X GET https://dev.softkeel.com/api/v1/account/peer_10/traffic_control
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : "ens18 --> class htb 1:109 root leaf cb97: prio 0 rate 20Mbit ceil 20Mbit burst 1600b cburst 1600b \n Sent 0 bytes 0 pkt (dropped 0, overlimits 0 requeues 0) \n backlog 0b 0p requeues 0\n\nwg106 --> class htb 1:109 root leaf cb98: prio 0 rate 20Mbit ceil 20Mbit burst 1600b cburst 1600b \n Sent 0 bytes 0 pkt (dropped 0, overlimits 0 requeues 0) \n backlog 0b 0p requeues 0\n\n",
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
-Account not found
```

- - - - - -

## Account Dump

**Request Structure:** `https://<puqvpnvp>/api/v1/account/<NAME>/dump`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Example:**

```shell
curl \
-b "access_hash=eda121857897bcf0e4cdf5a3eaf957f35ccb62d39d5bc0bfbfb6d31644eee3cd7f8365e71ad94a60" \
-X GET https://dev.softkeel.com/api/v1/account/peer_10/dump
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "allowed_ips" : "10.0.105.18/32",
      "endpoint" : "(none)",
      "keepalive" : "off",
      "latest_handshake" : "0",
      "transfer_rx" : "0",
      "transfer_tx" : "0"
   },
   "status" : "success"
}

```

**Errors:**

```
-Not authorized
-Account not found
```

- - - - - -

## Account Traffic statistics

**Request Structure:** `https://<puqvpnvp>/api/v1/account/<NAME>/traffic_statistics/<YEAR>/<MONTH>`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Example:**

```shell
curl \
-b "access_hash=eda121857897bcf0e4cdf5a3eaf957f35ccb62d39d5bc0bfbfb6d31644eee3cd7f8365e71ad94a60" \
-X GET https://dev.softkeel.com/api/v1/account/ruslan_telefon/traffic_statistics/2022/11
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : [
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-01",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-02",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-03",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-04",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-05",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-06",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-07",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-08",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-09",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-10",
         "traffic_download" : 1209108969,
         "traffic_upload" : 375698174
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-11",
         "traffic_download" : 1588256401,
         "traffic_upload" : 406223360
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-12",
         "traffic_download" : 1963382022,
         "traffic_upload" : 49067202
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-13",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-14",
         "traffic_download" : 178929,
         "traffic_upload" : 127102
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-15",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-16",
         "traffic_download" : 168658637,
         "traffic_upload" : 15390640
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-17",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-18",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-19",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-20",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-21",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-22",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-23",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-24",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-25",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-26",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-27",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-28",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-29",
         "traffic_download" : 0,
         "traffic_upload" : 0
      },
      {
         "account" : "ruslan_telefon",
         "date" : "2022-11-30",
         "traffic_download" : 0,
         "traffic_upload" : 0
      }
   ],
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
-Account not found
-Wrong month setting
-Wrong year setting
```

- - - - - -