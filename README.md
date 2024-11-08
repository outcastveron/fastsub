## 优选代理

每 6 小时更新一次，使用 [clash-speedtest](https://github.com/faceair/clash-speedtest) 对 [go4sharing](https://raw.githubusercontent.com/go4sharing/sub/main/sub.yaml) 的节点进行测速，筛选出延迟低于 2s 且速度大于 5MB/s 的代理，并更新 [freesub.yaml](https://raw.githubusercontent.com/faceair/freesub/main/freesub.yaml)。

```yaml
proxy-providers:
  freesub:
    type: http
    url: https://raw.githubusercontent.com/faceair/freesub/main/freesub.yaml
    path: ./freesub.yaml
    health-check:
      enable: true
      interval: 300
      url: http://www.gstatic.com/generate_204
```

## LICENSE

MIT
