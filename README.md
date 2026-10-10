# InkPetal AI

一个放在 Obsidian 里的 AI 学习助手，专门帮助 Linguistics 学生：

- 学习怎么给老师写清楚、礼貌的邮件
- 从基础开始理解抽象的语言学课程
- 根据考试日期和薄弱点安排学习计划
- 阅读课程 Slides、Reading、PDF、图片和 Obsidian 笔记

AI 默认被设置为一位经验丰富的 Linguistics 教授。它会先判断你卡在哪里，再通过解释、例子和小问题一步步教你，而不是只丢给你一个答案。

## 开始前要准备什么

你需要：

1. 一台安装了 [Obsidian](https://obsidian.md/download) 的电脑
2. 一个 OpenAI API Key
3. 少量 OpenAI API 余额

> [!IMPORTANT]
> ChatGPT Plus 和 OpenAI API 是两个分开计费的产品。即使已经订阅 ChatGPT Plus，也仍然需要单独开通 API 余额。

## 最简单的安装方法

这个方法适合第一次使用 Obsidian 插件的人。

### 第一步：下载完整示例库

点击下载：

**[InkPetal-Demo.zip](https://github.com/xinxincodingc/ink-petal-ai/releases/latest/download/InkPetal-Demo.zip)**

下载后双击解压，会得到一个叫 `InkPetal-Demo` 的文件夹。

### 第二步：用 Obsidian 打开

1. 打开 Obsidian。
2. 点击 **Open folder as vault**，中文版可能显示为 **打开本地库**。
3. 选择刚才解压得到的 `InkPetal-Demo` 文件夹。
4. 如果出现是否信任作者的提示，确认这是从本仓库下载的文件后再继续。

### 第三步：启用插件

1. 点击 Obsidian 左下角的齿轮，打开 **Settings / 设置**。
2. 点击 **Community plugins / 第三方插件**。
3. 点击 **Turn on community plugins / 开启第三方插件**。
4. 在已安装插件中找到 **InkPetal AI**。
5. 打开它右侧的开关。

启用成功后，Obsidian 左侧会出现一个花朵图标。

## 配置 ChatGPT

### 第一步：准备 API 余额

1. 打开 [OpenAI API Billing](https://platform.openai.com/account/billing)。
2. 登录自己的 OpenAI 账号。
3. 根据页面提示添加少量 API 余额。
4. 建议同时设置较低的使用限额，避免意外产生过多费用。

余额更新有时需要等待几分钟。

### 第二步：创建 API Key

1. 打开 [OpenAI API Keys](https://platform.openai.com/api-keys)。
2. 点击 **Create new secret key**。
3. 给它起一个容易识别的名字，例如 `InkPetal Obsidian`。
4. 创建后立即复制以 `sk-` 开头的 Key。这个 Key 通常只完整显示一次。

不要把 API Key 发给任何人，也不要放进截图、聊天记录或公开笔记。

### 第三步：填进 Obsidian

1. 回到 Obsidian。
2. 打开 **Settings / 设置**。
3. 在左侧找到 **InkPetal AI**。
4. 将刚才复制的内容粘贴到 **OpenAI API Key**。
5. 其他选项第一次使用时不用修改：

| 选项 | 保持这个内容 |
| --- | --- |
| API 地址 | `https://api.openai.com/v1` |
| 模型 | `gpt-4.1-mini` |
| 回复语言 | `跟随我的语言` |

设置会自动保存，不需要再点击保存按钮。

### 第四步：测试是否连接成功

1. 点击左侧花朵图标。
2. 选择 **课程**。
3. 输入：

```text
我在学习 Linguistics。请用一个简单例子解释 morphology 和 syntax 的区别，最后问我一道小题。
```

4. 按 Enter 或点击右下角的发送按钮。

能够收到解释和小题，就代表配置成功。

## 日常怎么使用

### 邮件：学习给老师写邮件

选择 **邮件**，尽量告诉 AI：

- 写给谁
- 为什么写
- 希望对方做什么
- 是否有截止日期
- 使用中文还是英文
- 有没有已经写好的草稿

例如：

```text
我要给 Syntax 课的老师写英文邮件。
我没理解 Assignment 2 的 constituency test 要做到什么程度。
我想预约周三的 office hour，也想先确认需要准备什么。
请先教我搭结构，不要马上替我写完整邮件。
```

### 课程：从基础理解抽象概念

不用假装自己已经懂很多，可以直接说明基础不好：

```text
我在学 formal semantics，但逻辑基础很弱。
我现在最不懂的是 generalized quantifier。
请先判断我缺少哪些前置知识，然后一次只教一个小目标。
```

AI 会先定位问题，再按照“直觉解释、语言例子、正式定义、小练习”的顺序教学。

### 计划：安排复习

选择 **计划**，告诉 AI：

- 考试或作业日期
- 每周可以学习多久
- 已经学会什么
- 最薄弱的部分
- 有多少份 Slides、Reading 或习题

例如：

```text
四周后考 Phonology，每周可以学习 5 小时。
我会 IPA，但 feature 和 rule ordering 不稳。
材料有 8 讲 Slides 和 4 份 problem set。
请先安排未来 7 天，并写清每次任务的时间和完成标准。
```

### 精读：阅读 Slides 和 Reading

1. 先把 PDF、图片或 Markdown 笔记放进当前 Obsidian 库。
2. 打开 InkPetal AI，选择 **精读**。
3. 点击 **添加材料**。
4. 选择需要阅读的文件。
5. 输入你希望它怎么教。

例如：

```text
先告诉我这份 Reading 的研究问题、核心主张和证据。
遇到我可能缺少的前置知识时先停下来解释。
每读完一部分问我一道检查题，不要一次讲完整篇。
```

目前支持 Markdown、TXT、PDF、PNG、JPG、JPEG 和 WEBP。PPTX 请先导出为 PDF，单个文件不要超过 20 MB。

### 使用正在看的笔记

输入框上方有一个 **当前笔记** 按钮：

- 按钮亮起：AI 会一起阅读当前打开的 Markdown 笔记
- 按钮关闭：AI 只根据聊天内容和手动添加的材料回答

右上角的下载图标可以把整段对话保存到 `学习记录` 文件夹。

## 常见问题

### 提示 API Key 错误或 401

- 检查复制时有没有多出空格。
- 回到 OpenAI API Keys 页面重新创建一个 Key。
- 不要使用 ChatGPT 登录密码代替 API Key。

### 提示 insufficient_quota、credit balance 或 429

- 打开 [OpenAI API Billing](https://platform.openai.com/account/billing) 检查余额。
- 没有余额时需要添加 API credits。
- 刚充值后等待几分钟再试。

### 左侧没有花朵图标

打开：

**Settings / 设置 → Community plugins / 第三方插件**

确认 InkPetal AI 右侧的开关已经打开。

### 找不到 InkPetal AI 设置

通常表示插件还没有启用。先到第三方插件页面打开插件，再回到设置列表。

### PDF 无法读取

- 检查文件是否超过 20 MB。
- 扫描版 PDF 可能需要先做 OCR。
- 可以只截取需要学习的页面并作为图片添加。

### 回答里说无法确认页码或内容

这是正常的保护机制。InkPetal AI 不会假装读到了模糊或缺失的内容，也不会编造页码和文献。

## 安装到自己已有的 Obsidian 库

不想使用示例库时，可以手动安装：

1. 下载 **[InkPetal-AI-plugin.zip](https://github.com/xinxincodingc/ink-petal-ai/releases/latest/download/InkPetal-AI-plugin.zip)**。
2. 解压后会得到 `ink-petal-ai` 文件夹。
3. 在 Obsidian 中打开 **Settings → Community plugins**。
4. 点击插件页面上的文件夹图标，打开 Obsidian 的插件目录。
5. 将整个 `ink-petal-ai` 文件夹放进去。
6. 回到 Obsidian，点击刷新图标。
7. 找到 InkPetal AI 并打开开关。

插件文件夹中应该有：

```text
ink-petal-ai/
├── main.js
├── manifest.json
└── styles.css
```

## 隐私和费用

- API Key 保存在当前 Obsidian 库的插件数据中，不会提交到本 GitHub 仓库。
- 发送消息时，问题和所选材料会直接发送给设置的 OpenAI API。
- 不要上传包含密码、身份证件、医疗记录或其他敏感信息的笔记。
- API 会按照 OpenAI 的实际用量计费。可以在 OpenAI 平台设置较低的使用限额。

## 给开发者

```bash
git clone https://github.com/xinxincodingc/ink-petal-ai.git
cd ink-petal-ai
npm install
npm run build
```

构建产物为 `main.js`。

## License

[MIT](LICENSE)
