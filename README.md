# luci-app-tailscale
OpenWrt-luci-app-tailscale
github action build IPK

第一次运行需要进入控制台：tailscale up 启动，根据返回的注册链接绑定设备
如果出现：failed to connect to local tailscaled……这样的报错，执行一下：/etc/init.d/tailscale start，再执行：tailscale up

https://openwrt.org/docs/guide-user/services/vpn/tailscale/start 的调用
因为 tailscale 占用了 config/tailscale 和 init.d/tailscale , 故使用 luci-app-tailscaler 作为插件名称

启动任务
```
    /etc/init.d/tailscaler start 
```
关闭任务
```
    /etc/init.d/tailscaler stop
```



更改应用界面服务到VPN菜单里
