# Static 静态资源目录

## 📚 题库文件

### questions_3000.json
- **用途**: 内置题库（3000题）
- **加载方式**: 通过 `/static/questions_3000.json` URL 动态加载
- **特点**: 不打包到 Vue 代码中，可以在 GitHub Pages 上直接替换

## 🔄 题库加载逻辑

系统会按以下优先级加载题库：

1. **优先**: `/data/questions.json` - 动态题库（如果存在）
2. **备用**: `/static/questions_3000.json` - 内置题库（3000题）

### 动态题库优先
- 如果 `/data/questions.json` 存在且可访问，系统将**仅使用**动态题库
- 动态题库可以通过服务器动态生成和更新

### 内置题库备用
- 如果动态题库不存在或加载失败，系统将使用内置的 3000 题题库
- 内置题库存放在 `public/static/` 目录，不会打包到 JS 代码中

## 📝 如何替换题库

### 在 GitHub Pages 上替换题库

1. 直接替换 `public/static/questions_3000.json` 文件
2. 重新部署或直接在 Pages 仓库中替换该文件
3. 无需重新构建 Vue 应用

### 题库格式

```json
{
  "elementary": [
    {
      "expression": "x + 3 = 7",
      "answers": { "x": 4 },
      "level": 1,
      "hint": ""
    }
  ],
  "intermediate": [...],
  "advanced": [...]
}
```

## 🎯 优势

- ✅ 题库不打包到 JS 代码中，减小构建体积
- ✅ 可以在部署后直接替换题库文件
- ✅ 支持动态题库优先，灵活扩展
- ✅ 内置题库作为备用，保证可用性
