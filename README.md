好的，这是根据我们之前讨论的所有修改（包括内置字体文件）最终确定的 `README.md` 文件内容。

您可以直接复制下面的完整代码。

-----

# Github Plus for Typora ✨

[](https://opensource.org/licenses/MIT)
[](https://www.google.com/search?q=https://github.com/33niang/typora-theme-github-plus)
[](https://www.google.com/search?q=https://github.com/33niang)

这是一款为 [Typora](https://typora.io/) 设计的深度定制主题，它基于官方默认的 `Github` 主题，但在其简洁明了的基础上，注入了大量美学与实用性增强功能。`Github Plus` **内置了精选字体文件**，确保每一位用户都能获得开箱即用、完美统一的视觉体验。

## 🚀 核心特性 (Features)

  * **✒️ 内置精选字体，开箱即用**:

      * **中西文双字体方案**: 中文内容采用 `MapleMonoNormal-Bold` (霞鹜文楷等宽)，字形优雅；英文与代码则选用 `Google Sans Code`，显示效果清晰锐利。所有字体均已内置，无需用户手动安装。
      * **Minimalist 风格**: 继承 `Github` 主题的优点，界面干净，元素间距舒适，让您能更专注于内容创作。

  * **🎨 动态与美学**:

      * **左下角动态 GIF**: 在编辑器左下角加入了可轮播切换的 GIF 动图，为静态的写作环境增添一丝活力。
      * **界面元素美化**: 对左下角的功能按钮进行了美化，使其颜色更醒目，交互更友好。

  * **🛡️ 水印保护 (可选)**:

      * 提供一个额外的 `github-plus-watermark.css` 文件，它可以在编辑器和导出的PDF中显示全覆盖水印，有效保护您的文档版权。

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
4.  将下载的 `github-plus.css` 以及 **完整的 `github-plus` 文件夹** 复制到该目录中。如果您需要水印功能，请额外复制 `github-plus-watermark.css` 文件。
5.  完全重启 Typora。
6.  从菜单栏的 `主题` 菜单中选择 `Github Plus` (无水印) 或 `Github Plus Watermark` (带水印) 即可生效。

您的主题文件夹最终结构应如下所示，**请确保 `fonts` 文件夹被正确复制**：

```
themes/
├── github-plus.css           # 核心主题文件
├── github-plus-watermark.css # (可选) 带水印的主题文件
└── github-plus/
    ├── fonts/                # <-- 存放字体文件
    │   ├── MapleMonoNormal-Bold.ttf
    │   └── GoogleSansCode[wght].ttf
    └── img/                  # <-- 存放GIF图片
        └── bg.gif
```

## 🔧 自定义 (Customization)

### 1\. 替换内置字体

1.  将您自己的字体文件（推荐 `.ttf` 或 `.woff2` 格式）放入 `github-plus/fonts/` 文件夹。
2.  使用文本编辑器打开 `github-plus.css` (或带水印版) 文件。
3.  找到 `/* --- 新增：自定义字体设置 (内置字体) --- */` 部分。
4.  在 `@font-face` 规则中，修改 `src: url(...)` 的路径，使其指向您的新字体文件名。

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
