# 规范文档
沙包工作室项目管理相关规范

## 版本号规范
参照 [语义化版本号](http://semver.org/lang/zh-CN/)

## 源代码管理
使用git作为版本管理工具
私有项目使用[码云作为托管平台](https://git.oschina.net/organizations/shabao-studio)
开源项目使用[Github作为托管平台](https://github.com/shabao-studio/)

### 版本库命名

```
项目名-版本库文件内容
```

#### 项目名 
由小写字母/数字/下划线构成,如`osu_keyobard_v3`

#### 版本库文件内容
如版本库中的文件为项目`osu_keyobard_v3`的固件,版本库命名为 `osu_keyobard_v3-fw`

```
对照表
固件 - fw
文档 - doc
PC端程序 - pc
说明书 - um
参考手册 - rm
数据手册 - ds
```

## 更新日志规范
参照 [如何维护更新日志](http://keepachangelog.com/zh-CN/0.3.0/)

## 文档规范
将文档等同于源代码进行管理, 必要时可使用 [Read The Docs](http://docs.readthedocs.io) 生成html或pdf.

### 使用Markdown的场合
简单的文档, 如维护记录, 更新日志等.

### 使用reStructuredText
较复杂文档,如规范手册/库参考手册等使用rst格式书写文档.

