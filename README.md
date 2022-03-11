# 规范文档

## 项目编号

项目编号，例：`NYPX01`

## 版本管理

电路板版本：
例：`Rev.A1`，其中`A`为主版本号，`1`为

软件版本：
例：`v1.2.3`，参照 [语义化版本号(semver)](http://semver.org/lang/zh-CN/)

### 软件发布

在git仓库中添加tag，并编写更新日志（参照 [如何维护更新日志](http://keepachangelog.com/zh-CN/0.3.0/)）。

### 硬件打样

将生产文件放到PCB仓库的`produce`目录下，编写更新日志，在git仓库中添加tag。如：

```
└── nypx06-pcb
    ├── produce
    │   ├── nypx06-pcb-rev.a0
    │   │   ├── nypx06-B_Cu.gbl
    │   │   ├── nypx06-B_Mask.gbs
    │   │   ├── nypx06-B_Paste.gbp
    │   │   ├── nypx06-B_SilkS.gbo
    │   │   ├── nypx06-Edge_Cuts.gm1
    │   │   ├── nypx06-F_Cu.gtl
    │   │   ├── nypx06-F_Mask.gts
    │   │   ├── nypx06-F_Paste.gtp
    │   │   ├── nypx06-F_SilkS.gto
    │   │   ├── nypx06-NPTH.drl
    │   │   ├── nypx06-NPTH-drl_map.gbr
    │   │   ├── nypx06-PTH.drl
    │   │   └── nypx06-PTH-drl_map.gbr
    │   └── nypx06-pcb-rev.a1
    │       ├── nypx06-B_Cu.gbl
    │       ├── nypx06-B_Mask.gbs
    │       ├── nypx06-B_Paste.gbp
    │       ├── nypx06-B_SilkS.gbo
    │       ├── nypx06-Edge_Cuts.gm1
    │       ├── nypx06-F_Cu.gtl
    │       ├── nypx06-F_Mask.gts
    │       ├── nypx06-F_Paste.gtp
    │       ├── nypx06-F_SilkS.gto
    │       ├── nypx06-NPTH.drl
    │       ├── nypx06-NPTH-drl_map.gbr
    │       ├── nypx06-PTH.drl
    │       └── nypx06-PTH-drl_map.gb
```

## 术语表

- 固件：fw
- 文档： docs
- PC端程序： pc
- 说明书： um
- 参考资料： refer
- 生产： produce

## 电路设计规范

### 原理图

值标注时，应带物理符号, 而不是例如电容生产中用的"104"(0.1u)这种习惯性表记方式，例如：

- 电阻值例：0r，200r，2K
- 电容值例: 0.1u，1n，10u

元件有特殊要求，但原理图符号无法体现时，应直接在值里标注，如：

- `22u/50V`
- `22u/Polyster`

PCB布局、制造工艺上有要求时，添加适当的注释，如：

- 线路的阻抗、电流要求
- 元件摆放要求

### PCB

丝印标注：

* LOGO
* 项目代号、板子名称
* 版本号
* PCB修改时间

### 接口定义

SWD调试接口：

```
0: VCC
1: GND
2: SWCLK
3: SWDIO
4: RESET
```

调试串口：

```
0: VCC
1: GND
2: TXD
3: RXD
```

### 线材颜色

专用颜色，不应使用这两种颜色线材作为其他功能：

- 黑：GND
- 红：VCC

参考颜色，仅作参考：

- 绿：TXD
- 白：RXD
- 黄：DATA
- 蓝：CLK
