## Free Sub

> 本项目仅为 clash-speedtest 的功能演示。因为 Github Action 在国外机器上运行，筛选结果不代表国内直连的实际网络情况。

使用 [clash-speedtest](https://github.com/faceair/clash-speedtest) 对 [go4sharing](https://raw.githubusercontent.com/go4sharing/sub/main/sub.yaml) 的节点进行测速，筛选出延迟低于 2s 且速度大于 5MB/s 的节点，每 6 小时更新一次。

```yaml
proxy-providers:
  freesub:
    type: http
    url: https://raw.githubusercontent.com/faceair/freesub/main/freesub.yaml
    interval: 3600
    path: ./freesub.yaml
    health-check:
      enable: true
      interval: 300
      url: https://www.google.com/generate_204
```

## LICENSE

MIT
