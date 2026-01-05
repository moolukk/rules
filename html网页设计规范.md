# HTML 网页设计规范

## 目的
本规范旨在统一项目中 HTML 页面结构、可维护性和可访问性，提升开发效率并保证良好的用户体验。

## 文件命名与存放位置
- 使用 UTF-8 无 BOM 编码。
- 文件扩展名使用小写 `.md`（本规范为文档），页面文件使用 `.html`。
- 将文档放在 docs/ 或设计规范目录下；页面文件放在 `src/` 或 `public/` 下对应模块目录。

## 文档结构与语义化
- 使用语义化标签（header, nav, main, article, section, aside, footer）代替大量 div。
- 页面必须包含 `<!DOCTYPE html>` 声明和正确的 `lang` 属性，例如 `<html lang="zh-CN">`。
- 每个页面应有唯一的 `<title>`，并在 head 中包含必要的 meta（charset, viewport, description）。

## 无障碍（Accessibility）
- 图片必须包含有意义的 `alt` 属性；纯装饰性图片 `alt=""` 并加 `role="presentation"`。
- 表单控件必须有关联的 `<label>` 或 `aria-label`/`aria-labelledby`。
- 交互元素（按钮、链接）应可通过键盘操作并提供明显的焦点样式。

## 响应式与视口
- 在 head 中加入 `<meta name="viewport" content="width=device-width, initial-scale=1">`。
- 使用移动优先的响应式设计（mobile-first）。

## SEO 基础
- 每个页面应包含描述性的 `<meta name="description">`。
- 使用语义化标题（h1~h6），且页面只出现一个 h1。
- 对重要内容使用结构化数据（必要时使用 JSON-LD）。

## 资源引用与路径
- 使用相对或根路径引用资源，避免使用硬编码主机名。
- 静态资源（图片、字体）应放在统一目录并启用缓存策略。

## CSS / JS 分离
- 结构（HTML）与表现（CSS）与行为（JS）分离。
- 尽量将关键 CSS 内联以减少首次绘制时间，将其余样式异步加载或打包。

## 图片与多媒体优化
- 使用现代图片格式（WebP/AVIF）并提供回退格式。
- 根据设备像素比提供不同分辨率的图片（srcset）。

## 国际化与本地化
- 文案应支持国际化，避免在 HTML 中写死语言字符串，使用翻译文件或模板变量。
- 使用正确的 `lang` 属性并在必要时设置 `dir="rtl"`。

## 代码风格与可读性
- 缩进使用两个或四个空格，团队统一即可。
- 保持标签与属性的书写一致，属性值使用双引号。

## 注释与文档
- 在模板/组件中为复杂结构添加简短注释，解释意图而非复述代码。

## 示例模板（基础）
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>页面标题 - 项目名</title>
  <meta name="description" content="页面描述，便于 SEO 和社交分享。">
  <link rel="stylesheet" href="/assets/styles/main.css">
</head>
<body>
  <header>
    <!-- 导航 -->
  </header>
  <main>
    <h1>页面主标题</h1>
    <section>
      <h2>小节标题</h2>
      <p>内容...</p>
    </section>
  </main>
  <footer>
    <!-- 页脚 -->
  </footer>
  <script src="/assets/scripts/main.js" defer></script>
</body>
</html>
```

## 版本与变更记录
- 在文档顶部或单独文件中记录主要变更和版本号，以便追踪规范演进。

---

如需我把文件放到特定目录（例如 `docs/` 或 `website/`）或用特性分支提交，请告诉我目标路径和分支名称。
