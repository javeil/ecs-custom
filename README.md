# ecs-custom

基于 [spiritLHLS/ecs](https://github.com/spiritLHLS/ecs) 的定制版融合怪测评脚本，将默认回程路由测试节点改为**天津三网**。

## 使用方法

```bash
bash <(curl -sL https://raw.githubusercontent.com/javeil/ecs-custom/main/ecs.sh)
```

## 与原版的区别

| 项目 | 原版 | 本版 |
|------|------|------|
| 默认回程路由节点 | 广州三网 | 天津三网 |
| 天津 `-r t` 参数 | 不支持 | 支持 |

### 天津三网节点 IP

| 运营商 | IP |
|-------|----|
| 天津电信 | `219.150.32.132` |
| 天津联通 | `202.99.96.68` |
| 天津移动 | `211.137.160.5` |

## 常用参数

```bash
# 默认测试（天津三网回程）
bash ecs.sh

# 指定回程路由节点
bash ecs.sh -r t   # 天津
bash ecs.sh -r b   # 北京
bash ecs.sh -r g   # 广州
bash ecs.sh -r s   # 上海
bash ecs.sh -r c   # 成都

# IPv6 三网
bash ecs.sh -r b6  # 北京 IPv6
bash ecs.sh -r g6  # 广州 IPv6
bash ecs.sh -r s6  # 上海 IPv6
```

## 致谢

- 原脚本作者：[spiritLHLS](https://github.com/spiritLHLS/ecs)
- 回程路由核心：[nexttrace](https://github.com/nxtrace/NTrace-core)、[backtrace](https://github.com/oneclickvirt/backtrace)
