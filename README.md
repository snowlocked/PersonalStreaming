# PersonalStreaming

个人流媒体库，使用 [auto_bangumi](https://github.com/EstrellaXD/Auto_Bangumi) + [qbittorrent](https://github.com/qbittorrent/qBittorrent) + [jellyfin](https://github.com/jellyfin/jellyfin)实现订阅追番+自动下载+本地流媒体播放

## 安装和配置

> 前置使用条件  
安装 docker python 及 docker-compose

```bash
# 拉取项目
git clone https://github.com/snowlocked/PersonalStreaming.git ${YourPath}

cd ${YourPath} && cp .env.example .env
# 修改你的环境变量
vi .env

# 如果需要修改python版本则需要再改改yml文件
# vi docker-compose.yml

docker-compose up -d
```

执行命令后

访问 
- Jellyfin: http://${YOUR_HOST}:8096
- qb: http://${YOUR_HOST}:8989
- ab: :http://${YOUR_HOST}:7892

其中qb和ab的账号均为admin，密码为adminadmin

其他更多配置参考 
- [auto_bangumi](https://github.com/EstrellaXD/Auto_Bangumi)
- [qbittorrent](https://github.com/qbittorrent/qBittorrent)
- [jellyfin](https://github.com/jellyfin/jellyfin)

## 使用

1. 访问 jellyfin，添加用户，然后登录进入控制台的媒体库选项添加媒体库
2. 访问 [蜜柑计划](https://mikanani.me/) (需要有某些工具访问)，注册账号，进入账号设置，把高级订阅打开
3. 订阅番剧：如图根据你实际需要选择番剧订阅
![img](https://github.com/snowlocked/PersonalStreaming/assets/19562649/5fb2b2ef-f357-4a16-afca-02bea7d5531d)
4. 获取你的token：点击这里跳转url
![img](https://github.com/snowlocked/PersonalStreaming/assets/19562649/4caed101-a877-436a-ae26-2752206011f8)
![img](https://github.com/snowlocked/PersonalStreaming/assets/19562649/b1c4b9ba-199f-47a8-a068-00ed7677c270)
记下你的token
5. 访问 ab，使用默认账号密码登录，进入设置，订阅配置，把你的token复制进来即可，其他配置可根据你实际需求配置
![img](https://github.com/snowlocked/PersonalStreaming/assets/19562649/7f1ab22b-7c83-4a6c-bf84-ae7ed0b834ea)
6. 访问qb查看下载进度。
7. 下载完后到你的jellyfin即可观看

## reference
- [auto_bangumi](https://github.com/EstrellaXD/Auto_Bangumi)
- [qbittorrent](https://github.com/qbittorrent/qBittorrent)
- [jellyfin](https://github.com/jellyfin/jellyfin)
- [蜜柑计划](https://mikanani.me/)
