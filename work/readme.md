[![license](https://img.shields.io/github/license/anncwb/vue-vben-admin.svg)](LICENSE)

<h1>一站式飞行训练运营系统</h1>

**中文**

## 简介

一站式训练运营系统使用了最新的`vue3`,`vite5`,`TypeScript`等主流技术开发。

## 特性

- **最新技术栈**：使用 Vue3/vite5 等前端前沿技术开发
- **TypeScript**: 应用程序级 JavaScript 的语言
- **主题**：可配置的主题
- **国际化**：内置完善的国际化方案
- **Mock 数据** 内置 Mock 数据方案
- **权限** 内置完善的动态路由权限生成方案
- **组件** 二次封装了多个常用的组件

## 安装使用

### 注意：

- <font size=4 color=red>请确保你的 Node.js 版本 >= 18.12.0</font>
- <font size=4 color=red>请确保你的 pnpm 版本 >= 8.10.0</font>

- 获取项目代码

```bash
git clone https://gitee.com/chruit/tsms-fe.git
```

- 安装依赖

```bash
cd tsms-fe

pnpm install

```

- 运行

```bash
pnpm serve

测试账号: vben/123456
```

- 打包

```bash
pnpm build
```

## 项目结构

```json
--tsms-fe
  --internal            // 项目配置文件夹
    --ts-confg          // ts相关的配置文件夹
    --vite-config       // vite框架配置文件夹
    --stylelint-config  // 样式规范配置文件夹
    --eslint-config     // eslint规范配置文件夹
  --packages      // 项目包
    --hooks   // 项目全局通用hooks，配置路径："@vben/hooks": "workspace:*"
    --types       // 全局通用的ts工具类
  --src
    --api         // 存放接口的文件夹
    --assets      // 存放静态文件，例如：svg、img、icon
    --components  // 通用组件文件夹
    --design      // 通用样式文件夹
    --directives  // 全局通用指令
    --enums       // 全局枚举数据
    --hooks       // 通用hooks文件夹
    --layouts     // 基础布局文件夹
    --locales     // 国际化i18n文件夹
      --langs     // 翻译文本
    --logics      // 通用处理函数
    --router      // 路由文件夹
    --settings       // 全局配置参数
    --store       // pinia文件夹
    --utils       // 通用的轮子函数文件夹
    --views       // 存放项目page的文件夹
    --index.ts    // 入口文件
    --App.vue     // 入口
  --types         // 通用类型接口文件夹
  --env.**        // 项目全局运行配置
  --vite.config.ts
  --package.json
```

- 项目中看到`@vben/***`类似的引入方式，可以在`package.json`中查看配置，例如：`"@vben/hooks": "workspace:*"`，该配置表示在当前的项目路径下找到第一个匹配`hooks`文件夹来引入。
- 项目中的路由和菜单是分开维护的，会根据项目中的路由文件形成右侧菜单，但路由会被拍平成二级路由。

## 代码commit描述格式

<font size=4>`<type>(<scope>): <subject>`</font>

### type(必须)

1. feat：新功能（feature）。
2. fix/to：修复bug，可以是QA发现的BUG，也可以是研发自己发现的BUG。
   - fix：产生diff并自动修复此问题。适合于一次提交直接修复问题
   - to：只产生diff不自动修复此问题。适合于多次提交。最终修复问题提交时使用fix。
3. docs：文档（documentation）。
4. style：格式（不影响代码运行的变动）。
5. refactor：重构（即不是新增功能，也不是修改bug的代码变动）。
6. perf：优化相关，比如提升性能、体验。
7. test：增加测试。
8. chore：构建过程或辅助工具的变动。
9. revert：回滚到上一个版本。
10. merge：代码合并。
11. sync：同步主线或分支的Bug。
12. wip: 开发中。

### scope（可选）代码改动影响的范围

### subject(必须)

subject是commit目的的简短描述，不超过50个字符。建议使用中文。