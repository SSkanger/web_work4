# 待办事项应用 

一个采用工程化方式开发的待办事项应用。

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

### 启动程序

```bash
npm run dev
```

访问 http://localhost:8080


## 许可证

MIT License