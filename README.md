# 💕 测测你到底有多喜欢他

一个基于心理学五维度分析的恋爱测试网站。

## 功能特点

- 21道专业测试题目
- 五维度心理分析（潜意识关注、生理反应、情绪波动、排他性、未来投射）
- 移动端完美适配
- LeanCloud 点击统计

## 部署到 Vercel

### 方法一：直接部署（推荐）

1. Fork 或上传此项目到你的 GitHub
2. 在 Vercel 中导入该仓库
3. 直接部署即可

### 方法二：如果遇到 404 错误

确保项目结构如下：
```
├── public/
│   └── index.html
├── vercel.json
├── package.json
└── README.md
```

## 配置 LeanCloud 统计

1. 登录 [LeanCloud](https://console.leancloud.cn/)
2. 创建应用，获取 App ID、App Key 和服务器地址
3. 编辑 `public/index.html`，找到以下代码并替换：

```javascript
const LC_APP_ID = 'YOUR_APP_ID';  // 替换为你的 App ID
const LC_APP_KEY = 'YOUR_APP_KEY'; // 替换为你的 App Key
const LC_SERVER_URL = 'https://your-domain.lc-cn-n1-shared.com'; // 替换为你的服务器地址
```

4. 在 LeanCloud 控制台会自动创建 `TestClick` 表，记录以下字段：
   - `testId`: 测试标识
   - `testName`: 测试名称
   - `count`: 点击次数
   - `lastClickTime`: 最后点击时间

## 查看统计数据

在 LeanCloud 控制台 → 数据存储 → 结构化数据 → TestClick 表中查看。

可以按 `count` 降序排列，查看最受欢迎的测试。

## 技术栈

- 原生 HTML/CSS/JavaScript
- LeanCloud 数据存储
- Vercel 静态部署
