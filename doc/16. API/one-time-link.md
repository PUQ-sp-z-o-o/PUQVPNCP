# One-time link

##### [Order now](https://panel.puqcloud.com/index.php?rp=/store/puqvpn) | [Download](https://download.puqcloud.com/cp/puqvpncp/)| [FAQ](https://faq.puqcloud.com)

## One-time link Config

**Request Structure:** `https://<puqvpnvp>/api/v1/otl/config`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Example:**

```shell
curl \
-b "access_hash=def77a57825907131fca3ba92fc22970ffe7429fd8b49535e178f59542c42cf2be854e296941de9f" \
-X GET https://dev.softkeel.com/api/v1/otl/config
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "after_body" : "\n<br>\n<br>\n<hr>\n<br>\n<br>\n<div class=\"intro\">\n\t<a href=\"https://doc.puq.info\">doc.puq.info</a>\n\t<br>\n\t<a href=\"https://www.puqcloud.com\">www.puqcloud.com</a>\n\t<hr>\n</div>\n<p>PUQ sp. z o.o.</p>\n\t",
      "before_body" : "\n<h1>This is a one-time link with configuration options</h1>\n\t",
      "css" : "\n* {\n\tbackground-color: #E5E5E5;\n\ttext-align: center;\n}\n\n.wireguard,.ikev2 {\n\tmargin: auto;\n\twidth: 550px;\n\ttext-align: center;\n}\n    \n.qr-img{\n\ttext-align: center;\n}\n\n.config-text{\n\ttext-align: center;\n\tdisplay: inline-block;\n}\n\n.config-text pre {\n\twidth: 550px;\n\ttext-align: left;\n\toverflow-x: auto;\n\ttab-width: 1; \n\toverflow-x: auto;\n\twhite-space: pre-wrap;\n\twhite-space: -moz-pre-wrap !important;\n\twhite-space: -pre-wrap;\n\twhite-space: -o-pre-wrap;\n\tword-wrap: break-word;\n\tbackground: #fff;\n}\n\n.btn {\n\twidth: 400px;\n\tborder: none;\n\tcolor: white;\n\tpadding: 4px 10px;\n\ttext-align: center;\n\ttext-decoration: none;\n\tdisplay: inline-block;\n\tfont-size: 20px;\n\tmargin: 5px 5px;\n\ttransition-duration: 0.5s;\n\tcursor: pointer;\n\tbackground-color: white;\n\tcolor: black;\n\tborder: 5px solid #008CBA;\n}\n.btn:hover {\n\tbackground-color: RoyalBlue;\n}\n\n.authorization_data {\n\ttext-align: center;\n\tfont-size: 20px;\n}\n.authorization_data table {\n\twidth: 100%;\n}\n\n@media only screen and (orientation: portrait){\n\t* h1 {\n\t\tfont-size: 50px;\n\t}\n\t.wireguard,.ikev2 {\n\t\twidth: 90%;\n\t\tmargin: auto;\n\t}\n\t.btn {\n\t\twidth: 90%;\n\t\tfont-size: 50px;\n\t\tmargin: 5px 5px;\n\t}\n\t.qr-img img{\n\t\twidth: 100%;\n\t\theight: 100%;\n\t}\n\t.config-text{\n\t\twidth: 100%;\n\t}\n\t.config-text pre {\n\t\twidth: 100%;\n\t}\n\t.authorization_data {\n\t\ttext-align: center;\n\t\tfont-size: 50px;\n\t}\n}\n",
      "lifetime" : "10",
      "not_relevant" : "\n<h1>This link is no longer relevant.</h1>\n<h1>Request a new link.</h1>\n<br>\n<div class=\"intro\">\n\t<a href=\"https://doc.puq.info\">doc.puq.info</a>\n\t<br>\n\t<a href=\"https://www.puqcloud.com\">www.puqcloud.com</a>\n\t<hr>\n</div>\n<p>PUQ sp. z o.o.</p>\n\t",
      "title" : "One-time link"
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
```

- - - - - -

## One-time link list

**Request Structure:** `https://<puqvpnvp>/api/v1/otl/list`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Example:**

```shell
curl \
-b "access_hash=def77a57825907131fca3ba92fc22970ffe7429fd8b49535e178f59542c42cf2be854e296941de9f" \
-X GET https://dev.softkeel.com/api/v1/otl/list
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "olts" : {
         "05fcdebdbd5744aa4df6b72386cacc0bea2b452475d5d31ff25744695c7372a2a3adaed3988382b8" : {
            "account" : "ruslan_windows",
            "created_data" : "2022-12-09",
            "key" : "05fcdebdbd5744aa4df6b72386cacc0bea2b452475d5d31ff25744695c7372a2a3adaed3988382b8",
            "lifetime" : "2022-12-19"
         },
         "569a3095db4c2251491e0dc19c302b1a9d5f64a67f83d53040cde52a108ea970d940926ca0eb58dc" : {
            "account" : "peer_101",
            "created_data" : "2022-12-09",
            "key" : "569a3095db4c2251491e0dc19c302b1a9d5f64a67f83d53040cde52a108ea970d940926ca0eb58dc",
            "lifetime" : "2022-12-19"
         },
         "84cb3a75982f739f68458e72e361ee3eae6f419400ce28713f88a371ff254a3f3db4392cf405a00f" : {
            "account" : "ruslan_windows",
            "created_data" : "2022-12-09",
            "key" : "84cb3a75982f739f68458e72e361ee3eae6f419400ce28713f88a371ff254a3f3db4392cf405a00f",
            "lifetime" : "2022-12-19"
         },
         "8d0fa51763d06ebe7db4d82e6f5a521421087b4a13e6b7fb1f5c1f6939171926437d23c8d66402ef" : {
            "account" : "ruslan_windows",
            "created_data" : "2022-12-09",
            "key" : "8d0fa51763d06ebe7db4d82e6f5a521421087b4a13e6b7fb1f5c1f6939171926437d23c8d66402ef",
            "lifetime" : "2022-12-19"
         },
         "b91361407612aec12803ecac999bba70a3b4b1466caa50c61344e93acac86f8f1caa7cc1f8bcafdc" : {
            "account" : "ruslan_windows",
            "created_data" : "2022-12-09",
            "key" : "b91361407612aec12803ecac999bba70a3b4b1466caa50c61344e93acac86f8f1caa7cc1f8bcafdc",
            "lifetime" : "2022-12-19"
         },
         "dbfa0ab6ba04d3c186031cd6b276c7405d030d12c6524e52accc4cd32e2e68554cf6fecabfb56c1e" : {
            "account" : "ruslan_dom_pc",
            "created_data" : "2022-12-10",
            "key" : "dbfa0ab6ba04d3c186031cd6b276c7405d030d12c6524e52accc4cd32e2e68554cf6fecabfb56c1e",
            "lifetime" : "2022-12-20"
         }
      }
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
```

- - - - - -

## One-time link WireGuard Config section

**Request Structure:** `https://<puqvpnvp>/api/v1/otl/config_wireguard`

**Method:** `GET`

**Cookie: `access_hash=<access_hash>`**

**Example:**

```shell
curl \
-b "access_hash=def77a57825907131fca3ba92fc22970ffe7429fd8b49535e178f59542c42cf2be854e296941de9f" \
-X GET https://dev.softkeel.com/api/v1/otl/config_wireguard
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "button1_label" : "Download client Android",
      "button1_link" : "https://play.google.com/store/apps/details?id=com.wireguard.android",
      "button2_label" : "Download client iOS",
      "button2_link" : "https://apps.apple.com/us/app/wireguard/id1441195209",
      "button3_label" : "Download client Windows",
      "button3_link" : "https://download.wireguard.com/windows-client/wireguard-installer.exe",
      "button4_label" : "Download client macOS",
      "button4_link" : "https://itunes.apple.com/us/app/wireguard/id1451685025",
      "button5_label" : "Official clients WireGuard",
      "button5_link" : "https://www.wireguard.com/install/",
      "button6_label" : "",
      "button6_link" : "",
      "download_config_button_label" : "Dowload config file",
      "enable" : true,
      "enable_config_qr" : true,
      "enable_config_text" : true
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
```

- - - - - -

## One-time link IKEv2 Config section

**Cookie: `access_hash=<access_hash>`**

**Example:**

```shell
curl \
-b "access_hash=def77a57825907131fca3ba92fc22970ffe7429fd8b49535e178f59542c42cf2be854e296941de9f" \
-X GET https://dev.softkeel.com/api/v1/otl/config_ikev2
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "button1_label" : "Download client Android",
      "button1_link" : "https://play.google.com/store/apps/details?id=org.strongswan.android",
      "button2_label" : "Download client Debian/Ubuntu",
      "button2_link" : "https://download.strongswan.org/NetworkManager/",
      "button3_label" : "Official clients strongSwan",
      "button3_link" : "https://download.strongswan.org/",
      "button4_label" : "",
      "button4_link" : "",
      "button5_label" : "",
      "button5_link" : "",
      "button6_label" : "",
      "button6_link" : "",
      "download_certificate_button_label" : "Dowload Certificate CA",
      "download_profile_button_label" : "Dowload Profile",
      "enable" : true
   },
   "status" : "success"
}
```

**Errors:**

```
-Not authorized
```

- - - - - -