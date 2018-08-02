# rtc-app-php

PHP AppServer for RTC.

You could also write AppServer by following languages:

* Golang: https://github.com/winlinvip/rtc-app-golang
* Java: https://github.com/winlinvip/rtc-app-java
* Python: https://github.com/winlinvip/rtc-app-python
* C#: https://github.com/winlinvip/rtc-app-csharp
* Nodejs: https://github.com/winlinvip/rtc-app-nodejs
* PHP: https://github.com/winlinvip/rtc-app-php

For RTC deverloper:

* RTC [workflow](https://help.aliyun.com/document_detail/74889.html).
* RTC [token generation](https://help.aliyun.com/document_detail/74890.html).

Use OpenAPI to create channel:

* Golang: https://help.aliyun.com/document_detail/74890.html#channel-golang
* Java: https://help.aliyun.com/document_detail/74890.html#channel-java
* Python: https://help.aliyun.com/document_detail/74890.html#channel-python
* C#: https://help.aliyun.com/document_detail/74890.html#channel-csharp
* Nodejs: https://help.aliyun.com/document_detail/74890.html#channel-nodejs
* PHP: https://help.aliyun.com/document_detail/74890.html#channel-php

Token generation algorithm:

* Golang: https://help.aliyun.com/document_detail/74890.html#token-golang
* Java: https://help.aliyun.com/document_detail/74890.html#token-java
* Python: https://help.aliyun.com/document_detail/74890.html#token-python
* C#: https://help.aliyun.com/document_detail/74890.html#token-csharp
* Nodejs: https://help.aliyun.com/document_detail/74890.html#token-nodejs
* PHP: https://help.aliyun.com/document_detail/74890.html#token-php

## Usage

1. Generate AK from [here](https://usercenter.console.aliyun.com/#/manage/ak):

```
AccessKeyID: OGAEkdiL62AkwSgs
AccessKeySecret: 4JaIs4SG4dLwPsQSwGAHzeOQKxO6iw
```

2. Create APP from [here](https://rtc.console.aliyun.com/#/manage):

```
AppID: iwo5l81k
```

4. Clone SDK:

```
git clone https://github.com/winlinvip/rtc-app-php.git &&
cd rtc-app-php/app/v1 &&
git clone https://github.com/aliyun/aliyun-openapi-php-sdk.git
```

5. Create DB file for php:

```
touch db.txt && chmod 777 db.txt
```

6. Create Config.php by your data:

```
echo "<?php" > Config.php
echo "\$listen = 8080;" >> Config.php
echo "\$region_id = 'cn-hangzhou'; " >> Config.php
echo "\$endpoint = 'rtc.aliyuncs.com'; " >> Config.php
echo "\$access_key_id = 'OGAEkdiL62AkwSgs'; " >> Config.php
echo "\$access_key_secret = '4JaIs4SG4dLwPsQSwGAHzeOQKxO6iw'; " >> Config.php
echo "\$app_id = 'iwo5l81k'; " >> Config.php
echo "\$gslb = 'https://rgslb.rtc.aliyuncs.com'; " >> Config.php
echo "?>" >> Config.php
```

> User can use other DB like MySQL.

7. Verify AppServer by [here](http://localhost:8080/app/v1/login.php?room=5678&user=nvivy&passwd=12345678).

> Remark: You can setup client native SDK by `http://30.2.228.19:8080/app/v1`.

> Remark: Please use your AppServer IP instead by `ifconfig eth0`.

## History

* Support create channel and sign user token.

