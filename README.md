# Resource CDN

Resource Path: `/spiderbox/images/logo/bob.jpg`

| Usage                                                           | Provider   | Region |
| --------------------------------------------------------------- | ---------- | ------ | 
| `https://static.spiderapi.cn` + Resource Path                   |  aliyun    | CN     |
| `https://static-upyun.spiderapi.cn` + Resource Path             | upyun      | CN     |
| `https://cdn.jsdelivr.net/gh/TRHX/resources` + Resource Path    | jsdelivr   | World  |
| `https://cdn.jsdmirror.com/gh/TRHX/resources`  + Resource Path  | jsdmirror  | CN     |
| `https://jsd.onmicrosoft.cn/gh/TRHX/resources`  + Resource Path | 渺软公益CDN | CN     |

---

# jsDelivr 节点

来自：https://github.com/cqmzgg/cqmzgg.github.io/issues/20

jsDelivr 是由 @cloudflare 提供的免费开源公共 CDN。默认的提供的节点是 cdn.jsdelivr.net，但该节点在国内几乎不可用，需要使用可用性高的节点作为替代。

## 官方 jsDelivr 节点：

| 节点                       | ping 最快       | ping 最慢          | ping 平均 | 测试时间   | 备注          |
| -------------------------- | --------------- | ------------------ | --------- | ---------- | ------------- |
| fastly.jsdelivr.net        | 美国 <1ms       | 西藏[移动] 357ms    | 105.0ms   | 2024.09.03 |  国内使用一般  |
| quantil.jsdelivr.net       | 美国圣何塞 <1ms | 西藏[移动] 357ms     | 106.5ms   | 2024.09.03 |  国内使用一般  |
| originfastly.jsdelivr.net  | 美国洛杉矶 <1ms | 西藏[移动] 357ms     | 106.7ms   | 2024.09.03 |  国内使用一般  |
| cdn.jsdelivr.net           | 美国圣何塞 <1ms | 辽宁鞍山[电信] 890ms | 212.8ms   | 2024.09.03 |  国内使用较差  |
| gcore.jsdelivr.net         | 日本 <1ms       | 江苏南京[电信] 873ms | 272.4ms   | 2024.09.03 |  国内使用较差  |
| testingcf.jsdelivr.net     | 新加坡 <1ms     | 四川成都[电信] 861ms | 286.7ms   | 2024.09.03 |  国内使用较差  |
| test1.jsdelivr.net         |  找不到主机     | 找不到主机           | 找不到主机 | 2024.09.03 |  找不到主机    |

## 第三方 jsDelivr 节点：

| 节点               | ping 最快           | ping 最慢               | ping 平均 | 测试时间   | 备注                       |
| ------------------ | ------------------- | ----------------------- | -------- | ---------- | --------------------------- |
| cdn.jsdmirror.com  | 浙江宁波[电信] <1ms  | 德国 157ms              | 30.3ms   | 2024.09.03 | 国内 CDN，推荐               | 
| jsd.onmicrosoft.cn | 四川成都[电信] <1ms  | 美国 186ms              | 43.6ms   | 2024.09.03 | 国内 CDN                     |
| gh.776161.xyz      | 新加坡 <1ms          | 黑龙江哈尔滨[联通] 286ms | 152.4ms  | 2024.09.03 | 海外 CDN 优化回国            |
| jsdelivr.b-cdn.net | 中国台湾省 <1ms      | 新疆乌鲁木齐[移动] 394ms | 152.9ms  | 2024.09.03 | 台湾省 CDN                   |
| cdn.jsdelivr.us    | 荷兰 1ms            | 辽宁鞍山[电信] 330ms     | 223.2ms  | 2024.09.03 | 海外融合 Anycast/CDN 优化回国 |

# 静态资源公共库

使用公共库，需要注意可能会被投毒，参考：
- https://archive.is/cIn5g
- https://github.com/uBlockOrigin/uAssets/pull/24285
- https://www.bleepingcomputer.com/news/security/polyfillio-bootcdn-bootcss-staticfile-attack-traced-to-1-operator/

## 国内节点

| 节点                  | ping 最快           | ping 最慢              | ping 平均 | 测试时间   | 备注              |
| --------------------- | ------------------- | ---------------------- | -------- | ---------- | ------------------ |
| cdn.bytedance.com     | 山东济南[联通] <1ms  | 荷兰 252ms             | 28.6ms  | 2024.09.03 | 字节跳动，有段时间没更新了，推荐 |
| cdn.baomitu.com       | 北京[多线] 1ms       | 澳洲 221ms             | 46.7ms  | 2024.09.03 | 360前端，推荐                  |
| lib.sinaapp.com       | 山东青岛[多线] <1ms  | 荷兰 229ms             | 47.3ms  | 2024.09.03 | 新浪，有段时间没更新了          |
| npm.elemecdn.com      | 山东济南[联通] <1ms  | 荷兰 252ms             | 28.6ms  | 2024.09.03 | 饿了么同步快，缺的多            |
| unpkg.zhimg.com       | 山东济南[联通] <1ms  | 中国香港 144ms         | 11.5ms  | 2024.09.03 | 知乎同步慢                     |
| code.bdstatic.com/npm | 甘肃兰州[电信] <1ms  | 韩国 292ms             | 25.5ms  | 2024.09.03 | 百度仅同步热门包               |
| jscdn.upai.com        | 甘肃兰州[电信] <1ms  | 韩国 273ms             | 26.4ms  | 2024.09.03 | 又拍云，有段时间没更新了        |
| npm.onmicrosoft.cn    | 四川成都[电信] <1ms  | 美国 186ms             | 43.6ms   | 2024.09.03 | 公益节点，需准确的版本号       |
| npm.akass.cn          | 辽宁大连[电信] <1ms  | 新疆乌鲁木齐[电信] 78ms | 18.1ms   | 2024.09.03 | 公益需准确的版本号             |
| cdn.staticfile.net    | 中国台湾省 <1ms      | 黑龙江绥化[联通] 328ms  | 194.7ms  | 2024.09.03 | 保持最新，但有投毒风险，不推荐 |
| cdn.bootcdn.net       | 山东济南[联通] <1ms  | 江苏镇江[电信] 159ms    | 21.7ms   | 2024.09.03 | 保持最新，但有投毒风险，不推荐 |

## 国际节点

| 节点                  | ping 最快   | ping 最慢                | ping 平均 | 测试时间   | 备注             |
| --------------------- | ----------- | ------------------------ | -------- | ---------- | ------------------ |
| ajax.aspnetcdn.com    | 新加坡 <1ms | 河北石家庄[电信] 320ms     | 153.8ms  | 2024.09.03 |  microsoft，国内慢 | 
| unpkg.com             | 新加坡 <1ms | 内蒙古呼和浩特[电信] 898ms | 236.9ms  | 2024.09.03 | unpkg，国内慢       | 
| cdnjs.cloudflare.com  | 新加坡 <1ms | 湖北十堰[电信] 848ms       | 271.6ms  | 2024.09.03 | cloudflare，国内慢 | 

# Github 加速站

| 节点                  | ping 最快   | ping 最慢                | ping 平均 | 测试时间   | 备注             |
| --------------------- | ----------- | ------------------------ | -------- | ---------- | ------------------ |
| mirror.ghproxy.com    | 中国台湾省 57ms | 安徽合肥[移动] 380ms |  213.1ms | 2024.09.03 | |
| gh.mzec.top |  中国香港 2ms | 德国 320ms | 60.1ms | 2024.09.03 | |
| gh.mixyun.cyou |  德国 3ms | 美国圣何塞 253ms | 57.7ms | 2024.09.03 | |
| git.domob.org | 韩国 1ms | 荷兰 254ms | 74.6ms | 2024.09.03 | |
| ghproxy.053000.xyz | 日本 1ms | 德国 253ms | 87.6ms | 2024.09.03 | |
| gh.nxnow.top | 美国 32ms | 西藏[移动] 310ms | 181.7ms |  2024.09.03 | |
