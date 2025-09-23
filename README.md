# Github Plus for Typora ✨

[](https://opensource.org/licenses/MIT)
[](https://www.google.com/search?q=https://github.com/33niang/typora-theme-github-plus)
[](https://www.google.com/search?q=https://github.com/33niang)

这是一款为 [Typora](https://typora.io/) 设计的深度定制主题，它基于官方默认的 `Github` 主题，但在其简洁明了的基础上，注入了大量美学与实用性增强功能。`Github Plus` 旨在为您提供一个既沉浸又不失活力的写作环境。

## 🚀 核心特性 (Features)

  * **✒️ 精选字体，优化阅读**:

      * **中西文双字体方案**: 中文内容主要采用 `MapleMonoNormal-Bold` (霞鹜文楷等宽) 字体，字形优雅且带有手写的自然感；英文与代码则选用 `Google Sans Code Semibold`，显示效果清晰锐利，代码辨识度更高。
      * **Minimalist 风格**: 完整继承 `Github` 主题的优点，界面干净，元素间距舒适，让您能更专注于内容创作。

  * **🎨 动态与美学**:

      * **左下角动态 GIF**: 在编辑器左下角加入了可轮播切换的 GIF 动图，设计灵感来源于优秀的 `onelight` 主题，为静态的写作环境增添一丝活力。
      * **界面元素美化**: 对左下角的功能按钮进行了美化，使其颜色更醒目，交互更友好。

  * **🛡️ 水印保护 (可选)**:

      * 提供一个额外的 `github-plus-watermark.css` 文件，它可以在编辑器中实时显示全覆盖的 SVG 水印，并在导出 PDF 或打印时自动应用，有效保护您的文档版权。

## 📸 主题预览 (Preview)

<table>
  <tr>
    <td><img src="./github-plus/img/bg5.gif" alt="Preview GIF 1" width="200"/></td>
    <td><img src="./github-plus/img/mutou.gif" alt="Preview GIF 2" width="200"/></td>
    <td><img src="./github-plus/img/mutou2.gif" alt="Preview GIF 3" width="200"/></td>
  </tr>
</table>

## 🛠️ 安装指南 (Installation)

1.  下载本项目的所有文件。
2.  打开 Typora，导航至 `文件` -\> `偏好设置...` -\> `外观`。
3.  点击 `打开主题文件夹` 按钮。
4.  将下载的 `github-plus.css` 以及 `github-plus` 文件夹完整复制到该目录中。如果您需要水印功能，请额外复制 `github-plus-watermark.css` 文件。
5.  完全重启 Typora。
6.  从菜单栏的 `主题` 菜单中选择 `Github Plus` (无水印) 或 `Github Plus Watermark` (带水印) 即可生效。

您的主题文件夹最终结构应如下所示：

```
themes/
├── github-plus.css           # 核心主题文件
├── github-plus-watermark.css # (可选) 带水印的主题文件
└── github-plus/
    └── img/
        ├── bg.gif
        └── ... (其他GIF图片)
```

## 🔧 自定义 (Customization)

您可以轻松地对主题进行个性化调整。

### 1\. 修改字体

1.  使用文本编辑器打开 `github-plus.css` (或带水印版) 文件。
2.  定位到 `/* --- 新增：自定义字体设置 --- */` 注释部分。
3.  修改 `body` 和 `.md-fences, code, tt` 中的 `font-family` 属性，替换为您想要的字体名称。

### 2\. 修改左下角 GIF

1.  **增删 GIF**: 直接将您的 GIF 图片放入 `github-plus/img/` 文件夹内。
2.  **调整轮播**:
      * 在 CSS 文件中找到 `/* --- 新增：左下角GIF轮播 --- */` 注释。
      * **修改动画时长**: `animation-duration` 的值决定了所有图片轮播一遍的总时长。
      * **修改动画关键帧**: 在 `@keyframes image-switcher` 规则中，根据您图片的数量和顺序，修改或增删 `background-image` 路径，并确保百分比均匀分布。

## 📜 开源许可 (License)

本项目基于 [MIT License](https://www.google.com/search?q=LICENSE) 开源。您可以自由地使用、修改和分发。

## 🙏 特别致谢 (Credits)

  * 主题的初始结构基于 Typora 官方的 [Github Theme](https://github.com/typora/typora-default-themes)。
  * 左下角 GIF 动图功能的设计灵感来源于优秀的 [onelight-theme](https://github.com/upupming/typora-theme-onelight)。
