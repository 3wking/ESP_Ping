# ESP_Ping
## 使用:
#### ESP8266
```Arduino
#include <ESP8266WiFi.h>
#include <ESP8266Ping.h>
```
#### ESP32
```Arduino
#include <WiFi.h>
#include <ESP32Ping.h>
```

调用' Ping.ping() '函数  < ip >
```Arduino
IPAddress ip (192, 168, 0, 1); // 要 ping 的ip
bool ret = Ping.ping(ip);
```

调用' Ping.ping() '函数  < 域名 >
```Arduino
bool ret = Ping.ping("www.google.com");
```

`ret` 如果远程响应了ping，那么ret`将为true，如果无法访问，则为false。

函数' Ping.ping() '第二个整数参数"count" ，该参数指定发送多少ping：
```Arduino
bool ret = Ping.ping(ip_or_host, 10);
```

调用' Ping.ping() '后 ，平均响应时间（以毫秒为单位）

```Arduino
int avg_time_ms = Ping.averageTime();
```
