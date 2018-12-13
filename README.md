# Streak 1.0

#### 版本说明：

- Toolkit4DNF现在已更名Streak
- 更名重置了版本号，但相对于Toolkit4DNF有较多更新
- 当前版本过期时间为2019-01-04

#### 配置说明：

当前版本允许自定义配置，配置文件为config.json，需要和主程序在同一目录，当该文件不存在的时候会载入默认配置。

目前开放的配置项如表所示：

|    配置项    |  类型  |                说明                |
| :----------: | :----: | :--------------------------------: |
|    Paths     | Array  |              游戏目录              |
| StopService  |  Bool  |   是否开启停止服务功能，默认开启   |
|  BlockLive   |  Bool  |   是否开启禁用直播功能，默认开启   |
| KillProcess  |  Bool  |   是否开启结束进程功能，默认开启   |
|  AutoStart   |  Bool  | 是否在打开程序时自动启动，默认关闭 |
|   Autokeys   | Array  |              连发列表              |
| BlinkHotKey  | String |           Blink的快捷键            |
| EscapeHotKey | String |           Escape的快捷键           |

以下是一个配置示例：

```json
[
    "Paths": [
    	"D:\\DNF",
    	"E:\\DNF"
	],
	"BlockLive": false,
	"AutoStart": true,
	"Autokeys": [
    	["AX", "Ctrl+NumPad1"]
	]
]
```

> 注意：
>
> - 路径中的\需要写为\\\\不然会出现语法错误
> - 建议配置游戏目录，不然每次启动会全盘查找，比较浪费时间
> - 连发的配置，第一项是连发的名字(不需要exe后缀)，第二项是快捷键
> - 快捷键可以配置为功能键+常规键，功能键[Ctrl, Alt, Shift]，常规键[A, B, F1, NumPad1...]，例如："Ctrl+NumPad1"，"Ctrl+Alt+F12"，请注意大小写。

#### 使用说明：

- Start/Stop，开启/关闭[停用服务]、[禁用直播]、[结束进程]三个功能，可通过配置来控制是否启动
- Cleanup，清理无用文件，暂未开放规则配置
- Escape，强制关闭游戏，默认快捷键Ctrl+Alt+E，可通过配置修改
- Blink，隐藏/显示游戏，默认快捷键Ctrl+Alt+B，可通过配置修改
- About，关于