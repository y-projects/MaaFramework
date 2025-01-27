<div align="center">

<img alt="LOGO" src="https://cdn.jsdelivr.net/gh/MaaAssistantArknights/design@main/logo/maa-logo_512x512.png" width="256" height="256" />

# MAA Framework

<br>

一款软件自动化测试框架，基于图像识别技术，模拟点击控制，一键完成设定好的测试任务

</div>

<br>

## 拆库及解耦

- [MaaFramework](https://github.com/MaaAssistantArknights/MaaFramework)  
  技术栈：C++ / Vision  
  通用 图像识别 + 控制 框架，~~Json 解释器~~，不涉及具体待测软件业务逻辑

- [MaaCommon](https://github.com/MaaAssistantArknights/MaaCommon)  
  技术栈：C# / RPC / ......  
  平台相关上层业务，~~也就是现在每个 UI 都写了一遍的逻辑~~  
  Http / WS APIs, 模拟器控制、端口查找、定时任务、版本更新、资源下载……

- MaaCore  
  技术栈：C++ / Python / Vision  
  待测软件业务逻辑，图像识别 + 控制 部分

## 目标期望

如果适配新软件，Framework 一行不改，Common 只进行配置文件相关修改

## How to build

1. Download pre-built third-party libraries.
  
  ```bash
  python maadeps-download.py
  ```

2. Build with MAA.sln or cmake.
