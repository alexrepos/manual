# 环境变量

[![English][1]][2] [![German][3]][4] [![Russian][5]][6]

[1]: ../resources/english.svg
[2]: https://www.v2ray.com/en/configuration/env.html
[3]: ../resources/german.svg
[4]: https://www.v2ray.com/de/configuration/env.html
[5]: ../resources/russian.svg
[6]: https://www.v2ray.com/ru/configuration/env.html

V2Ray 提供以下环境变量以供修改 V2Ray 的一些底层配置。

## 每个连接的缓存大小 {#buffer-size}

* 名称: `v2ray.ray.buffer.size` 或 `V2RAY_RAY_BUFFER_SIZE`
* 单位: MBytes
* 默认值:
  * (V2Ray 3.33-) 统一为 10
  * (V2Ray 3.34+) 在 x86、amd64、arm64、s390x 上为 2，其它平台上禁用该缓存。
* 特殊值: 0 表示缓存无上限

对于一个代理连接，当上下游网络速度有差距时，V2Ray 会缓存一部分数据，以减小对网络传输的影响。这个配置设置了缓存的大小，越大的缓存会占用更多的内存，也会使网络性能越好。

## 资源文件路径 {#asset-location}

* 名称: `v2ray.location.asset` 或 `V2RAY_LOCATION_ASSET`
* 默认值: 和 v2ray 文件同路径

这个环境变量指定了一个文件夹位置，这个文件夹应当包含 geoip.dat 和 geosite.dat 文件。

## 配置文件位置 {#config-location}

* 名称: `v2ray.location.config` 或 `V2RAY_LOCATION_CONFIG`
* 默认值: 和 v2ray 文件同路径

这个环境变量指定了一个文件夹位置，这个文件夹应当包含 config.json 文件。
