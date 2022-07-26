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

#### 2021-12-13 16：18：00

    1. 更新滚动条组件自身内部监听页面宽度，小窗口（移动端）隐藏自定义滚动条

#### 2021-12-12 22：18：00

    1. 规范组件属性名称
    2. 调整页面宽度布局

#### 2021-12-11 13：04：00

    1. 规范了组件名称
    2. 修改组件展示页面类型，每个组件单独显示
    3. 响应式布局优化

#### 2021-12-09 17：23：00

    1. 更新滚动条监听元素高及页面窗口尺寸变化，自动更新滚动条（解决初始化滚动条不准确问题）
    2. 更新自定义渲染组件元素逻辑（全局模态框，提示框）
    3. vue3展示md文件升级vue-loader版本
    4. vue2版本内容全部改为vue3

#### 2021-12-06 17：55：00

    1. 更改代码编写vue3方式
    - 在vue2模块功能基础上进行vue3编码

#### 2022-05-12 10：00：00

    1. 增加长文本查询

#### 2022-05-12 16：00：00

    1. 重置高亮优化
    2. 加载动画优化

#### 2022-05-27 16：00：00

    1. 目录显示层级控制
    2. 本地纯文本关键词查询
    3. 解决table中空格和纯文本中空格问题
    4. 解决循环递归加高亮标签return(同段多句中关键词bug ，同句)

#### 2022-05-28 16：00：00

    1. 等待动画位置调整
    2. 背景色设置配置项
    3. 抽离长文本组件30%

#### 2022-05-29 16：00：00

    1. 优化上下切换
    2. 抽离长文本组件90%

#### 2022-05-30 16：00：00

    1. 长文本组件变量命名优化
    2. 读取业务文本和其他文本判断
    3. 其他文本根据是否存在标签判断，纯文本还是有格式的
    4. 纯文本以回车分割，包裹<p>标签展示（便于同段）
    5. 读取本地html格式长文本说明文档
    6. 阻止表格初始移除报错
    7. 目录层级负数处理
    8. 功能介绍本地文件初始展示
    9. 增加层级和截取可配置
    10. 添加演示文件下载
    11. 滚动条样式修改

#### 2022-05-30 16：00：00

    1. 点击目录，长文本定位标题并且高亮
    2. 修改左右箭头切换报错，判断是不是默认首次定位第一个
    3. 表格中按td分割段落查询
    4. 增加目录默认层级全部展开
    5. 增加目录同时展开多个或一个
    6. 增加手动输入数据网址展示

#### 2022-06-15 11：00：00

    1. 更新字体图标
    2. 封装鼠标拖拽到common.js中
    3. 配置页面获取数据类型

#### 2022-07-06 11：00：00

    1. 增加模拟数据数字范围

#### 2022-07-11 11：00：00

    1. 增加模拟数据布局拖拽改变尺寸

#### 2022-07-12 15：12：00

    1. 增加技术问题记录查询页面

#### 2022-07-12 18：30：00

    1. 解决匹配一个词时，点击左侧匹配定位，无灰色高亮范围bug
    2. 开发五子棋功能

#### 2022-07-13 18：30：00

    1. 五子棋功能完成（边界处理，相对复杂）

#### 2022-07-14 15：51：00

    1. todoList布局搭建

#### 2022-07-15 15：51：00

    1. 五子棋增加即使和胜利次数

#### 2022-07-18 15：51：00

    1. 增加任务列表

#### 2022-07-18 15：51：00

    1. 任务状态改变时，相关列表全部重置收起状态
    2. 添加一键删除全部任务列表功能

#### 2022-07-20 15：51：00

    1. 使用yarn add mitt监听事件总线（解决编辑任务事件触发）
    2. main.js => app.config.globalProperties.$bus = new mitt()
    3. 组件中监听onMounted生命周期中监听editTask事件  proxy.$bus.on('editTask', editTask);
        // 使用mitt监听编辑事件
        onMounted(() => {
            proxy.$bus.on('editTask', editTask);
        });
        // 编辑事件触发val传递的参数
        const editTask = (val) => {
            console.log('编辑任务父组件', val);
        };
    4. 组件中触发editTask事件传递参数  proxy.$bus.emit('editTask', data.myEditTack);
    5. 使用pre标签保留文本格式
    6. 增加任务导出功能

#### 2022-07-22 16：35：00

    1. 增加控制页面全屏按键和F11兼容实现效果统一
    2. 追加任务去除重复id任务
    3. 首页样式修改

#### 2022-07-26 16：35：00

    1. 增加导航图标动画

### vue2 版本（之前项目迁移过来的老功能）

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

#### 2021-11-22 10：00：00

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

#### vue3 批量注册组件时

```
app.component(key, components[key].name);
```

- vue3 中批量注册组件时,使用数组循环,key 值是下标,开发环境下可以正常运行，但是 build 时会报错
