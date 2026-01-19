# 待办事项应用 (Todo App)

一个现代化的Vue.js待办事项应用，采用工程化开发方式。

## 项目特性

- 🎯 **组件化开发** - 使用Vue.js单文件组件
- 🛠️ **工程化构建** - 基于Webpack的现代化构建流程
- 📏 **代码规范** - 集成ESLint和Prettier
- 🔥 **热重载** - 开发时实时预览修改效果
- 📱 **响应式设计** - 适配不同屏幕尺寸

## 技术栈

- **前端框架**: Vue.js 2.7
- **构建工具**: Webpack 5
- **代码规范**: ESLint + Prettier
- **开发语言**: JavaScript (ES6+)

## 项目结构

```
work6/
├── src/                    # 源代码目录
│   ├── components/         # Vue组件
│   │   ├── TodoItem.vue   # 单个待办项组件
│   │   ├── TodoInput.vue  # 输入框组件
│   │   └── TodoList.vue   # 待办列表组件
│   ├── App.vue            # 根组件
│   └── main.js            # 入口文件
├── public/                # 静态资源
│   └── index.html         # HTML模板
├── dist/                  # 构建输出目录
├── package.json           # 项目配置
├── webpack.config.js      # Webpack配置
├── .eslintrc.js          # ESLint配置
├── .prettierrc           # Prettier配置
└── README.md             # 项目说明
```

## 快速开始

### 安装依赖

```bash
npm install
```

### 开发模式

```bash
npm run dev
```

访问 http://localhost:8080 查看应用

### 构建生产版本

```bash
npm run build
```

### 代码检查

```bash
npm run lint
```

### 代码格式化

```bash
npm run format
```

## 功能说明

### 核心功能

1. **添加待办事项** - 输入文本并点击添加按钮
2. **删除待办事项** - 点击每个事项的删除按钮
3. **清空所有事项** - 一键清空所有待办事项
4. **键盘支持** - 支持回车键快速添加

### 组件设计

- **TodoItem**: 单个待办项展示和操作
- **TodoInput**: 输入框和添加按钮
- **TodoList**: 待办列表容器和清空功能
- **App**: 根组件，管理应用状态

## 开发规范

### 代码风格

- 使用ES6+语法
- 组件名使用PascalCase
- 变量名使用camelCase
- 使用单引号
- 行尾不添加分号

### 组件规范

- 每个组件使用单文件结构
- 组件名使用多单词命名
- 使用props进行数据传递
- 使用emit进行事件通信

## 构建说明

项目使用Webpack进行构建，支持：

- Vue单文件组件编译
- ES6+语法转译
- CSS样式处理
- 代码分割和优化
- 开发服务器热重载

## 浏览器支持

- Chrome (推荐)
- Firefox
- Safari
- Edge

## 许可证

MIT License