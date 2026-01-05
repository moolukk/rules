---
description: UI 设计规范
alwaysApply: false
---
## 二、排版系统

### 字体栈
```css
font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, 
             "Helvetica Neue", Arial, sans-serif;
```
**原则**：系统原生字体，保证跨平台一致性

### 字号规范
```css
--fs-h1: 32px;        /* 主标题 */
--fs-h2: 18px;        /* 区块标题 */
--fs-body: 15px;      /* 正文、按钮、输入框 */
--fs-label: 14px;     /* Label、提示 */
--fs-code: 13px;      /* 代码、数据 */
```

### 字重规范
```css
--fw-bold: 600;       /* 标题 */
--fw-medium: 500;     /* Label、按钮 */
--fw-normal: 400;     /* 正文 */
```

### Letter Spacing（微调）
```css
h1: -0.5px;           /* 大标题收紧 */
.section-title: -0.3px;
.btn: -0.2px;
```

---

## 三、间距系统

### 基础单位：8px

```css
/* 内边距 */
--p-xs: 8px;
--p-sm: 16px;
--p-md: 20px;
--p-lg: 32px;
--p-xl: 40px;

/* 外边距 */
--m-sm: 8px;
--m-md: 24px;
--m-lg: 48px;
```

### 应用规则
```css
/* 卡片 */
.section {
    padding: 32px;           /* 内部宽松 */
    margin-bottom: 24px;     /* 卡片间距 */
}

/* 表单组 */
.form-group {
    margin-bottom: 20px;     /* 表单项间距 */
}

/* Label */
label {
    margin-bottom: 8px;      /* Label 到输入框 */
}

/* 页面边距 */
body {
    padding: 40px 20px;      /* 顶部宽松，左右适中 */
}
```

---

## 四、圆角系统

### 统一圆角规范
```css
--radius-lg: 12px;    /* 卡片 */
--radius-md: 8px;     /* 按钮、输入框、提示框 */
--radius-sm: 4px;     /* 滚动条 */
```

### 避免
- ❌ 直角（0px）
- ❌ 过圆（16px+）
- ✅ 适中圆角（8-12px）

---

## 五、阴影系统

### 轻量级阴影（Light Shadows）
```css
/* 卡片阴影 - 几乎不可见 */
box-shadow: 0 1px 3px rgba(0, 0, 0, 0.04);

/* 按钮 Hover 阴影 */
box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);

/* Focus 阴影 - 黑色透明 */
box-shadow: 0 0 0 3px rgba(26, 26, 26, 0.08);
```

### 原则
- **静态状态**：阴影极轻（不可察觉）
- **交互状态**：阴影稍重（提供反馈）
- **颜色**：黑色半透明（避免彩色阴影）

---

## 六、组件规范

### 1. 按钮（Button）
```css
.btn {
    padding: 12px 28px;
    background: #1a1a1a;      /* 纯黑背景 */
    color: white;
    border-radius: 8px;
    font-size: 15px;
    font-weight: 500;
    transition: all 0.2s ease;
    letter-spacing: -0.2px;
}

.btn:hover {
    background: #2d2d2d;      /* 变亮 */
    transform: translateY(-1px); /* 微抬升 */
    box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

.btn:active {
    transform: translateY(0);  /* 按下归位 */
}

.btn:disabled {
    background: #d1d1d1;      /* 浅灰 */
    cursor: not-allowed;
    transform: none;
}
```

### 2. 输入框（Input/Select）
```css
input, select {
    padding: 12px 16px;
    border: 1px solid #d1d1d1;
    border-radius: 8px;
    font-size: 15px;
    background: white;
    transition: all 0.2s ease;
}

input:hover, select:hover {
    border-color: #999;        /* Hover 变深 */
}

input:focus, select:focus {
    outline: none;
    border-color: #1a1a1a;     /* Focus 纯黑边框 */
    box-shadow: 0 0 0 3px rgba(26, 26, 26, 0.08);
}
```

### 3. 卡片（Card/Section）
```css
.section {
    background: white;
    border-radius: 12px;
    padding: 32px;
    border: 1px solid #e5e5e5;
    box-shadow: 0 1px 3px rgba(0,0,0,0.04);
}
```

### 4. 标签页（Tabs）
```css
.tab {
    padding: 12px 20px;
    border-bottom: 2px solid transparent;
    color: #6e6e6e;
    transition: all 0.2s ease;
}

.tab:hover {
    color: #1a1a1a;
    background: #fafafa;       /* 轻微背景变化 */
}

.tab.active {
    color: #1a1a1a;
    border-bottom-color: #1a1a1a; /* 底部黑线 */
}
```

### 5. 代码/结果框（Code Box）
```css
.result-box {
    background: #f8f8f8;       /* 浅灰背景 */
    border: 1px solid #e5e5e5;
    border-radius: 8px;
    padding: 20px;
    font-family: 'SF Mono', 'Monaco', monospace; /* 等宽字体 */
    font-size: 13px;
    max-height: 600px;
    overflow-y: auto;
}

/* 滚动条样式 */
.result-box::-webkit-scrollbar {
    width: 8px;
}

.result-box::-webkit-scrollbar-thumb {
    background: #d1d1d1;
    border-radius: 4px;
}
```

### 6. Loading 动画
```css
.spinner {
    border: 2px solid #f0f0f0;      /* 轨道灰 */
    border-top: 2px solid #1a1a1a;  /* 转动黑 */
    border-radius: 50%;
    width: 32px;
    height: 32px;
    animation: spin 0.8s linear infinite;
}
```

### 7. 状态提示
```css
/* 成功 - 低饱和 */
.success {
    background: #f7fafc;
    border: 1px solid #cbd5e0;
    color: #2d3748;
    padding: 16px;
    border-radius: 8px;
}

/* 错误 - 低饱和 */
.error {
    background: #fff5f5;
    border: 1px solid #fed7d7;
    color: #c53030;
    padding: 16px;
    border-radius: 8px;
}
```

---

## 七、动画与过渡

### 统一时长
```css
transition: all 0.2s ease;  /* 通用：200ms */
animation: spin 0.8s linear infinite; /* Loading：800ms */
```

### 微交互
```css
/* 按钮抬升 */
.btn:hover {
    transform: translateY(-1px);
}

/* 按钮按下 */
.btn:active {
    transform: translateY(0);
}

/* 淡入效果 */
@keyframes fadeIn {
    from { opacity: 0; transform: translateY(4px); }
    to { opacity: 1; transform: translateY(0); }
}
```

---

## 八、布局规范

### 容器宽度
```css
.container {
    max-width: 1000px;         /* 不要过宽 */
    margin: 0 auto;
}
```

### 留白原则
- **页面边距**：40px 顶部 + 20px 左右
- **卡片间距**：24px
- **区块内部**：32px 内边距
- **表单项间距**：20px

### 垂直节奏
```css
/* 头部 */
.header {
    margin-bottom: 48px;       /* 大留白 */
}

/* 标题到内容 */
.section-title {
    margin-bottom: 24px;       /* 中等留白 */
}

/* 输入框到按钮 */
button {
    margin-top: 0;             /* 紧凑 */
}
```

---

## 九、响应式原则

### 移动端适配
```css
@media (max-width: 768px) {
    body {
        padding: 20px 16px;    /* 缩小边距 */
    }
    
    .section {
        padding: 24px;         /* 缩小内边距 */
    }
    
    h1 {
        font-size: 28px;       /* 缩小标题 */
    }
}
```

---

## 十、代码模板（快速复用）

### 基础框架
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>产品名称</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
            background: #fafafa;
            color: #1a1a1a;
            line-height: 1.6;
            padding: 40px 20px;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
        }

        .header {
            text-align: center;
            margin-bottom: 48px;
        }

        h1 {
            font-size: 32px;
            font-weight: 600;
            margin-bottom: 8px;
            letter-spacing: -0.5px;
        }

        .subtitle {
            color: #6e6e6e;
            font-size: 15px;
        }

        .section {
            background: white;
            border-radius: 12px;
            padding: 32px;
            margin-bottom: 24px;
            border: 1px solid #e5e5e5;
            box-shadow: 0 1px 3px rgba(0,0,0,0.04);
        }

        .btn {
            padding: 12px 28px;
            background: #1a1a1a;
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 15px;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        .btn:hover {
            background: #2d2d2d;
            transform: translateY(-1px);
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>产品标题</h1>
            <p class="subtitle">Product Subtitle</p>
        </div>

        <div class="section">
            <button class="btn">开始使用</button>
        </div>
    </div>
</body>
</html>
```

---

## 十一、设计检查清单

### ✅ 色彩
- [ ] 使用中性色系（灰、白、黑）
- [ ] 避免紫色和高饱和度颜色
- [ ] 状态色低饱和

### ✅ 圆角
- [ ] 卡片 12px
- [ ] 按钮/输入框 8px
- [ ] 避免直角

### ✅ 阴影
- [ ] 卡片阴影极轻（0.04 透明度）
- [ ] Hover 阴影适中（0.15 透明度）
- [ ] 使用黑色半透明

### ✅ 留白
- [ ] 页面边距充足（40px+）
- [ ] 卡片内边距宽松（32px）
- [ ] 组件间距适中（20-24px）

### ✅ 字体
- [ ] 系统原生字体栈
- [ ] 字号合理（13-32px）
- [ ] 字重克制（400/500/600）

### ✅ 动画
- [ ] 过渡时间统一（0.2s）
- [ ] 微交互自然（抬升/按下）
- [ ] 避免过度动画

---

## 总结

**三个关键词**：
1. **克制**：不滥用颜色、阴影、动画
2. **留白**：充足的空间让内容呼吸
3. **轻量**：轻边框、轻阴影、轻交互

**对比其他风格**：
- ❌ 不是 Material Design（太重）
- ❌ 不是 Ant Design（太复杂）
- ✅ 更像 Linear、Stripe、Vercel（极简科技感）

**核心原则**：Less is More

