## SubTopH 前端笔记（vue3 版本）

- 记录个人前端开发心得、笔记、问题解决方法等

### 项目地址

- https://subtoph.github.io

### 项目源码

- Gitee 远程仓库
- git remote add origin https://gitee.com/Subtop/personal-notes.git

### 项目部署

- GitHub 远程仓库
- git remote add origin https://github.com/SubtopH/SubtopH.github.io.git

## 更新日志

### vue3 版本

#### 2021-12-09 17：23：00

    1. 更新滚动条监听元素高及页面窗口尺寸变化，自动更新滚动条
    2. 更新自定义渲染组件元素逻辑（全局模态框，提示框）
    3. vue3展示md文件升级vue-loader版本 
    4. vue2版本内容全部改为vue3

#### 2021-12-06 17：55：00

    1. 更改代码编写vue3方式
    - 在vue2模块功能基础上进行vue3编码

### vue2 版本

#### 2021-12-01 16：28：00

    1. 更改引入组件展示文件结构
    2. 修改事件调用弹窗动画

#### 2021-11-28 21：40：00

    1. 添加公共组件模块展示
    - 组件导航
    - 组件实例
    - 查看组件源码

#### 2021-11-24 17：55：00

    1. 更新整体移动端页面布局
    2. 移动端导航折叠
    3. 取消移动端滚动条

#### 2021-11-23 23：12：00

    1. 修改自定义滚动条

#### 2021-11-23 11：52：00

    1. 动态批量加载md文件组件
    2. 把history模式修改为hash模式解决刷新404问题
    3. 增加了页面右上角点击复制网站地址

#### 2021-11-22 10：00:：00

    1. 项目初始化
    2. 主要模块 - 学习笔记 - 个人介绍

### 问题

#### vue3 版本注意问题

- 展示 markdown 文件时"vue-loader": "^16.8.3",版本才可以
- .md 文件中\<font\>控制颜色标签，会报警告 Failed to resolve component: font

#### 判断滚动元素是否到底部

- e.target.scrollTop + e.target.offsetHeight == e.target.scrollHeight

#### 子组件自定义 click 事件时

- 要声明这是自定义事件
- 这样父组件@click 才是自定义，不然会默认原生事件

```
emits: ["click"],
  setup(props, ctx) {
    const Myclick = function () {
      ctx.emit("click", this.type);
    };
    return {
      Myclick,
    };
  },
```
