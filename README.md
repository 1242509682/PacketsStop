## 插件说明
```
作者：羽学  
源码地址：[github]https://github.com/1242509682/PacketsStop/   
插件源码来于少司命的游客限制插件，将其处理数据包方法做成了一个独立的功能插件  
这是一个Tshock服务器插件主要用于：  
- 使用指令开启拦截玩家数据包  
- 使用前必须先给default组一个权限【免拦截】  
- 接着通过修改配置文件添加数据包名使用/reload重载  
- 输入【/拦截 add 名字】将玩家分配到一个新建的【LJ组】  
- 封锁了大部分可用权限并对其数据包拦截。  
```

## 插件版本
```
更新日志  
v2.0.0  
修复数据包拦截插件的GetPacket逻辑：原对配置文件内的数据包名以外的全部拦截问题已修复  

v1.0.0  
1.将少司命游客限制源码提取作为独立方法
2.通过Config自定义拦截的数据包，可使用Reload重载
3.加入了2个权限与预设的配置文件实例
4.将开启功能绑定在了add与del子命令上
5.加入了个add子命令，可通过添加玩家名字将其分配到一个自动创建的LJ组
6.加入了个del子命令，可通过移除玩家名字将其分配回default组

```
## 命令
```
/拦截 -开启功能
/拦截 add 玩家名 -添加拦截指定玩家并分配到一个自动创建的LJ组
/拦截 del 玩家名 -移除拦截指定玩家并分配回default组
```
## 权限
```
拦截  
免拦截  
```
## 权限示例
```
/group addperm default 免拦截

```

## 配置示例
```(json)
{
  "数据包名可查看": "https://github.com/Pryaxis/TSAPI/blob/general-devel/TerrariaServerAPI/TerrariaApi.Server/PacketTypes.cs",
  "插件指令与权限名": "拦截",
  "第一次使用输这个": "/group addperm default 免拦截",
  "拦截的数据包名": [
    "ConnectRequest",
    "Disconnect",
    "ContinueConnecting",
    "ContinueConnecting2",
    "PlayerInfo",
    "PlayerSlot",
    "TileGetSection",
    "PlayerSpawn",
    "ProjectileNew",
    "ProjectileDestroy",
    "SyncProjectileTrackers"
  ]
}
```
