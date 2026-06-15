# My Tools

简洁高效的在线工具箱，所有工具在浏览器本地运行，无需上传文件到服务器。

## 项目结构

```
tools/
├── index.html                  # 首页 - 工具导航入口
├── README.md                   # 项目说明
└── tools/                      # 所有工具存放目录
    ├── hash-compare/           # 文件 Hash 两两对比工具
    │   └── index.html
    └── color-picker/           # 取色器工具
        └── index.html
```

## 添加新工具

1. 在 `tools/` 目录下创建新文件夹，如 `tools/my-tool/`
2. 在文件夹中创建 `index.html`
3. 在首页 `index.html` 的 `tools` 数组中添加一条记录：

```javascript
{
    name: "工具名称",
    desc: "工具简介描述",
    icon: '<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="..."/>',
    path: "tools/my-tool/index.html",
    color: "from-green-500 to-green-600",
    tags: ["标签1", "标签2"]
}
```

## 工具列表

| 工具 | 说明 |
|------|------|
| [文件 Hash 两两对比](tools/hash-compare/index.html) | 批量上传文件，计算 MD5/SHA-1/SHA-256 哈希值，自动两两对比找出重复文件 |
| [取色器](tools/color-picker/index.html) | 可视化取色，支持 HSL 面板调节、透明度、HEX/RGB/HSL 格式输出、屏幕取色及颜色历史 |
