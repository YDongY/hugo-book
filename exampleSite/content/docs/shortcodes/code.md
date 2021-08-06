# Python

```python
print("hello world")
```

# golang

```golang
package main

import "fmt"

func main(){
    fmt.Println("hello world")
}
```

# Nginx

```nginx
server {
    listen                  80;
    server_name             example.com example.com;

    location / {
        root /var/www/ydongy.github.io/public; # 自己的静态博客目录
        index index.html;
    }

    # nginx 转发 webhook 的请求，给 webhook.js ,注意端口和 js 监听端口一致
    location /webhook {
        proxy_pass http://127.0.0.1:6666;
    }
}
```

# MySQL

```mysql
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| demo               |
| django_tutorial    |
| fisher             |
| information_schema |
| mysite             |
| mysql              |
| orm_intro          |
| performance_schema |
| sys                |
| toutiao            |
+--------------------+
10 rows in set (0.02 sec)
```

# Jinja

```jinja
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>首页</title>
</head>
<body>
<h1>index</h1>
{{ username }}
{{ age }}
{{ gender }}
{{ info.phone }}
{{ info["phone"] }}
{{ info.email }}
{{ info.aaa }}
<a href="{{ url_for('login',ref="/") }}">登陆</a>
{{ value|default('默认值',boolean=True) }}

{% for x in range(1,10) %}
     ......代码块
{% endfor %}

</body>
</html>
```
