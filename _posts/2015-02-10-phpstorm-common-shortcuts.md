---
layout: post
title: PhpStorm常用快捷键
category: 资源
tags: PhpStorm
keywords: PhpStorm
description:
---

## 编辑

    Ctrl + Space : 基本代码完成(任何类的名称, 方法或变量)，注意系统输入法切换的快捷不要冲突了
    Ctrl + Shift + Enter : 智能代码完成
    Ctrl + Alt + Space : 类名及接口的提示
    Ctrl + J : 插入 live templates
    Alt + / : 补全当前文件存在的word
     
    Alt + Insert : 生成代码
    Ctrl + O : 重写（覆盖）基类中的方法
    Ctrl + I : 实现魔术方法
    Ctrl + Alt + T : 给代码添加外围的一些代码
    Ctrl + / : 单行注释的启用和取消
    Ctrl + Shift + / : 块注释的启用和取消
     
    Ctrl + P : 提示当前调用方法的参数信息
    Ctrl + Q : 快速查看描述
    Ctrl + mouse over code : 按住Ctrl键，然后鼠标移动到上面显示信息摘要
    Ctrl + F1 : 在错误或者警告标志上显示说明
    Shift + F1 : 外部文档
    Alt + Q : 上下文信息，如在类的任意地方按此快捷键查看类的定义
     
    Ctrl + W : 递进式选择代码块
    Ctrl + Shift + W : 返回上一次选择的代码块状态
    Shift + End / Home : 选择当前光标位置开始到行末/行首
    Ctrl + Shift + ] / [ : 选择到代码块结束/开始
     
    Ctrl + Alt + L : 重新格式化代码
    Ctrl + Alt + I : 自动缩进
    Tab / Shift + Tab : 缩进所选的行
     
    Ctrl + X or Shift + Delete : 剪切当前行或所选块代码到剪贴板
    Ctrl + C or Ctrl + Insert : 复制当前行或所选块代码到剪贴板
    Ctrl + V or Shift + Insert : 从剪贴板中粘贴
    Ctrl + Shift + V : 剪贴板 可以复制多个文本
    Ctrl + D : 直接复制当前行或所选块
    Ctrl + Y : 删除光标所在行
    Ctrl + Shift + J : 合并行
    Ctrl + Enter : 分割行
    Shift + Enter : 在当前行下方新建行
    Shift + Alt + Enter : 在当前行上方新建行
    Ctrl + Shift + U : 大小写切换
    Ctrl + Delete : 删除到单词末尾
    Ctrl + Backspace : 删除到单词的开始
    Alt + Shift + Top/Bottom : 移动当前行到上一行/下一行
    Alt + 鼠标选区 : 垂直选择代码
     
    Ctrl + NumPad+/- : 折叠/展开代码
    Ctrl + Shift + NumPad+/- : 所有代码的折叠/展开
     
    Ctrl + F4 : 关闭活跃编辑标签
    Shift + Click : 关闭指定的编辑标签
     
    Ctrl + Top/Bottom : 以屏幕为单位滚屏
     
    Ctrl + Shift + C : 复制文件路径

## 搜索/替换

    Ctrl + F : 查找
    F3 : 查找下一个
    Ctrl + F3 : 查找当前光标所在的单词，并依次往下查找下去
    Shift + F3 : 查找当前光标所在的单词，并依次向前查找下去
    Ctrl + R : 替换
    Ctrl + Shift + F : 在路径中查找
    Ctrl + Shift + R : 在路径中替换

## 用法搜索

    Ctrl + F7 : 在当前文件中查找所使用的地方
    Ctrl + Shift + F7 : 在当前文件中高亮光标所在位置的字符
    Alt + F7 : 在当前项目中查找使用的地方
    Ctrl + Alt + F7 : 显示使用的地方（可以显示方法、变量等在哪些地方被使用了）
    Ctrl + Alt + Top/Bottom

## Running

    Alt + Shift + F10 : 选择配置和运行（弹出窗口，选择要运行的项目，运行）
    Alt + Shift + F9 : 选择配置和调试（弹出窗口，选择要调试的项目，调试）
    Shift + F10 : 运行
    Shift + F9 : 调试
    Ctrl + Shift + F10 : Run context configuration from editor
    Ctrl + Shift + X : 运行命令行工具

## 调试

    F8 : 跳过
    F7 : 步入
    Shift + F7 : 智能步入
    Shift + F8 : 跳出
    Alt + F9 : 运行到光标处
    Alt + F8 : 计算表达式
    F9 : 恢复程序运行
    Ctrl + F8 : 切换断点
    Ctrl+Shift+F8 : 查看断点

## 导航

    Alt + Left/Right : 代码编辑窗口的左右切换
    Ctrl + Tab : 标签和工具窗口快速切换
    Ctrl + E : 打开最近编辑过的文件列表
    Ctrl + N : 跳到指定Class
    Ctrl + Shift + N : 跳到指定文件
    Ctrl + Alt + Shift + N : 通过一个字符查找函数位置
     
    F12 : 回到以前的工具窗口
    Esc : 从工具窗口回到编辑器窗口
    Shift + Esc : 隐藏当前或最后一个激活的窗口
    Ctrl + Shift + F4 : 收缩编辑器窗口左边的工具窗口
     
    Ctrl + G : 跳到指定行
    Ctrl + Alt + Left/Right : 切换到前一个或后一个光标所在位置，如果你的快捷键被调整屏幕方向快捷键占用，可以在控制面板->英特尔图形和媒体 关闭快捷键
    Ctrl + Shift + Backspace : 定位到上次编辑的位置
    Ctrl + Left/Right : 以word为单位移动光标
    Alt + Up/Down : 跳到前/后一个函数
    Ctrl + ]/[ : 跳到代码块的结尾或开始
     
    Alt + F1 : 针对当前文件的一些快捷操作
    Ctrl + Alt + F12 : 跳到文件所在位置
     
    Ctrl + B 或 Ctrl + Click 或 F4 : 跳转到声明位置
    Ctrl + Alt + B : 跳转到实现的代码位置
    Ctrl + Shift + I : 打开快速查找定义
    Ctrl + Shift + B : 前往类型声明
    Ctrl + U : 跳转到父类
     
    Ctrl + F12 : 弹出文件结构 （Alt + 7）
    Ctrl + H : 类层级结构
    Ctrl + Shift + H : 方法层级结构
    Ctrl + Alt + H : 方法被调用层级结构
     
    F2/Shift + F2 : 下一个/上一个突出显示错误
     
    Alt + Home : 在导航条中显示
     
    F11 : 添加bookmap 
    Ctrl + F11 : 添加bookmap并设置标记
    Ctrl + Shift + #[0-9] : 快速添加bookmap标记
    Ctrl + #[0-9] : 跳转到指定标记的书签
    Shift + F11 : 管理bookmap

## 重构

    F5 : 复制当前文件到指定目录
    F6 : 移动当前文件到指定目录
    Alt + Delete : 安全删除
    Shift + F6 : 重命名
    Ctrl + Alt + N : 用当前变量的变量值代替当前变量
    Ctrl + Alt + M : 修改方法名称
    Ctrl + Alt + V : 修改变量名称
    Ctrl + Alt + F : Extract Field
    Ctrl + Alt + C : 修改常量名称

## 版本控制

    Alt + BackQuote (`) : 弹出快速操作窗口
    Ctrl + K : 提交项目
    Ctrl + T : 更新项目
    Alt + Shift + C : 查看最近更改

## 常规

    Ctrl + Shift + A : 快速查找到某个操作
    Alt + #[0-9] : 打开响应的工具窗口
    Ctrl + Shift + F12 : 切换最大化编辑器
    Alt + Shift + F : 添加到收藏夹
    Alt + Shift + I    : 检查当前文件错误概要
    Ctrl + BackQuote (`) : 快速切换方案
    Ctrl + Alt + S : 设置
    Alt + Shift + N : 添加一个任务