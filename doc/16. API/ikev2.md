# IKEv2

##### [Order now](https://panel.puqcloud.com/index.php?rp=/store/puqvpn) | [Download](https://download.puqcloud.com/cp/puqvpncp/)| [FAQ](https://faq.puqcloud.com)

## IKEv2 info

**Request Structure:** `https://<puqvpnvp>/api/v1/ikev2/info`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Example:**

```shell
curl \
-b "access_hash=def77a57825907131fca3ba92fc22970ffe7429fd8b49535e178f59542c42cf2be854e296941de9f" \
-X GET https://dev.softkeel.com/api/v1/ikev2/info
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "pid_charon" : "1473837",
      "pid_starter" : "1473836",
      "strongswan" : "5.9.1-1+deb11u3"
   },
   "status" : "success"
}

```

**Errors:**

```
-Not authorized
```

- - - - - -

## IKEv2 Config

**Request Structure:** `https://<puqvpnvp>/api/v1/ikev2/config`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Example:**

```shell
curl \
-b "access_hash=def77a57825907131fca3ba92fc22970ffe7429fd8b49535e178f59542c42cf2be854e296941de9f" \
-X GET https://dev.softkeel.com/api/v1/ikev2/config
```

**Response example{Server configuration example}:**

```JSON
{
   "error" : "",
   "msg" : {
      "ca_cert" : "-----BEGIN CERTIFICATE-----\nMIIFfDCCA2SgAwIBAgIIMYZL3xAvgfwwDQYJKoZIhvcNAQEMBQAwXDEQMA4GA1UE\nAxMHUFVRIFZQTjEXMBUGA1UEChMOUFVRIHNwLiB6IG8uby4xEDAOBgNVBAsTB1BV\nUSBWUE4xEDAOBgNVBAcTB1dhcnN6YXcxCzAJBgNVBAYTAlBMMB4XDTIyMTIwNTEx\nMzIzOFoXDTMyMTIwMjExMzIzOFowXDEQMA4GA1UEAxMHUFVRIFZQTjEXMBUGA1UE\nChMOUFVRIHNwLiB6IG8uby4xEDAOBgNVBAsTB1BVUSBWUE4xEDAOBgNVBAcTB1dh\ncnN6YXcxCzAJBgNVBAYTAlBMMIICIjANBgkqhkiG9w0BAQEFAAOCAg8AMIICCgKC\nAgEA1nYVzVwZxckXMsCeR3AnoPgvRHubvIslIPvp4lCFnSXZJhTXC5mmicZauPm1\nL0mpclc9umNOM1LxSHV4pcFYP+M1bDUYMef3iaufeQO3cU4R4UrJLsCC/WGwvw1o\nIqYDCxUtB0ePxZHNsBXDxu2/F0eVjX5SiPnCDxyY/tKsouJnX+bTGB5r0byeon6h\nA7V9mVrKJfKrIXhzKPtle28nFa9c6aRu+ROq3KotcradPSdzzzzFhCSCXChbI7+y\ndfnSiJ3rARREHljMpv0rWM/9NyCPHUIJaR+XJ8JQMDdQxMP8oN0fKB8y66foLiFD\noXWLvtGIFPkEnHbX2T7N//ly5xkA97upoQvo7wxtWV4xOIe1nfLesSZVCl/UL50d\n+LVf6NbguDda2HE15AuX6MjnOtX18Yn6VQNUo8R5rr+3dpuZnUYVzfdbnaVmmSuc\nISsQEUTZMzwTzCffpUwPzp8MMWB2K1pSOMTtC7o7cEjnv2BV8IuKhgK1V66lRapx\ncCWF/L1bHRasaqr5JCebGIVZNsd2qYJyuD6p0xP+VVo3PoboqusASKvbQ9PcoMdx\nm8GJHzNnJsuUQhapP2PpDpdht58p0xstWyPnANDsfbqooFWpwAJWhHlkl7JhQWuY\nepEWKs78B3C2LYT6UeU4nJmRYNmsuclOUj9HpSJEMZ/nPnECAwEAAaNCMEAwDwYD\nVR0TAQH/BAUwAwEB/zAOBgNVHQ8BAf8EBAMCAQYwHQYDVR0OBBYEFFbCzI+j1Md8\nNjG1pCPq+ksO0MhgMA0GCSqGSIb3DQEBDAUAA4ICAQBpmyQRfUF/BiuF76vEcwci\nOuuiBaoPcEOwQIueje84KtaEwA0a+QKX4sPGHE4Eoxv7JHEJhBfoeKABTgpIv+qF\nnWdEO+sMTowLhrcoB1VPTw50w3mOYDLG+aqcC3e7UrXoMx+MWmPM3u3/zUkp5j/f\nAsIZL4YdXBtwqmmoj13zg6URslhXhlPeqw+OiqevfpPZE1a1IgXTEY0Xnba1B5o6\neRUCLcUO4dYjv3Eg55WKKN4uPkmm0u1JiWZp8g13FBK1hss/g1qkh3ZW5nMVDjTP\nGFGrY+eHLzEgM8RRieJpU+Jq9mmezp/r0pC0EqoDILxOUz05qm/c892D8ZZVqvKP\nTQnuHppAyYATGcPBIOHURi4ufCfiEzbaOjK6KLLJMRtGZEuMgTTz77HSvfuGP0/C\n+OVNxvSWcXf26AUhQHXS5wjFo6eLTWsfyi4ZegT9rTOUfwJ/x3hYCnxfGFsofgdh\nbL6jLJkygi+tjQAiJzNmmgRddDpun195Emc9yPYWQT5gz6qwy6ExhAmyfZ6fnIIr\nzWIYcS+oUh+mffeqjBHSUAPfFSlOiWfeshx+XN1oun0SiPaeA9YAb/eiKF+l/0Fl\nwX59Ea2Mr559mRB0Dg9OHMRMqG5K52gYy3V3tXg2/ZZNKeXML0OVbctf+hSkdsT4\nCZwL60LmJPQCBkNr6XOfBA==\n-----END CERTIFICATE-----\n",
      "ca_common_name" : "dev.softkeel.com",
      "ca_country_name" : "",
      "ca_key" : "-----BEGIN RSA PRIVATE KEY-----\n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\n-----END RSA PRIVATE KEY-----\n",
      "ca_locality" : "",
      "ca_organization" : "dev.softkeel.com",
      "ca_organizational_unit" : "",
      "ca_state_or_province_name" : "",
      "enabled" : true,
      "server_cert" : "-----BEGIN CERTIFICATE-----\nMIIFnTCCA4WgAwIBAgIIZqs60I6InzAwDQYJKoZIhvcNAQEMBQAwXDEQMA4GA1UE\nAxMHUFVRIFZQTjEXMBUGA1UEChMOUFVRIHNwLiB6IG8uby4xEDAOBgNVBAsTB1BV\nUSBWUE4xEDAOBgNVBAcTB1dhcnN6YXcxCzAJBgNVBAYTAlBMMB4XDTIyMTIxMTEw\nMzQyM1oXDTI3MTIxMDEwMzQyM1owUTEZMBcGA1UEAxMQZGV2LnNvZnRrZWVsLmNv\nbTEZMBcGA1UEChMQZGV2LnNvZnRrZWVsLmNvbTEZMBcGA1UECxMQZGV2LnNvZnRr\nZWVsLmNvbTCCAiIwDQYJKoZIhvcNAQEBBQADggIPADCCAgoCggIBANt/3Wdzsk88\ntLzJ4cw7plofxOgtXKkF01/j41MVtUNjysq4QhxvwXO96336npPYisPzZan7pIaq\nGN8EDcQ3tiQvCTOPu/JeoNTtEgUdy5/MXSGfl6981MxG0+njtE9+4WEg7D0wTgs2\nKuyVv1G/hpbz+XnkyPEYAXLVJXcwdFODZZkAuDk84olNr0QT/AeLKHf0QThTQipZ\nnDIn0OQs1zKULaw/kVs3owhAConAi8Vra5In63K0UBHetdL8eB/YgiGx/ZIcmQtf\nAWLEaUv0kRpv5iWoqqmtpODNVrZRxS/HN3lZWJZwO3DZfFtViADFS8xQ+jwPq2/R\nh6cs+OD3J7lSViJuKXEDyfvSzSf7dNrQQsjtAlkMqQVi134mEabhd6pZ2wNjPqvf\njOZge/ssYqmB+esIJsO3CmcVxop7aUzLx9HaAFNj1dyc2mFeIBovUqSaQLN103fY\n5axEJutRRFbRUNf55w71gPEKcSdkYfDAkG6pZn4+TD/Q28piMj+N8iLwsKWm3kgl\nzh9dhEPhaPhZL6nPy1p7t4YEr+07XumMzp6v5KcACSj7a8Jb+X+I9RjJ9NttvWo8\nPaR8of5dJ1d2AaQAPfqtXP3uq01cwpxwuAjVLkEAURFMIoznOTxleMucvV7FSgIn\nCbx5DbLGNGbPzGPPKGwpKWGbWw5qwErzAgMBAAGjbjBsMB8GA1UdIwQYMBaAFFbC\nzI+j1Md8NjG1pCPq+ksO0MhgMCoGA1UdEQQjMCGCEGRldi5zb2Z0a2VlbC5jb22C\nDTc3Ljg3LjEyNS4yMDAwHQYDVR0lBBYwFAYIKwYBBQUHAwEGCCsGAQUFCAICMA0G\nCSqGSIb3DQEBDAUAA4ICAQDOKUmPnSZcW0oj49WstpGzumNxQz25k6qqyPK3tuAm\n8DCVm+6vjVuApEdeVu+JlHOwJu1TdMiIUcHWRpF/gmgRewc27ZD86zWAVTjGOCuV\ne8aHP3CYIQzs5SHvfE389xKpsGV+5CPB93fxJ5jxGthbJ7wI1XZXTTmC66s0fE5F\nDVIi0e/d3vc5IWP9BLPOlWWUmDgmZi0Zosk1Lr3+1WQ4w+EIcSZ1jRc4/LmwoEXk\nr/Do/pP6oKkZ/zcuYFWGWzupUTc1nfU4pWOK2gxeleMO6YRL3EtM1LvMIdXgvZaO\nQ+HZ89P/4Ttt3r2XpgRcyddjv1iUbjyTuhmkX6xrF7n3p4740VwvdJ1bIaJOdVhc\n10Ii5vBaoLbQt7T3722UoMdKGTTpbC+fSA5hH1NrSwePgSG0f0stdKTVmQ4MXIK4\nYld92SMscQ4c/w/3s8+M3wGMOg2oXvjS7Z+FKvL+C51lQLIPDutEI3EQx/C4Zwtm\n6QvWYd2Cq7CsQ/E7ahr6NI8r9i08nSMZUqCQEj7glnTuPuwnl4wAgZ8X2Msdgv3F\n3tLhxVQLBgubtYK89/WskPEKKFZk/vhjz6yuFGwXW23NeRsFTRc446F4V08OZSEl\nA+mdfigBVsM1L8kdpuvIWH0rA52mhSou2odtcL2xlhLsYVhHl6mNMjo31J5uobHr\nPQ==\n-----END CERTIFICATE-----\n",
      "server_key" : "-----BEGIN RSA PRIVATE KEY-----\n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\n-----END RSA PRIVATE KEY-----\n",
      "server_common_name" : "dev.softkeel.com",
      "server_country_name" : "",
      "server_domain" : "dev.softkeel.com",
      "server_ip" : "77.87.125.200",
      "server_locality" : "",
      "server_organization" : "dev.softkeel.com",
      "server_organizational_unit" : "",
      "server_state_or_province_name" : ""
   },
   "status" : "success"
}
```

**Response example{Example of not configuring server}:**

```JSON
{
   "error" : "",
   "msg" : {
      "ca_cert" : "",
      "ca_common_name" : "dev.softkeel.com",
      "ca_country_name" : "",
      "ca_key" : "",
      "ca_locality" : "",
      "ca_organization" : "dev.softkeel.com",
      "ca_organizational_unit" : "",
      "ca_state_or_province_name" : "",
      "enabled" : false,
      "server_cert" : "",
      "server_common_name" : "dev.softkeel.com",
      "server_country_name" : "",
      "server_domain" : "dev.softkeel.com",
      "server_ip" : "77.87.125.200",
      "server_key" : "",
      "server_locality" : "",
      "server_organization" : "dev.softkeel.com",
      "server_organizational_unit" : "",
      "server_state_or_province_name" : ""
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
```

- - - - - -

## IKEv2 Import CA certificate and key

**Request Structure:** `https://<puqvpnvp>/api/v1/ikev2/import_ca_rsa`

**Cookie: `access_hash=<access_hash>`**

**Method: `PUT`**

**PUT data:**

**Options required:**

```JSON
"ca_cert" = ""
"ca_key" = ""
```

**Example:**

```shell
curl \
-b "access_hash=def77a57825907131fca3ba92fc22970ffe7429fd8b49535e178f59542c42cf2be854e296941de9f" \
-d "ca_cert=$(sed 's,+,%2B,g' <<EOF
-----BEGIN CERTIFICATE-----
MIIFfDCCA2SgAwIBAgIIMYZL3xAvgfwwDQYJKoZIhvcNAQEMBQAwXDEQMA4GA1UE
AxMHUFVRIFZQTjEXMBUGA1UEChMOUFVRIHNwLiB6IG8uby4xEDAOBgNVBAsTB1BV
USBWUE4xEDAOBgNVBAcTB1dhcnN6YXcxCzAJBgNVBAYTAlBMMB4XDTIyMTIwNTEx
MzIzOFoXDTMyMTIwMjExMzIzOFowXDEQMA4GA1UEAxMHUFVRIFZQTjEXMBUGA1UE
ChMOUFVRIHNwLiB6IG8uby4xEDAOBgNVBAsTB1BVUSBWUE4xEDAOBgNVBAcTB1dh
cnN6YXcxCzAJBgNVBAYTAlBMMIICIjANBgkqhkiG9w0BAQEFAAOCAg8AMIICCgKC
AgEA1nYVzVwZxckXMsCeR3AnoPgvRHubvIslIPvp4lCFnSXZJhTXC5mmicZauPm1
L0mpclc9umNOM1LxSHV4pcFYP+M1bDUYMef3iaufeQO3cU4R4UrJLsCC/WGwvw1o
IqYDCxUtB0ePxZHNsBXDxu2/F0eVjX5SiPnCDxyY/tKsouJnX+bTGB5r0byeon6h
A7V9mVrKJfKrIXhzKPtle28nFa9c6aRu+ROq3KotcradPSdzzzzFhCSCXChbI7+y
dfnSiJ3rARREHljMpv0rWM/9NyCPHUIJaR+XJ8JQMDdQxMP8oN0fKB8y66foLiFD
oXWLvtGIFPkEnHbX2T7N//ly5xkA97upoQvo7wxtWV4xOIe1nfLesSZVCl/UL50d
+LVf6NbguDda2HE15AuX6MjnOtX18Yn6VQNUo8R5rr+3dpuZnUYVzfdbnaVmmSuc
ISsQEUTZMzwTzCffpUwPzp8MMWB2K1pSOMTtC7o7cEjnv2BV8IuKhgK1V66lRapx
cCWF/L1bHRasaqr5JCebGIVZNsd2qYJyuD6p0xP+VVo3PoboqusASKvbQ9PcoMdx
m8GJHzNnJsuUQhapP2PpDpdht58p0xstWyPnANDsfbqooFWpwAJWhHlkl7JhQWuY
epEWKs78B3C2LYT6UeU4nJmRYNmsuclOUj9HpSJEMZ/nPnECAwEAAaNCMEAwDwYD
VR0TAQH/BAUwAwEB/zAOBgNVHQ8BAf8EBAMCAQYwHQYDVR0OBBYEFFbCzI+j1Md8
NjG1pCPq+ksO0MhgMA0GCSqGSIb3DQEBDAUAA4ICAQBpmyQRfUF/BiuF76vEcwci
OuuiBaoPcEOwQIueje84KtaEwA0a+QKX4sPGHE4Eoxv7JHEJhBfoeKABTgpIv+qF
nWdEO+sMTowLhrcoB1VPTw50w3mOYDLG+aqcC3e7UrXoMx+MWmPM3u3/zUkp5j/f
AsIZL4YdXBtwqmmoj13zg6URslhXhlPeqw+OiqevfpPZE1a1IgXTEY0Xnba1B5o6
eRUCLcUO4dYjv3Eg55WKKN4uPkmm0u1JiWZp8g13FBK1hss/g1qkh3ZW5nMVDjTP
GFGrY+eHLzEgM8RRieJpU+Jq9mmezp/r0pC0EqoDILxOUz05qm/c892D8ZZVqvKP
TQnuHppAyYATGcPBIOHURi4ufCfiEzbaOjK6KLLJMRtGZEuMgTTz77HSvfuGP0/C
+OVNxvSWcXf26AUhQHXS5wjFo6eLTWsfyi4ZegT9rTOUfwJ/x3hYCnxfGFsofgdh
bL6jLJkygi+tjQAiJzNmmgRddDpun195Emc9yPYWQT5gz6qwy6ExhAmyfZ6fnIIr
zWIYcS+oUh+mffeqjBHSUAPfFSlOiWfeshx+XN1oun0SiPaeA9YAb/eiKF+l/0Fl
wX59Ea2Mr559mRB0Dg9OHMRMqG5K52gYy3V3tXg2/ZZNKeXML0OVbctf+hSkdsT4
CZwL60LmJPQCBkNr6XOfBA==
-----END CERTIFICATE-----
EOF
)
&\
ca_key=$(sed 's,+,%2B,g' <<EOF
-----BEGIN RSA PRIVATE KEY-----
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
-----END RSA PRIVATE KEY-----
EOF
)
" \
-X PUT https://dev.softkeel.com/api/v1/ikev2/import_ca_rsa
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "ca_cert" : "-----BEGIN CERTIFICATE-----\nMIIFfDCCA2SgAwIBAgIIMYZL3xAvgfwwDQYJKoZIhvcNAQEMBQAwXDEQMA4GA1UE\nAxMHUFVRIFZQTjEXMBUGA1UEChMOUFVRIHNwLiB6IG8uby4xEDAOBgNVBAsTB1BV\nUSBWUE4xEDAOBgNVBAcTB1dhcnN6YXcxCzAJBgNVBAYTAlBMMB4XDTIyMTIwNTEx\nMzIzOFoXDTMyMTIwMjExMzIzOFowXDEQMA4GA1UEAxMHUFVRIFZQTjEXMBUGA1UE\nChMOUFVRIHNwLiB6IG8uby4xEDAOBgNVBAsTB1BVUSBWUE4xEDAOBgNVBAcTB1dh\ncnN6YXcxCzAJBgNVBAYTAlBMMIICIjANBgkqhkiG9w0BAQEFAAOCAg8AMIICCgKC\nAgEA1nYVzVwZxckXMsCeR3AnoPgvRHubvIslIPvp4lCFnSXZJhTXC5mmicZauPm1\nL0mpclc9umNOM1LxSHV4pcFYP+M1bDUYMef3iaufeQO3cU4R4UrJLsCC/WGwvw1o\nIqYDCxUtB0ePxZHNsBXDxu2/F0eVjX5SiPnCDxyY/tKsouJnX+bTGB5r0byeon6h\nA7V9mVrKJfKrIXhzKPtle28nFa9c6aRu+ROq3KotcradPSdzzzzFhCSCXChbI7+y\ndfnSiJ3rARREHljMpv0rWM/9NyCPHUIJaR+XJ8JQMDdQxMP8oN0fKB8y66foLiFD\noXWLvtGIFPkEnHbX2T7N//ly5xkA97upoQvo7wxtWV4xOIe1nfLesSZVCl/UL50d\n+LVf6NbguDda2HE15AuX6MjnOtX18Yn6VQNUo8R5rr+3dpuZnUYVzfdbnaVmmSuc\nISsQEUTZMzwTzCffpUwPzp8MMWB2K1pSOMTtC7o7cEjnv2BV8IuKhgK1V66lRapx\ncCWF/L1bHRasaqr5JCebGIVZNsd2qYJyuD6p0xP+VVo3PoboqusASKvbQ9PcoMdx\nm8GJHzNnJsuUQhapP2PpDpdht58p0xstWyPnANDsfbqooFWpwAJWhHlkl7JhQWuY\nepEWKs78B3C2LYT6UeU4nJmRYNmsuclOUj9HpSJEMZ/nPnECAwEAAaNCMEAwDwYD\nVR0TAQH/BAUwAwEB/zAOBgNVHQ8BAf8EBAMCAQYwHQYDVR0OBBYEFFbCzI+j1Md8\nNjG1pCPq+ksO0MhgMA0GCSqGSIb3DQEBDAUAA4ICAQBpmyQRfUF/BiuF76vEcwci\nOuuiBaoPcEOwQIueje84KtaEwA0a+QKX4sPGHE4Eoxv7JHEJhBfoeKABTgpIv+qF\nnWdEO+sMTowLhrcoB1VPTw50w3mOYDLG+aqcC3e7UrXoMx+MWmPM3u3/zUkp5j/f\nAsIZL4YdXBtwqmmoj13zg6URslhXhlPeqw+OiqevfpPZE1a1IgXTEY0Xnba1B5o6\neRUCLcUO4dYjv3Eg55WKKN4uPkmm0u1JiWZp8g13FBK1hss/g1qkh3ZW5nMVDjTP\nGFGrY+eHLzEgM8RRieJpU+Jq9mmezp/r0pC0EqoDILxOUz05qm/c892D8ZZVqvKP\nTQnuHppAyYATGcPBIOHURi4ufCfiEzbaOjK6KLLJMRtGZEuMgTTz77HSvfuGP0/C\n+OVNxvSWcXf26AUhQHXS5wjFo6eLTWsfyi4ZegT9rTOUfwJ/x3hYCnxfGFsofgdh\nbL6jLJkygi+tjQAiJzNmmgRddDpun195Emc9yPYWQT5gz6qwy6ExhAmyfZ6fnIIr\nzWIYcS+oUh+mffeqjBHSUAPfFSlOiWfeshx+XN1oun0SiPaeA9YAb/eiKF+l/0Fl\nwX59Ea2Mr559mRB0Dg9OHMRMqG5K52gYy3V3tXg2/ZZNKeXML0OVbctf+hSkdsT4\nCZwL60LmJPQCBkNr6XOfBA==\n-----END CERTIFICATE-----\n",
      "ca_common_name" : "dev.softkeel.com",
      "ca_country_name" : "",
      "ca_key" : "-----BEGIN RSA PRIVATE KEY-----\n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\n-----END RSA PRIVATE KEY-----\n",
      "ca_locality" : "",
      "ca_organization" : "dev.softkeel.com",
      "ca_organizational_unit" : "",
      "ca_state_or_province_name" : "",
      "enabled" : false,
      "server_cert" : "",
      "server_common_name" : "dev.softkeel.com",
      "server_country_name" : "",
      "server_domain" : "dev.softkeel.com",
      "server_ip" : "77.87.125.200",
      "server_key" : "",
      "server_locality" : "",
      "server_organization" : "dev.softkeel.com",
      "server_organizational_unit" : "",
      "server_state_or_province_name" : ""
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
-The root certificate is already in the system
-CaCert must be filled
-CaKey must be filled
-Certificate not found
-Certificate failed
```

- - - - - -

## IKEv2 Generate CA certificate and key

**Request Structure:** `https://<puqvpnvp>/api/v1/ikev2/generate_ca_rsa`

**Cookie: `access_hash=<access_hash>`**

**Method: `PUT`**

**PUT data:**

**Options required:**

```JSON
"ca_common_name" = ""
"ca_organization" = ""
```

**Options not required:**

```JSON
"ca_country_name" = ""
"ca_locality" = ""
"ca_organization" = ""
"ca_organizational_unit" = ""
"ca_state_or_province_name" = ""
```

**Example:**

```shell
curl \
-b "access_hash=def77a57825907131fca3ba92fc22970ffe7429fd8b49535e178f59542c42cf2be854e296941de9f" \
-d "ca_common_name=TEST_CN&\
ca_country_name=TEST_C&\
ca_locality=TEST_L&\
ca_organization=TEST_O&\
ca_organizational_unit=TEST_OU&\
ca_state_or_province_name=TEST_S&\
" \
-X PUT https://dev.softkeel.com/api/v1/ikev2/generate_ca_rsa
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "ca_cert" : "-----BEGIN CERTIFICATE-----\nMIIFlDCCA3ygAwIBAgIIP9dfvYShrW8wDQYJKoZIhvcNAQEMBQAwaDEQMA4GA1UE\nAwwHVEVTVF9DTjEPMA0GA1UECgwGVEVTVF9PMRAwDgYDVQQLDAdURVNUX09VMQ8w\nDQYDVQQHDAZURVNUX0wxDzANBgNVBAQMBlRFU1RfUzEPMA0GA1UEBgwGVEVTVF9D\nMB4XDTIyMTIxMTE1MzgwM1oXDTMyMTIwODE1MzgwM1owaDEQMA4GA1UEAwwHVEVT\nVF9DTjEPMA0GA1UECgwGVEVTVF9PMRAwDgYDVQQLDAdURVNUX09VMQ8wDQYDVQQH\nDAZURVNUX0wxDzANBgNVBAQMBlRFU1RfUzEPMA0GA1UEBgwGVEVTVF9DMIICIjAN\nBgkqhkiG9w0BAQEFAAOCAg8AMIICCgKCAgEA4dJvCvJ+4CDpYMVzEtWLyOpKLeeg\ns3yCWjKwHQubGXiTl9KsQLlrWTXYyFO3FhqygEZ3V0LUgBm4fWE+668dFa2b3qpp\nxmPJdw1TmnIwadQBZfJh9/Ve/fsnk6ktZKS03lgW0qKvwjCi02hTwNwzrrGUrueY\nO0dK1sKzGJdSD4hZQUQ7/8OnfQy7gsyVZbipXs9OOWQBdpbMhTDH/5xGVH0UmZyW\n0hYyb5pQVsayQQYC8FixltHwACohqoGDfNQVEYu8sg0bnHUf8n/+lH8Kuw01xZie\nIvpF0RoGWJIlwOCX4BHbYkHs/yygzbQFQ/F31ONHLGgrx282AemDaGKNlJKlghQi\nmBwW6Qwp3NJAgBXcV1iViyyagRmsFKP3Raya+KaG0RVjFQWoLJ71Bxv6LoVWIAfH\nMnAWRLuFrXcGA3zJrKKpDwEi3zBfFkiRNdj97BHKHcLKmkcmGwn9w4RaJtFoAuhO\nQAAjcEwSAjyhhQTGW/VjW0FqctmnHMFT1jldDlqy4i92QUrvmrdH+Lk8LE1MaZhh\nYWwwH6eDGHYBpE2056Yxn1if6/wvgcii3yC5kA/vg56BNkBwnTR3in74oYdXGbLO\nkOOqXI0/mSAWYN+bk3PQ7Gb5IlpMK6s0gyj3fixepzAtzm5+FttFib5pNoK1QILR\nLn54cO7TPprNg48CAwEAAaNCMEAwDwYDVR0TAQH/BAUwAwEB/zAOBgNVHQ8BAf8E\nBAMCAQYwHQYDVR0OBBYEFCGwbrB4NeaArXVbUE5B83SF1G8ZMA0GCSqGSIb3DQEB\nDAUAA4ICAQDE0kq0gV0Bj4w6JkjgYGnQrNSWRL1PuC4sI2DYWykP6ALYD+lxEv0X\nOV+zhIqrnDUzBXvqHLFwmyiwH+qIHpv0j0q8DdgPCf7WcjlRWvS5rjc0bjFbcwnJ\n1zLnMyrEdsC+acaQocaLzgg9yXuqh5KNImbgMG8oy+raosf4fAimHSUh3s5rxhjE\nV/S+QlGjDufw/RfgUzBM7C3DpXudA9CEQySyc2Kttcoe+2H3pU6TLuquqFIayIjv\nDb65o6mEJ2whF8HJzK8FjH+0MxvT7Bmm/E7Yg1WJWS/OLRdjeXzI8BmrnrUR5nb2\naek+AXq3QNDdLNM6a+hDX7hpgHA+0X8N72yu/vwmB8VJ7P36YYG0/a+VQLz6x9wY\njiqM7jPXAmyffRhxzkCfXIlScz4SHvKBcLHxExdIP3kWhuRw9l1fkgpIgBdz/0FS\nw0e0IXRC9b3EkidxpQZlgq5JkwwC1Juy0jrDUs/hMuqy+2cmc2oYeJ86jmGIBjb4\nyugjQvLJk8jQfuWU2OTxt5DKNFENdVTVZmRT176eT4/vzVIq9J4HzPJbYTQHGpK2\nIiCJjyf81wkGNckbz7nLlpnN67AsMO7hNrGpPMF96ipZZOw5YqG9TmNmLcOBvTYH\nzjMtZdeD605y+wMgUkiCYK1yZ+MnXD9odD6q7dj1HWpPsOGhTIeK9A==\n-----END CERTIFICATE-----\n",
      "ca_common_name" : "TEST_CN",
      "ca_country_name" : "TEST_C",
      "ca_key" : "-----BEGIN RSA PRIVATE KEY-----\n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\n-----END RSA PRIVATE KEY-----\n",
      "ca_locality" : "TEST_L",
      "ca_organization" : "TEST_O",
      "ca_organizational_unit" : "TEST_OU",
      "ca_state_or_province_name" : "TEST_S",
      "enabled" : false,
      "server_cert" : "",
      "server_common_name" : "dev.softkeel.com",
      "server_country_name" : "",
      "server_domain" : "dev.softkeel.com",
      "server_ip" : "77.87.125.200",
      "server_key" : "",
      "server_locality" : "",
      "server_organization" : "dev.softkeel.com",
      "server_organizational_unit" : "",
      "server_state_or_province_name" : ""
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
-The root certificate is already in the system
-Common Name must be filled
-Organization must be filled
```

- - - - - -

## IKEv2 Delete CA certificate and key

**Request Structure:** `https://<puqvpnvp>/api/v1/ikev2/delete_ca_rsa`

**Cookie: `access_hash=<access_hash>`**

**Method: `DELETE`**

**Example:**

```shell
curl \
-b "access_hash=def77a57825907131fca3ba92fc22970ffe7429fd8b49535e178f59542c42cf2be854e296941de9f" \
-X DELETE https://dev.softkeel.com/api/v1/ikev2/delete_ca_rsa
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "ca_cert" : "",
      "ca_common_name" : "TEST_CN",
      "ca_country_name" : "TEST_C",
      "ca_key" : "",
      "ca_locality" : "TEST_L",
      "ca_organization" : "TEST_O",
      "ca_organizational_unit" : "TEST_OU",
      "ca_state_or_province_name" : "TEST_S",
      "enabled" : false,
      "server_cert" : "",
      "server_common_name" : "dev.softkeel.com",
      "server_country_name" : "",
      "server_domain" : "dev.softkeel.com",
      "server_ip" : "77.87.125.200",
      "server_key" : "",
      "server_locality" : "",
      "server_organization" : "dev.softkeel.com",
      "server_organizational_unit" : "",
      "server_state_or_province_name" : ""
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
-The ROOT certificate is not present in the system
```

- - - - - -

## IKEv2 Generate SERVER certificate and key

**Request Structure:** `https://<puqvpnvp>/api/v1/ikev2/generate_server_rsa`

**Cookie: `access_hash=<access_hash>`**

**Method: `PUT`**

**PUT data:**

**Options required:**

```JSON
"server_domain" = ""
"server_ip" = ""
"server_common_name" = ""
"server_organization" = ""
```

**Options not required:**

```JSON
"server_organizational_unit" = ""
"server_organization" = ""
"server_locality" = ""
"server_state_or_province_name" = ""
"server_country_name" = ""
```

**Example:**

```shell
curl \
-b "access_hash=def77a57825907131fca3ba92fc22970ffe7429fd8b49535e178f59542c42cf2be854e296941de9f" \
-d "server_domain=vpn.test.test&\
server_ip=172.16.0.1&\
server_common_name=TEST_CN&\
server_organizational_unit=TEST_OU&\
server_organization=TEST_O&\
server_locality=TEST_L&\
server_state_or_province_name=TEST_S&\
server_country_name=TEST_S&\
" \
-X PUT https://dev.softkeel.com/api/v1/ikev2/generate_server_rsa
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "ca_cert" : "-----BEGIN CERTIFICATE-----\nMIIFlDCCA3ygAwIBAgIIaQxQOCqyX0MwDQYJKoZIhvcNAQEMBQAwaDEQMA4GA1UE\nAwwHVEVTVF9DTjEPMA0GA1UECgwGVEVTVF9PMRAwDgYDVQQLDAdURVNUX09VMQ8w\nDQYDVQQHDAZURVNUX0wxDzANBgNVBAQMBlRFU1RfUzEPMA0GA1UEBgwGVEVTVF9D\nMB4XDTIyMTIxMTE2MjAyN1oXDTMyMTIwODE2MjAyN1owaDEQMA4GA1UEAwwHVEVT\nVF9DTjEPMA0GA1UECgwGVEVTVF9PMRAwDgYDVQQLDAdURVNUX09VMQ8wDQYDVQQH\nDAZURVNUX0wxDzANBgNVBAQMBlRFU1RfUzEPMA0GA1UEBgwGVEVTVF9DMIICIjAN\nBgkqhkiG9w0BAQEFAAOCAg8AMIICCgKCAgEA2mAubwuBj55hq/Ukk7U916waAKUG\nb08RdUqzDqC+HP7wpwrg7q8JFKyCDCLQDbDQNZxRPwEIOphRrwY7ZJ8Rmdn2Mu9M\noQOIwOvcJ5vBj/8ge7ypaOvBtp3kezp+WR2k3WE1DVPLoPn+sdMFQawnsKo7U/8O\naUPEMRpMAYMDLR3FeckET0BfJIRWL1WTx4ho6URfIp0F1jntI4i+vcHZPPzRCorG\n86WdmvOoHzKPOH9aHTMBEtG6kHUS67EKgPyLSZDYVjSi1GO4HbOiymV36EMIbaQS\ntQrkj+P9ODsErbBj3SkjDQ8J6a1DlE07gruasR9kVKyGwZfTGRJBcjLzMEzOk7KS\nMj0Z5v3clq3TficJ9HuYjAND9nk0UNzTp0FfwJVJyA/bdu7ev340ZJcH6rhIP6/t\najNDRJPRzJsP+TeAeba41AjhYU6LJjEYyng8g1osui/Lqjlj/n059SO21nobPaCX\norIAYigVlfoS+Jp+vaoFfM0S742q/wa/WGvrsm8ikd8MoKbBJLl9mJJi64REpzkb\nwUxs+7efFF8neMNtDKpx83Ub0nqPM/UCdfTmi2iwLD4i5Bv+Xd0U/q1I51Kbna8l\nimQ1N26JGE2+1NVH5PQ/SO++q7NE4oYsgJqlJHt0nm6+k46mUXjVQojtuSVaDp30\n8q+LubCtTdGjwF0CAwEAAaNCMEAwDwYDVR0TAQH/BAUwAwEB/zAOBgNVHQ8BAf8E\nBAMCAQYwHQYDVR0OBBYEFN9i/vdCTH3z/zc693rCsHS1PtqNMA0GCSqGSIb3DQEB\nDAUAA4ICAQAcz/UIJa8VQqj0e9gSekZq9+EnpaGxSmf7pb6WDcX9dVDmRbiWMgHE\nJwWovePd6Jdb7XOhY3IrYGSQK9mEeRh4ac1guUEgQNRpbj+dEKpvvoYt8UQhuc7U\nrpyNggHfpzmYoMDJ/Z7EYbh5qnIkmqsTjnr4ZXEUxKC8iwxA41j5mRTrlGE5GGiC\nfrfLNI0NdTgnmvEXVTFj6wvGbw5qzerkRk22vwj/C2wBZBkd6CYrmAJk/5G4oWik\nTWrwTLqM+pxVI4YXO84dRysEf90cHy+T1y4YvNtowLJ4SkQYNhR5+xW8PWQM9JRG\n65xDrFBGm2cnhvGDpZGApy4mtg8n2stuK4C/QB+puNs6EoV1aMs2SPmxf5PJHSjQ\nuK32L+ZPw+9wPZnlUURLTIryyIwcY70Wjx4+kgzjANyxgEk8y77RuWdya8RocT8G\nQvglhyKZxpojXt5VUFIM2d8fnKTugeNeds9zgh5CjrVcBkh+q85Im3+t4a8tUqlq\nxvH5C0d4wxnHsNh/dQAlGxC5ppNKxYmR259KqGmGvW24vSO6BSnTmDrWGKiGlixW\nV4CfC9Cpnghqu6jEThUw1QY7E6YOfKn7kpx+t3QbQJa3MYSrumZRFEgVYXvg8tdY\nyehwxBWIhVZVCZFbKasBPeatv1hwH8IzWAJFLctcM6Kp4xdRQUrkxQ==\n-----END CERTIFICATE-----\n",
      "ca_common_name" : "TEST_CN",
      "ca_country_name" : "TEST_C",
      "ca_key" : "-----BEGIN RSA PRIVATE KEY-----\n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\n-----END RSA PRIVATE KEY-----\n",
      "ca_locality" : "TEST_L",
      "ca_organization" : "TEST_O",
      "ca_organizational_unit" : "TEST_OU",
      "ca_state_or_province_name" : "TEST_S",
      "enabled" : false,
      "server_cert" : "-----BEGIN CERTIFICATE-----\n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\n-----END CERTIFICATE-----\n",
      "server_common_name" : "TEST_CN",
      "server_country_name" : "TEST_S",
      "server_domain" : "vpn.test.test",
      "server_ip" : "172.16.0.1",
      "server_key" : "-----BEGIN RSA PRIVATE KEY-----\nMIIJKQIBAAKCAgEA1Fw/nJ9q3W3avtdBIJP6RNOUwsk80Km4ezzVw/ikoaLVMDwJ\nCOJr1R7zxYh9GGYZUj06cFtQ7Q0JPSyYmEXozLEBDIsia6N34kX4q7n2cb2lzIOU\nblVFer2SjSqHDr2hlNtOr7lh83TsSTiVxzkIQ/fUR3VjOxT4vz+Oh/VDOCuQY6Qb\nlGL2hoonuusGXY6FMQhErktCmfUkLJKVXmN3/EUg1J/cHe5TZ6XQ2YYBBAXxEwP/\n/DWFa/4eWou1D2PlvSs4nq+PSNupM/ZeOkVmtyX/0vGL76BMoy3ZD7E8CIXaXsX6\n5ez6/PL9S96l0D0z7b/UKmCESCFLly5gU3HzW6GQyykEw5X3g/Cocg+oUK6gSonw\ntzvqTmvsEvb3RokzjceZzvV52HRl9JfgqbCBJiKLMVgelggBCxrCr4qZVjA1m6K0\nZ8rG3nTPGxYGDU/flS8sUfcL9BfbO83JEy4sBExmD2VQKSJdsQnqQ+NxnFNyl4y1\nxY8rQ+oqr49xsu1rrC60GOWQ3jp7tbgGIvErVaCRuk64M7tmdrVT5pdS1XqHMI5f\n3vAigGsPjcNrFXSQLDttQdLmGq9SOcLqKeao0UINr0VsM3Mejmb92ns8cFvWmq+S\nWNJyplYRUiLskJKS2hnigdqYiLI9VWaQ8uIlLQbV6tRZxSw+0ZdTy+58rHMCAwEA\nAQKCAgAa/rsLYuyHx242MlDSHl2DIE5Z0JENiXWtHNejuNjcv0FQh2Eyou3IQs4E\nP0x/rILthGEIZWNNLwoMn72qJcDpPFsAyDMQ8c/MkM6CrfoZDV2lONjGicpyRuT5\nUv2mLw76SEKhbfR4qVVcHXhUwfg+A6QVjWOW4Bya2y54NAJegpMxR2xGGapzAd75\nEOVXQUXHLODmMyT9Qz9c9ylLvWNES1lYDhZCK8iodViuPi2k4Eh7/VcuLXOPfddH\n9ViH41ASEwt4iKKzRVEmDNx/ldDv2UHDA/eg94Smfa6JIyOZhcJzp8E0N0LUouL2\nIRB8/zq5r1f+JxTJwonEZx3Rnbusn95x+92aRXjMyhtzViwCIm9LODFZ0suKgELP\nd75FIksG5e4JJCP866ZqkxP50Hbu/02pZwPWsJn752PgiI/1CPvcVYbV8BcN6mAa\ngHGTr7lzbTbyJOaCEht6Y5q8Qckc7TysHfUwgDbohfa8Byra9ITR39JJ5hnuN73/\nABE6SDpYXaK5JCf0pv29fcrr76Kra+cJ49ZBNtBJIqM0neNDPcZrX+MbFt8KDo6l\nrClE0Xk7mfHmTxMsdM6zGhW2ktTCdc07irWwidGLVdeIhO6H+kMHul0yB3AwWqw2\ncqGWCabP21CtIO43wIMg9SskYZ3bUgLtE1STYZwQsOugNv3lEQKCAQEA+NwBolZd\nY1F7VOR5lUq7YQLIwdhnMkbF+HORpXuaNfwfw7t5ByMUSF0NQhF937/DsAX5QRm7\nXiwOPD/axedXzhozfCpQak/lCSvpkef9EgnxcsPl/etyHtI8wV1JhHHs5nsHG1DD\nsL766w/60Syk2zAU/S3r2I56VD2RzId1ouHmB/xuOe8UapEB+AnO3Dbwme5o++KQ\nSzCp9JlFxZmXlZ3h1nwh6dLhF62qP7RySIa+GHDph+Fl8/rVPyxU/qlumBEcRL39\nkqa2j5+RNRHWKvseylq0x2qWH1UrScW1WMd6ZoCczftYhANesFF5TvC0uttPufGN\no5wGeNBjyKpriwKCAQEA2nQjhUfKzQ6/qV7zugZN9+5FuRT2dZPCmH03B74U2LJW\nmesV+rf1gKaoS67Bex9egb3UigdaLHBGTI6SYYy7dUjv1g5VPFvfGoNsf4lVP6yN\nAc/3VQQlZjpM6YpONc6oXWso50m29FOuIpAbWafRG+WDXuHc9WVvd/1w6ToACPmL\n4/EDW12rPSUaNqWXBbmzhRpOIbHuIzBcx7mDn8sXVCDr8nlrCpvsd4c/Zh+jPcvg\n5wyvSVgeKYeEM9J2B8K/uUSnKZK7QQuseKqyeXtMZHNQdrg6WRNQ/nQW56eWsZRD\nBurG6qX0oweN6xE9/+pavWvea/DYXI6wDDhVK1F/uQKCAQBCxj3GAmiCis2OBNQ+\n49ONf0LBCMD/84+RT+lHvves/p7DVV1vNdFubVFuZeUhkYH/jErKVg45gZa8QeIA\n8kdULSGdcnkrXY62PEsq9FWqbnKT+c6PqIpxjLXyqIZefHc1jNNmV/B6T3RieGIz\nmEgP7EHlgVnkPK7ERdUGTV6aOwUPJYOqFeWjho9Br9gKrM84bolK9QsEseUYlbvr\n/n93DOsZMyuiYww030tsVo3HuiftxPZUmH1Tzv1DOzD/OBVNxmGQbG5K2GLp/MXo\nuIV/+OvVHiudypLHi4HXBK7ZSIUmVeI9PvEMUx8oLmRfcyT7cnddDFyWBvqRllD/\n+gJrAoIBAQCAPP09GE/s4GOSwbLB2UGb8bvsUmn7y6nIankLioIiU06TPHXCoIr1\n4t+YzhW2eUu5Tf6eqII+5AnglzFHIp5I03A3cGKI9EWcAtqGY9AveNOt5K+EsNJj\nmIXd8trGq3IapPV2EMfd1eG7WG01zFXs0ma0JFLZm5o8DgNiZjHvEs8UGD+oOuxz\nEHy656ooKkNAN5j2HsV00sckV7r06vve3xSjWrODntTJthN5l8j0VeLIv6GGpLvQ\nFUV+RmYTWDfEQpD+zqwuGvQ8QbhTqBXIQglSKAPYloZNWUi45KCJzkcqoFf1F0bt\nDVo6S/zhZmmuGMyRAOmCLCEci1U0ALvBAoIBAQCWFh8HAtiPaFtX3vJs/tpyaDMf\nCuudCtEVnjgk+jD4V+Qj7wFAVcyQ0qF+S2XaapyukN8Yz935DQ/54I8vhhZhs8z4\nd0Mjm5sD7DP/3fkafxBfg5znpDsVrRBk/vMV+kR9REiEnf6TaEcKWfjnihp2xWX3\nNwF+OL4ojiECh9WLPETNI2nQa3nQoB1+LztuQ+w27YLdDs2qIXLfnkj3aYj6UQ9i\n9OhiIY8ZjHq0EaGTxyAVCqlh07C3KwA0aHbvG84pDyDpMJIjVEMnVd2uH38qAw3b\nclvXzBF+s0KAPFI4qCQSyY0yKLA2e03EANAoqwBIsUDNUFo1EpHGbPtddeQD\n-----END RSA PRIVATE KEY-----\n",
      "server_locality" : "TEST_L",
      "server_organization" : "TEST_O",
      "server_organizational_unit" : "TEST_OU",
      "server_state_or_province_name" : "TEST_S"
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
-The root certificate is not present in the system
-Server Domain must be filled
-Server IP must be filled
-Common Name must be filled
-Organization must be filled
```

- - - - - -

## IKEv2 Delete SERVER certificate and key

**Request Structure:** `https://<puqvpnvp>/api/v1/ikev2/delete_server_rsa`

**Cookie: `access_hash=<access_hash>`**

**Method: `DELETE`**

**Example:**

```shell
curl \
-b "access_hash=def77a57825907131fca3ba92fc22970ffe7429fd8b49535e178f59542c42cf2be854e296941de9f" \
-X DELETE https://dev.softkeel.com/api/v1/ikev2/delete_server_rsa
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "ca_cert" : "-----BEGIN CERTIFICATE-----\nMIIFlDCCA3ygAwIBAgIIaQxQOCqyX0MwDQYJKoZIhvcNAQEMBQAwaDEQMA4GA1UE\nAwwHVEVTVF9DTjEPMA0GA1UECgwGVEVTVF9PMRAwDgYDVQQLDAdURVNUX09VMQ8w\nDQYDVQQHDAZURVNUX0wxDzANBgNVBAQMBlRFU1RfUzEPMA0GA1UEBgwGVEVTVF9D\nMB4XDTIyMTIxMTE2MjAyN1oXDTMyMTIwODE2MjAyN1owaDEQMA4GA1UEAwwHVEVT\nVF9DTjEPMA0GA1UECgwGVEVTVF9PMRAwDgYDVQQLDAdURVNUX09VMQ8wDQYDVQQH\nDAZURVNUX0wxDzANBgNVBAQMBlRFU1RfUzEPMA0GA1UEBgwGVEVTVF9DMIICIjAN\nBgkqhkiG9w0BAQEFAAOCAg8AMIICCgKCAgEA2mAubwuBj55hq/Ukk7U916waAKUG\nb08RdUqzDqC+HP7wpwrg7q8JFKyCDCLQDbDQNZxRPwEIOphRrwY7ZJ8Rmdn2Mu9M\noQOIwOvcJ5vBj/8ge7ypaOvBtp3kezp+WR2k3WE1DVPLoPn+sdMFQawnsKo7U/8O\naUPEMRpMAYMDLR3FeckET0BfJIRWL1WTx4ho6URfIp0F1jntI4i+vcHZPPzRCorG\n86WdmvOoHzKPOH9aHTMBEtG6kHUS67EKgPyLSZDYVjSi1GO4HbOiymV36EMIbaQS\ntQrkj+P9ODsErbBj3SkjDQ8J6a1DlE07gruasR9kVKyGwZfTGRJBcjLzMEzOk7KS\nMj0Z5v3clq3TficJ9HuYjAND9nk0UNzTp0FfwJVJyA/bdu7ev340ZJcH6rhIP6/t\najNDRJPRzJsP+TeAeba41AjhYU6LJjEYyng8g1osui/Lqjlj/n059SO21nobPaCX\norIAYigVlfoS+Jp+vaoFfM0S742q/wa/WGvrsm8ikd8MoKbBJLl9mJJi64REpzkb\nwUxs+7efFF8neMNtDKpx83Ub0nqPM/UCdfTmi2iwLD4i5Bv+Xd0U/q1I51Kbna8l\nimQ1N26JGE2+1NVH5PQ/SO++q7NE4oYsgJqlJHt0nm6+k46mUXjVQojtuSVaDp30\n8q+LubCtTdGjwF0CAwEAAaNCMEAwDwYDVR0TAQH/BAUwAwEB/zAOBgNVHQ8BAf8E\nBAMCAQYwHQYDVR0OBBYEFN9i/vdCTH3z/zc693rCsHS1PtqNMA0GCSqGSIb3DQEB\nDAUAA4ICAQAcz/UIJa8VQqj0e9gSekZq9+EnpaGxSmf7pb6WDcX9dVDmRbiWMgHE\nJwWovePd6Jdb7XOhY3IrYGSQK9mEeRh4ac1guUEgQNRpbj+dEKpvvoYt8UQhuc7U\nrpyNggHfpzmYoMDJ/Z7EYbh5qnIkmqsTjnr4ZXEUxKC8iwxA41j5mRTrlGE5GGiC\nfrfLNI0NdTgnmvEXVTFj6wvGbw5qzerkRk22vwj/C2wBZBkd6CYrmAJk/5G4oWik\nTWrwTLqM+pxVI4YXO84dRysEf90cHy+T1y4YvNtowLJ4SkQYNhR5+xW8PWQM9JRG\n65xDrFBGm2cnhvGDpZGApy4mtg8n2stuK4C/QB+puNs6EoV1aMs2SPmxf5PJHSjQ\nuK32L+ZPw+9wPZnlUURLTIryyIwcY70Wjx4+kgzjANyxgEk8y77RuWdya8RocT8G\nQvglhyKZxpojXt5VUFIM2d8fnKTugeNeds9zgh5CjrVcBkh+q85Im3+t4a8tUqlq\nxvH5C0d4wxnHsNh/dQAlGxC5ppNKxYmR259KqGmGvW24vSO6BSnTmDrWGKiGlixW\nV4CfC9Cpnghqu6jEThUw1QY7E6YOfKn7kpx+t3QbQJa3MYSrumZRFEgVYXvg8tdY\nyehwxBWIhVZVCZFbKasBPeatv1hwH8IzWAJFLctcM6Kp4xdRQUrkxQ==\n-----END CERTIFICATE-----\n",
      "ca_common_name" : "TEST_CN",
      "ca_country_name" : "TEST_C",
      "ca_key" : "-----BEGIN RSA PRIVATE KEY-----\n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\n-----END RSA PRIVATE KEY-----\n",
      "ca_locality" : "TEST_L",
      "ca_organization" : "TEST_O",
      "ca_organizational_unit" : "TEST_OU",
      "ca_state_or_province_name" : "TEST_S",
      "enabled" : false,
      "server_cert" : "",
      "server_common_name" : "TEST_CN",
      "server_country_name" : "TEST_S",
      "server_domain" : "vpn.test.test",
      "server_ip" : "172.16.0.1",
      "server_key" : "",
      "server_locality" : "TEST_L",
      "server_organization" : "TEST_O",
      "server_organizational_unit" : "TEST_OU",
      "server_state_or_province_name" : "TEST_S"
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
-The ROOT certificate is not present in the system
```

- - - - - -

## IKEv2 Enable/Disable

**Request Structure:** `https://<puqvpnvp>/api/v1/ikev2/`

**Cookie: `access_hash=<access_hash>`**

**Method: `PUT`**

**PUT data:**

**Options required:**

```JSON
"enabled" = "0|1"
```

**Example:**

```shell
curl \
-b "access_hash=def77a57825907131fca3ba92fc22970ffe7429fd8b49535e178f59542c42cf2be854e296941de9f" \
-d "enabled=1" \
-X PUT https://dev.softkeel.com/api/v1/ikev2
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "ca_cert" : "-----BEGIN CERTIFICATE-----\nMIIFlDCCA3ygAwIBAgIIaQxQOCqyX0MwDQYJKoZIhvcNAQEMBQAwaDEQMA4GA1UE\nAwwHVEVTVF9DTjEPMA0GA1UECgwGVEVTVF9PMRAwDgYDVQQLDAdURVNUX09VMQ8w\nDQYDVQQHDAZURVNUX0wxDzANBgNVBAQMBlRFU1RfUzEPMA0GA1UEBgwGVEVTVF9D\nMB4XDTIyMTIxMTE2MjAyN1oXDTMyMTIwODE2MjAyN1owaDEQMA4GA1UEAwwHVEVT\nVF9DTjEPMA0GA1UECgwGVEVTVF9PMRAwDgYDVQQLDAdURVNUX09VMQ8wDQYDVQQH\nDAZURVNUX0wxDzANBgNVBAQMBlRFU1RfUzEPMA0GA1UEBgwGVEVTVF9DMIICIjAN\nBgkqhkiG9w0BAQEFAAOCAg8AMIICCgKCAgEA2mAubwuBj55hq/Ukk7U916waAKUG\nb08RdUqzDqC+HP7wpwrg7q8JFKyCDCLQDbDQNZxRPwEIOphRrwY7ZJ8Rmdn2Mu9M\noQOIwOvcJ5vBj/8ge7ypaOvBtp3kezp+WR2k3WE1DVPLoPn+sdMFQawnsKo7U/8O\naUPEMRpMAYMDLR3FeckET0BfJIRWL1WTx4ho6URfIp0F1jntI4i+vcHZPPzRCorG\n86WdmvOoHzKPOH9aHTMBEtG6kHUS67EKgPyLSZDYVjSi1GO4HbOiymV36EMIbaQS\ntQrkj+P9ODsErbBj3SkjDQ8J6a1DlE07gruasR9kVKyGwZfTGRJBcjLzMEzOk7KS\nMj0Z5v3clq3TficJ9HuYjAND9nk0UNzTp0FfwJVJyA/bdu7ev340ZJcH6rhIP6/t\najNDRJPRzJsP+TeAeba41AjhYU6LJjEYyng8g1osui/Lqjlj/n059SO21nobPaCX\norIAYigVlfoS+Jp+vaoFfM0S742q/wa/WGvrsm8ikd8MoKbBJLl9mJJi64REpzkb\nwUxs+7efFF8neMNtDKpx83Ub0nqPM/UCdfTmi2iwLD4i5Bv+Xd0U/q1I51Kbna8l\nimQ1N26JGE2+1NVH5PQ/SO++q7NE4oYsgJqlJHt0nm6+k46mUXjVQojtuSVaDp30\n8q+LubCtTdGjwF0CAwEAAaNCMEAwDwYDVR0TAQH/BAUwAwEB/zAOBgNVHQ8BAf8E\nBAMCAQYwHQYDVR0OBBYEFN9i/vdCTH3z/zc693rCsHS1PtqNMA0GCSqGSIb3DQEB\nDAUAA4ICAQAcz/UIJa8VQqj0e9gSekZq9+EnpaGxSmf7pb6WDcX9dVDmRbiWMgHE\nJwWovePd6Jdb7XOhY3IrYGSQK9mEeRh4ac1guUEgQNRpbj+dEKpvvoYt8UQhuc7U\nrpyNggHfpzmYoMDJ/Z7EYbh5qnIkmqsTjnr4ZXEUxKC8iwxA41j5mRTrlGE5GGiC\nfrfLNI0NdTgnmvEXVTFj6wvGbw5qzerkRk22vwj/C2wBZBkd6CYrmAJk/5G4oWik\nTWrwTLqM+pxVI4YXO84dRysEf90cHy+T1y4YvNtowLJ4SkQYNhR5+xW8PWQM9JRG\n65xDrFBGm2cnhvGDpZGApy4mtg8n2stuK4C/QB+puNs6EoV1aMs2SPmxf5PJHSjQ\nuK32L+ZPw+9wPZnlUURLTIryyIwcY70Wjx4+kgzjANyxgEk8y77RuWdya8RocT8G\nQvglhyKZxpojXt5VUFIM2d8fnKTugeNeds9zgh5CjrVcBkh+q85Im3+t4a8tUqlq\nxvH5C0d4wxnHsNh/dQAlGxC5ppNKxYmR259KqGmGvW24vSO6BSnTmDrWGKiGlixW\nV4CfC9Cpnghqu6jEThUw1QY7E6YOfKn7kpx+t3QbQJa3MYSrumZRFEgVYXvg8tdY\nyehwxBWIhVZVCZFbKasBPeatv1hwH8IzWAJFLctcM6Kp4xdRQUrkxQ==\n-----END CERTIFICATE-----\n",
      "ca_common_name" : "TEST_CN",
      "ca_country_name" : "TEST_C",
      "ca_key" : "-----BEGIN RSA PRIVATE KEY-----\n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\n-----END RSA PRIVATE KEY-----\n",
      "ca_locality" : "TEST_L",
      "ca_organization" : "TEST_O",
      "ca_organizational_unit" : "TEST_OU",
      "ca_state_or_province_name" : "TEST_S",
      "enabled" : true,
      "server_cert" : "-----BEGIN CERTIFICATE-----\n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\n-----END CERTIFICATE-----\n",
      "server_common_name" : "TEST_CN",
      "server_country_name" : "TEST_S",
      "server_domain" : "vpn.test.test",
      "server_ip" : "172.16.0.1",
      "server_key" : "-----BEGIN RSA PRIVATE KEY-----\n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\n-----END RSA PRIVATE KEY-----\n",
      "server_locality" : "TEST_L",
      "server_organization" : "TEST_O",
      "server_organizational_unit" : "TEST_OU",
      "server_state_or_province_name" : "TEST_S"
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
-The ROOT certificate is not present in the system
-The SERVER certificate is not present in the system
```

- - - - - -

## IKEv2 Advanced settings show

**Request Structure:** `https://<puqvpnvp>/api/v1/ikev2/advanced_settings`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Example:**

```shell
curl \
-b "access_hash=def77a57825907131fca3ba92fc22970ffe7429fd8b49535e178f59542c42cf2be854e296941de9f" \
-X GET https://dev.softkeel.com/api/v1/ikev2/advanced_settings
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "authby" : "pubkey",
      "charondebug_asn" : 0,
      "charondebug_cfg" : 0,
      "charondebug_chd" : 0,
      "charondebug_dmn" : 0,
      "charondebug_enc" : 0,
      "charondebug_esp" : 0,
      "charondebug_ike" : 0,
      "charondebug_imc" : 0,
      "charondebug_imv" : 0,
      "charondebug_job" : 0,
      "charondebug_knl" : 0,
      "charondebug_lib" : 0,
      "charondebug_mgr" : 0,
      "charondebug_net" : 0,
      "charondebug_pts" : 0,
      "charondebug_tls" : 0,
      "charondebug_tnc" : 0,
      "closeaction" : "none",
      "compress" : "no",
      "dpdaction" : "clear",
      "dpddelay" : 300,
      "dpdtimeout" : 150,
      "esp" : "aes256-sha256,chacha20poly1305-sha512,aes256-sha1,aes256gcm16-ecp384,3des-sha1!",
      "forceencaps" : "yes",
      "fragmentation" : "yes",
      "ike" : "aes256-sha1-modp1024,aes128-sha1-modp1024,chacha20poly1305-sha512-curve25519-prfsha512,aes256gcm16-sha384-prfsha384-ecp384,3des-sha1-modp1024!",
      "ikelifetime" : 86400,
      "inactivity" : 86400,
      "installpolicy" : "yes",
      "keyingtries" : 5,
      "lifetime" : 3600,
      "margintime" : 600,
      "mobike" : "yes",
      "modeconfig" : "pull",
      "reauth" : "yes",
      "rekey" : "no",
      "rekeyfuzz" : 100,
      "strictcrlpolicy" : "no",
      "type" : "tunnel",
      "uniqueids" : "no"
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
```

- - - - - -

## IKEv2 Advanced settings set

**Request Structure:** `https://<puqvpnvp>/api/v1/ikev2/advanced_settings`

**Cookie: `access_hash=<access_hash>`**

**Method: `PUT`**

**PUT data:**

**Options required:**

```JSON
"charondebug_dmn" = "-1|0|1|2|3|4"
"charondebug_mgr" = "1|0|1|2|3|4"
"charondebug_ike" = "1|0|1|2|3|4"
"charondebug_chd" = "1|0|1|2|3|4"
"charondebug_job" = "1|0|1|2|3|4"
"charondebug_cfg" = "1|0|1|2|3|4"
"charondebug_knl" = "1|0|1|2|3|4"
"charondebug_net" = "1|0|1|2|3|4"
"charondebug_asn" = "1|0|1|2|3|4"
"charondebug_enc" = "1|0|1|2|3|4"
"charondebug_lib" = "1|0|1|2|3|4"
"charondebug_esp" = "1|0|1|2|3|4"
"charondebug_tls" = "1|0|1|2|3|4"
"charondebug_tnc" = "1|0|1|2|3|4"
"charondebug_imc" = "1|0|1|2|3|4"
"charondebug_imv" = "1|0|1|2|3|4"
"charondebug_pts" = "1|0|1|2|3|4"
"uniqueids" = "yes|no|never|replace|keep"
"strictcrlpolicy" = "yes|no|ifuri"
"authby" = "pubkey|rsasig|ecdsasig|psk|secret|xauthrsasig|xauthpsk|never"
"closeaction" = "none|clear|hold|restart"
"compress" = "yes|no"
"dpdaction" = "none|clear|hold|restart"
"dpddelay" = "0-2147483647"
"dpdtimeout" = "0-2147483647"
"inactivity" = "0-2147483647"
"esp" = ""
"forceencaps" = "yes|no"
"fragmentation" = "yes|accept|force|no"
"ike" = ""
"ikelifetime" = "0-2147483647"
"installpolicy" = "yes|no"
"keyingtries" = "1-2147483647"
"lifetime" = "1-86400"
"margintime" = "1-2147483647"
"mobike" = "yes|no"
"modeconfig" = "push|pull"
"reauth" = "yes|no"
"rekey" = "yes|no"
"rekeyfuzz" = "0-2147483647"
"type" = "tunnel|transport|transport_proxy|passthrough|drop"
```

**Example:**

```shell
curl \
-b "access_hash=def77a57825907131fca3ba92fc22970ffe7429fd8b49535e178f59542c42cf2be854e296941de9f" \
-d "authby=pubkey&\
charondebug_asn=1&\
charondebug_cfg=1&\
charondebug_chd=1&\
charondebug_dmn=1&\
charondebug_enc=1&\
charondebug_esp=1&\
charondebug_ike=1&\
charondebug_imc=1&\
charondebug_imv=1&\
charondebug_job=1&\
charondebug_knl=1&\
charondebug_lib=1&\
charondebug_mgr=1&\
charondebug_net=1&\
charondebug_pts=1&\
charondebug_tls=1&\
charondebug_tnc=1&\
closeaction=none&\
compress=no&\
dpdaction=clear&\
dpddelay=300&\
dpdtimeout=150&\
esp=$(sed -e 's,!,%21,g' <<EOF
aes256-sha256,chacha20poly1305-sha512,aes256-sha1,aes256gcm16-ecp384,3des-sha1!
EOF
)
&\
forceencaps=yes&\
fragmentation=yes&\
ike=$(sed -e 's,!,%21,g' <<EOF
aes256-sha1-modp1024,aes128-sha1-modp1024,chacha20poly1305-sha512-curve25519-prfsha512,aes256gcm16-sha384-prfsha384-ecp384,3des-sha1-modp1024!
EOF
)
&\
ikelifetime=86400&\
inactivity=86400&\
installpolicy=yes&\
keyingtries=5&\
lifetime=3600&\
margintime=600&\
mobike=yes&\
modeconfig=pull&\
reauth=yes&\
rekey=no&\
rekeyfuzz=100&\
strictcrlpolicy=no&\
type=tunnel&\
uniqueids=no" \
-X PUT https://dev.softkeel.com/api/v1/ikev2/advanced_settings
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "authby" : "pubkey",
      "charondebug_asn" : 1,
      "charondebug_cfg" : 1,
      "charondebug_chd" : 1,
      "charondebug_dmn" : 1,
      "charondebug_enc" : 1,
      "charondebug_esp" : 1,
      "charondebug_ike" : 1,
      "charondebug_imc" : 1,
      "charondebug_imv" : 1,
      "charondebug_job" : 1,
      "charondebug_knl" : 1,
      "charondebug_lib" : 1,
      "charondebug_mgr" : 1,
      "charondebug_net" : 1,
      "charondebug_pts" : 1,
      "charondebug_tls" : 1,
      "charondebug_tnc" : 1,
      "closeaction" : "none",
      "compress" : "no",
      "dpdaction" : "clear",
      "dpddelay" : 300,
      "dpdtimeout" : 150,
      "esp" : "aes256-sha256,chacha20poly1305-sha512,aes256-sha1,aes256gcm16-ecp384,3des-sha1!",
      "forceencaps" : "yes",
      "fragmentation" : "yes",
      "ike" : "aes256-sha1-modp1024,aes128-sha1-modp1024,chacha20poly1305-sha512-curve25519-prfsha512,aes256gcm16-sha384-prfsha384-ecp384,3des-sha1-modp1024!",
      "ikelifetime" : 86400,
      "inactivity" : 86400,
      "installpolicy" : "yes",
      "keyingtries" : 5,
      "lifetime" : 3600,
      "margintime" : 600,
      "mobike" : "yes",
      "modeconfig" : "pull",
      "reauth" : "yes",
      "rekey" : "no",
      "rekeyfuzz" : 100,
      "strictcrlpolicy" : "no",
      "type" : "tunnel",
      "uniqueids" : "no"
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
-Incorrect value Charondebug dmn (should be -1 to 4)
-Incorrect value Charondebug mgr (should be -1 to 4)
-Incorrect value Charondebug ike (should be -1 to 4)
-Incorrect value Charondebug chd (should be -1 to 4)
-Incorrect value Charondebug job (should be -1 to 4)
-Incorrect value Charondebug cfg (should be -1 to 4)
-Incorrect value Charondebug knl (should be -1 to 4)
-Incorrect value Charondebug net (should be -1 to 4)
-Incorrect value Charondebug asn (should be -1 to 4)
-Incorrect value Charondebug enc (should be -1 to 4)
-Incorrect value Charondebug lib (should be -1 to 4)
-Incorrect value Charondebug esp (should be -1 to 4)
-Incorrect value Charondebug tls (should be -1 to 4)
-Incorrect value Charondebug tnc (should be -1 to 4)
-Incorrect value Charondebug imc (should be -1 to 4)
-Incorrect value Charondebug imv (should be -1 to 4)
-Incorrect value Charondebug pts (should be -1 to 4)
-Incorrect value Uniqueids (should be yes|no|never|replace|keep)
-Incorrect value Strictcrlpolicy (should be yes|no|ifuri)
-Incorrect value Authby (should be pubkey|rsasig|ecdsasig|psk|secret|xauthrsasig|xauthpsk|never)
-Incorrect value Closeaction (should be none|clear|hold|restart)
-Incorrect value Compress (should be yes|no)
-Incorrect value Closeaction (should be none|clear|hold|restart)
-Incorrect value Dpddelay (should be 0 to 2147483647)
-Incorrect value Dpdtimeout (should be 0 to 2147483647)
-Incorrect value Inactivity (should be 0 to 2147483647)
-Esp must be filled
-Incorrect value Forceencaps (should be yes|no)
-Incorrect value Forceencaps (should be yes|accept|force|no)
-Ike must be filled
-Incorrect value Ikelifetime (should be 0 to 2147483647)
-Incorrect value Installpolicy (should be yes|no)
-Incorrect value Keyingtries (should be 1 to 2147483647)
-Incorrect value Lifetime (should be 1 to 86400)
-Incorrect value Margintime (should be 1 to 2147483647)
-Incorrect value Mobike (should be yes|no)
-Incorrect value Modeconfig (should be  push|pull)
-Incorrect value Reauth (should be yes|no)
-Incorrect value Rekey (should be yes|no)
-Incorrect value Keyingtries (should be 0 to 2147483647)
-Incorrect value Type (should be  tunnel|transport|transport_proxy|passthrough|drop)
```

- - - - - -

## IKEv2 Advanced settings set default

**Request Structure:** `https://<puqvpnvp>/api/v1/ikev2/advanced_settings/default`

**Cookie: `access_hash=<access_hash>`**

**Method: `PUT`**

**Example:**

```shell
curl \
-b "access_hash=def77a57825907131fca3ba92fc22970ffe7429fd8b49535e178f59542c42cf2be854e296941de9f" \
-X PUT https://dev.softkeel.com/api/v1/ikev2/advanced_settings/default
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "authby" : "pubkey",
      "charondebug_asn" : 0,
      "charondebug_cfg" : 0,
      "charondebug_chd" : 0,
      "charondebug_dmn" : 0,
      "charondebug_enc" : 0,
      "charondebug_esp" : 0,
      "charondebug_ike" : 0,
      "charondebug_imc" : 0,
      "charondebug_imv" : 0,
      "charondebug_job" : 0,
      "charondebug_knl" : 0,
      "charondebug_lib" : 0,
      "charondebug_mgr" : 0,
      "charondebug_net" : 0,
      "charondebug_pts" : 0,
      "charondebug_tls" : 0,
      "charondebug_tnc" : 0,
      "closeaction" : "none",
      "compress" : "no",
      "dpdaction" : "clear",
      "dpddelay" : 300,
      "dpdtimeout" : 150,
      "esp" : "aes256-sha256,chacha20poly1305-sha512,aes256-sha1,aes256gcm16-ecp384,3des-sha1!",
      "forceencaps" : "yes",
      "fragmentation" : "yes",
      "ike" : "aes256-sha1-modp1024,aes128-sha1-modp1024,chacha20poly1305-sha512-curve25519-prfsha512,aes256gcm16-sha384-prfsha384-ecp384,3des-sha1-modp1024!",
      "ikelifetime" : 86400,
      "inactivity" : 86400,
      "installpolicy" : "yes",
      "keyingtries" : 5,
      "lifetime" : 3600,
      "margintime" : 600,
      "mobike" : "yes",
      "modeconfig" : "pull",
      "reauth" : "yes",
      "rekey" : "no",
      "rekeyfuzz" : 100,
      "strictcrlpolicy" : "no",
      "type" : "tunnel",
      "uniqueids" : "no"
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
```

- - - - - -

##  

##  

##  