# Vue-ElementBase

Vue-ElementBase 的前端部分,集成了 ESlint、Prettier、Vuetur 插件

语法检查采用`vue/recommended`、`eslint:recommended`、`google`、`prettier`，保存时自动检查语法问题并提供自动更正，运行时 warning 会被视为 error 无法通过编译

# 安装使用

## 项目部分安装

git clone 本项目即可，已包含 node_modules

## vsCode 部分安装

### 插件安装

需要安装几个插件，将项目主目录下 vscode 文件夹的内容复制到 `C:\Users\用户名\.vscode` 目录下

### 配置

打开 vscode，依次点击左上角 file->preferences->settings , 搜索`git.path` ，点击 `edit in settings.json`
将如下配置复制进

```Javascript
{
    "editor.formatOnType": true,
    "editor.formatOnSave": true,
    "editor.wordWrap": "on",
    "editor.minimap.enabled": false,
    "files.autoSave": "afterDelay",
    "eslint.validate": [
        "javascript",
        "javascriptreact",
        {
            "language": "vue",
            "autoFix": true
        }
    ],
    "eslint.autoFixOnSave": true,
      "vetur.format.defaultFormatter.html": "prettyhtml",
      "vetur.format.defaultFormatter.css": "prettier",
      "vetur.format.defaultFormatter.postcss": "prettier",
      "vetur.format.defaultFormatter.scss": "prettier",
      "vetur.format.defaultFormatter.less": "prettier",
      "vetur.format.defaultFormatter.stylus": "stylus-supremacy",
      "vetur.format.defaultFormatter.js": "prettier",
      "vetur.format.defaultFormatter.ts": "prettier",
      "editor.codeActionsOnSave": {
        "source.fixAll": true
    },
    "git.autofetch": true,
    "terminal.integrated.rendererType": "dom",
    "[vue]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },

}
```

## 使用

`npm run serve`
