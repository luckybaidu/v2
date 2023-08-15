支持 V2Ray 绝大多数传输协议，WebSocket + TLS，HTTP/2，Shadowsocks，动态端口，集成 BBR 和锐速优化等。

前言
V2Ray 官网：https://www.v2ray.com

V2Ray 是一个于 Shadowsocks 之后非常好用的代理软件，但是由于 V2Ray 的配置略复杂，GUI 客户端不完善，所以 V2Ray 并没有像 Shadowsocks 在科学上网人群之中那么流行。
不过我想，像我这种小小白萌新，更需要的是一个好用的一键安装脚本……
所以，此脚本是为了方便像我这种小小白萌新更加容易去使用 V2Ray，配置 V2Ray。希望对你有帮助 ^_^

如果你是毫无经验的小白，搭建 V2Ray 请看此教程：V2Ray搭建详细图文教程

更新日志
2018-01-28
第一个完善版本发布…
2018-5-2
支持 HTTP/2 … 懒得发一个版本就在这里写一下
2018-5-26
支持 Socks5 …
2019-1-5
v3.05 版本，更加好用了。新年快乐！

温馨提示
特么这个脚本没有挖矿，没有挖矿，没有挖矿。 我很抱歉……认真的开了个玩笑
脚本是开源的，开源地址： https://github.com/233boy/v2ray

功能特点
支持 V2Ray 多数传输协议
支持 WebSocket + TLS / HTTP/2
支持 动态端口 (WebSocket + TLS，Socks5， HTTP/2 除外)
支持 屏蔽广告
支持 配置 Shadowsocks
支持 下载客户端配置文件 (不用 Xshell 也可以下载)
客户端配置文件同时支持 SOCKS 和 HTTP
支持 生成 V2Ray 配置二维码链接 (仅适用部分客户端)
支持 生成 V2Ray 配置信息链接
支持 生成 Shadowsocks 配置二维码链接
支持修改 V2Ray 传输协议
支持修改 V2Ray 端口
支持修改 动态端口
支持修改 用户ID
支持修改 TLS 域名
支持修改 Shadowsocks 端口
支持修改 Shadowsocks 密码
支持修改 Shadowsocks 加密协议
自动启用 BBR 优化 (如果内核支持)
集成可选安装 BBR (by teddysun.com)
集成可选安装 锐速 (by moeclub.org)
一键 查看运行状态 / 查看配置信息 / 启动 / 停止 / 重启 / 更新 / 卸载 / 等等…
人性化向导 & 纯净安装 & 卸载彻底

哈哈哈..我故意要写够 23 条的。说着当然，脚本肯定都会有如上所说的功能。

安装或卸载
温馨提醒，此脚本默认屏蔽一些不友好的网站！(仅限轮子相关)

要求：Ubuntu 16+ / Debian 8+ / CentOS 7+ 系统
推荐使用 Debian 9 系统，脚本会自动启用 BBR 优化。
备注：不推荐使用 Debian 8 系统，因为 Caddy 申请证书可能会出现一些莫名其妙的问题
强烈推荐使用 搬瓦工VPS，稳定，快速，针对中国线路专门优化，完全无须担心跑路，服务好，30天退款保证。
在这里可以找到 搬瓦工 VPS 套餐大全 ，优惠码在这里： 搬瓦工 VPS 优惠码
使用 root 用户输入下面命令安装或卸载

bash <(curl -s -L https://git.io/v2ray.sh)
如果提示 curl: command not found ，那是因为你的 VPS 没装 Curl
ubuntu/debian 系统安装 Curl 方法: apt-get update -y && apt-get install curl -y
centos 系统安装 Curl 方法: yum update -y && yum install curl -y
安装好 curl 之后就能安装脚本了

备注：安装完成后，输入 v2ray 即可管理 V2Ray
如果提示你的系统不支持此脚本，那么请尝试更换系统

下面是此脚本的一些截图

安装选项

安装 V2Ray
配置 Shadowsocks

配置 Shadowsocks
安装完成

V2Ray 安装完成
管理面板

V2Ray 管理面板
Telegram 专用代理
如果你在使用 Telegram 的话，你可以配置一个 Telegram 的专用代理，这样来，在某些情况下你就不需要再开一个代理软件了。
输入 v2ray tg 即可配置 TG 专用代理
配置 Telegram MTProto

配置Telegram MTProto
Telegram MTProto 配置信息

Telegram MTProto 配置信息
快速管理
v2ray info 查看 V2Ray 配置信息
v2ray config 修改 V2Ray 配置
v2ray link 生成 V2Ray 配置文件链接
v2ray infolink 生成 V2Ray 配置信息链接
v2ray qr 生成 V2Ray 配置二维码链接
v2ray ss 修改 Shadowsocks 配置
v2ray ssinfo 查看 Shadowsocks 配置信息
v2ray ssqr 生成 Shadowsocks 配置二维码链接
v2ray status 查看 V2Ray 运行状态
v2ray start 启动 V2Ray
v2ray stop 停止 V2Ray
v2ray restart 重启 V2Ray
v2ray log 查看 V2Ray 运行日志
v2ray update 更新 V2Ray
v2ray update.sh 更新 V2Ray 管理脚本
v2ray uninstall 卸载 V2Ray

配置文件路径
V2Ray 配置文件路径：/etc/v2ray/config.json
Caddy 配置文件路径：/etc/caddy/Caddyfile
脚本配置文件路径: /etc/v2ray/233blog_v2ray_backup.conf

警告，请不要修改脚本配置文件，免得出错。。
如果你不是有特别的需求，也不要修改 V2Ray 配置文件
不过也没事，若你实在想要瞎折腾，出错了的话，你就卸载，然后重装，再出错 ，再卸载，再重装，重复到自己不再想折腾为止。。

WS+TLS / HTTP2
如果你使用了这两个协议，那么就会使用了脚本自带的 Caddy 集成
不管如何，不建议直接去更改 Caddy 的配置：/etc/caddy/Caddyfile
如果你需要配置其他网站相关，请将网站的配置文件放到 /etc/caddy/sites 目录下，然后重启 Caddy 进程即可，脚本默认生成的 Caddy 的配置会加载 /etc/caddy/sites 这个目录下的所有配置文件。
所以，请将你的网站配置文件放到 /etc/caddy/sites 目录下，完完全全不需要去更改 /etc/caddy/Caddyfile
记得重启 Caddy 进程：service caddy restart

Caddy 插件相关
本脚本集成了 Caddy，但不集成任何 Caddy 插件，如果你需要安装某些 Caddy 插件，你可以使用官方的 Caddy 安装脚本来一键安装。
本人的脚本集成的 Caddy 的安装路径，跟 Caddy 官方的安装脚本是一致的。所以可以直接安装，不会有任何问题

举个例子，安装包含 http.filebrowser 插件的 Caddy，执行如下命令即可

curl https://getcaddy.com | bash -s personal http.filebrowser
你可以在 https://caddyserver.com/download 找到 Caddy 更多插件和安装命令。

备注
V2Ray 客户端配置文件 SOCKS 监听端口为 2333， HTTP 监听端口为 6666
可能某些 V2Ray 客户端的选项或描述略有不同，但事实上，此脚本显示的 V2Ray 配置信息已经足够详细，由于客户端的不同，请对号入座。

反馈问题
请先查阅：V2Ray 一键安装脚本疑问集合
Telegram 群组： https://t.me/blog233
Github 反馈： https://github.com/233boy/v2ray/issues
任何有关于 V2Ray 的问题，请自行到 V2Ray 官方反馈。
目前只支持配置一个 V2Ray 账号…一个 Shadowsocks 账号。。不支持 SSR。。
使用国际大厂的 VPS，请自行在安全组 (防火墙) 开放端口和 UDP 协议 (如果你要使用含有 mKCP 的传输协议)

备份
为了避免由于不可抗拒的原因所造成本人主动删除脚本，所以建议请将本脚本 Fork 一份
备份地址： https://github.com/233boy/v2ray/fork
安装方法，确保你已经 Fork 了脚本，将 233boy 修改成你的 Github 用户名

git clone https://github.com/233boy/v2ray
cd v2ray
chmod +x install.sh
./install.sh local
如果提示 git 命令不可用，那就自己安装咯，不会安装啊？我也不知道啊。哈哈

及时更新脚本
为确保你能愉快使用，请留意使用 v2ray update.sh 命令来更新管理脚本。
脚本难免会有 BUG，所以建议有空就检查一下更新情况。

关注脚本最新动态
本人会在 本站 Telegram 公告频道 推送脚本最新动态相关，如果你使用 Telegram 的话，可以关注一下。
当然啦，你也可以加入 本站 Telegram 群组 来吹水。

资助 V2Ray
如果你觉得 V2Ray 很好用，能解决你的某些问题，请考虑 资助 V2Ray 发展 。

感谢
V2Ray： https://www.v2ray.com/

版权
此脚本使用 GPL v3 协议共享。

分享
如果觉得脚本好用，记得分享给你的其他小伙伴们哦~

其他
请勿违反国家法律法规，否则后果自负！
使用一键脚本并不会害了你，并且会让你节省大量的时间，工具从来都是为了更快的解决问题。
