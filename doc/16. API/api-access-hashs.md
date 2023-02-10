# API Access Hashs

##### [Order now](https://panel.puqcloud.com/index.php?rp=/store/puqvpn) | [Download](https://download.puqcloud.com/cp/puqvpncp/)| [FAQ](https://faq.puqcloud.com)

##### To manage API Access Hashs, go to the section Settings-&gt;API

[![image-1668764483617.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1668764483617.png)](https://doc.puq.info/uploads/images/gallery/2022-11/image-1668764483617.png)

You can view/create/delete API Access Hashs.

<p class="callout info">Accept the fact that once the Access Hashs API is created, it will only be shown once.  
Each API Access Hash only works from a specific IP address.</p>

To authorize the API, API Access Hashs must be passed in the http header as the value of the "access\_hash" parameter in Cookies.

**API Root Link:** https://&lt;Your\_server&gt;/api/v1/

Application methods:

- **GET** - To get information about an object
- **POST** - Creating a new object
- **PUT** - Edit an existing object
- **DELETE** - Delete an existing object

**The data is sent to the server using the POST method.**

**Response from the server in json format**

**Each response from the server will have the same structure.**

```
{
   "error" : "",
   "msg" : "",
   "status" : ""
}
```

- **STATUS:**  if the result is successful then it will be "**SUCCESS"**, If the result is not successful it will be "**ERROR**"
- **MSG:** Here are the results of a successful request
- **ERROR:** In case of an error, the error text will appear here.

##### Here is an example using curl

```shell
curl \
-b "access_hash=7effe99173b87e9cdebdab66d6fb23c9b244af250cb09b5dd36d8f80d14a8510b2d00bcba7290252" \
-X GET https://dev.softkeel.com/api/v1/system/status
```

**Response example:**

```JSON
{
   "error" : "",
   "msg" : {
      "count_accounts" : 550,
      "count_accounts_available" : 550,
      "count_wireguard" : 100,
      "license" : "2023-11-13T18:38:43+01:00",
      "license_valid" : true,
      "status" : "Loading (Wireguard delete old interfaces)",
      "version" : "1.0"
   },
   "status" : "success"
}
```