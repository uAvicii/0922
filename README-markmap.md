# Markmap思维导图生成器

这是一个使用markmap库生成交互式思维导图的完整示例项目。

## 🚀 快速开始

### 1. 安装依赖
```bash
npm install
```

### 2. 运行示例
```bash
# 运行内置示例
node markmap.js

# 或运行详细示例
node markmap-example.js

# 从Markdown文件生成
node markmap.js your-file.md output-name
```

## 📖 使用方法

### 方法1: 使用类实例
```javascript
import MarkmapGenerator from './markmap.js';

const generator = new MarkmapGenerator();

// 从文本生成
await generator.generateMindMap(markdownText, 'filename');

// 从文件生成  
await generator.generateFromFile('path/to/file.md', 'output-name');
```

### 方法2: 使用便捷函数
```javascript
import { generateMindMapFromText, generateMindMapFromFile } from './markmap.js';

// 从文本生成
await generateMindMapFromText(markdownText, 'filename');

// 从文件生成
await generateMindMapFromFile('path/to/file.md', 'output-name');
```

## 📝 Markdown格式要求

支持标准的Markdown语法：

```markdown
# 主标题

## 二级标题
### 三级标题
- 列表项1
- 列表项2
  - 嵌套列表
  - 更多内容

## 另一个分支
### 子分支
- 内容A
- 内容B
```

## 🎯 功能特点

- ✅ 支持从Markdown文本直接生成
- ✅ 支持从Markdown文件生成  
- ✅ 生成交互式HTML思维导图
- ✅ 自动创建输出目录
- ✅ 支持命令行使用
- ✅ 完整的错误处理
- ✅ 中文支持

## 📂 输出文件

生成的HTML文件保存在 `./markmap-output/` 目录下，可以直接在浏览器中打开查看。

## 🔧 自定义配置

你可以修改 `MarkmapGenerator` 类来自定义：
- 输出目录
- HTML模板
- 样式配置
- 功能扩展

## 📋 依赖包

- `markmap-lib`: 核心转换库
- `markmap-view`: 视图渲染库  
- `markmap-cli`: 命令行工具

## 💡 使用技巧

1. **结构化内容**: 使用清晰的标题层级
2. **适度嵌套**: 避免层级过深
3. **简洁文本**: 每个节点保持简洁
4. **逻辑分组**: 相关内容归类整理

## 🐛 常见问题

**Q: 生成的HTML文件为空？**  
A: 检查Markdown格式是否正确，确保有标题结构

**Q: 中文显示异常？**  
A: 确保文件编码为UTF-8

**Q: 无法安装依赖？**  
A: 尝试使用 `npm install --legacy-peer-deps`

## 📞 支持

如有问题，请检查：
1. Node.js版本 >= 14
2. 依赖是否正确安装
3. Markdown语法是否规范
