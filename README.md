# Typora Theme - Github Plus

这是一个基于 Typora 默认的 `Github` 主题进行美化和功能增强的自定义主题。它在保留 `Github` 主题简洁、清晰风格的基础上，融入了更多个性化元素，旨在提供更舒适、更具创造力的写作体验。

This is a custom theme for Typora, based on the default `Github` theme. It enhances the original's clean style with more personalized features, aiming to provide a more comfortable and creative writing experience.


---

## ✨ 主要特性 (Features)

* **🎨 优雅的字体融合**:
    * **英文字体**: 采用了 `Google Sans Code Semibold`，显示代码和英文时更加清晰、现代化。
    * **中文字体**: 采用了 `MapleMonoNormal-Bold` (霞鹜文楷等宽)，让中文内容在保持等宽美感的同时，兼具手写的自然感。

* **🎬 左下角动态GIF**:
    * 在编辑器的左下角增加了一个可轮播的 GIF 动图，灵感来源于优秀的 `onelight` 主题，为静态的写作环境增添一丝活力。
    * 支持轻松自定义，您可以随意增删或修改动图。

* ** minimalist 风格**:
    * 继承了 `Github` 主题的所有优点，界面干净，元素间距舒适，让您能更专注于内容创作。

## ⚙️ 安装方法 (Installation)

1.  下载本项目。你可以直接 `git clone` 或者下载 ZIP 压缩包。
2.  打开 Typora，进入 `文件` -> `偏好设置...` -> `外观`。
3.  在 `主题` 部分，点击 `打开主题文件夹` 按钮。
4.  将本项目中的 `github-plus.css` 文件和 `github-plus` 文件夹完整地复制到打开的主题文件夹中。
5.  完全关闭并重启 Typora。
6.  在菜单栏 `主题` 菜单中选择 `Github Plus` 即可应用。

最终你的主题文件夹结构应如下所示：

```
themes/
├── github-plus.css
└── github-plus/
    └── img/
        ├── bg.gif
        ├── mutou.gif
        └── ... (你的其他GIF图片)
```

## 🛠️ 自定义 (Customization)

你可以非常轻松地对主题进行个性化修改。

### 修改字体

1.  用文本编辑器打开 `github-plus.css` 文件。
2.  找到 `/* --- 新增：自定义字体设置 --- */` 这段注释。
3.  在 `body { ... }` 中，修改 `font-family` 的值即可更换全局字体。

    ```css
    /* 例如，将 "MapleMonoNormal-Bold" 替换成 "微软雅黑" */
    body {
        font-family: "Google Sans Code Semibold", "微软雅黑", "Open Sans", sans-serif;
    }
    ```

### 修改左下角GIF

1.  **增删 GIF**:
    * 直接将你想要的 GIF 图片放入 `github-plus/img/` 文件夹中。

2.  **调整轮播**:
    * 打开 `github-plus.css` 文件，找到 `/* --- 新增：左下角GIF轮播 --- */` 这段注释。
    * **修改总时长**: 如果你有 N 张图片，想让每张显示 M 秒，那么 `animation-duration` 的值就应该是 `N * M` 秒。
    * **修改关键帧**: 在 `@keyframes image-switcher` 中，添加或删除对应的图片路径。请确保百分比均匀分布（`100% / N`）。

    ```css
    /* 示例：如果你有3张图，每张显示5秒 */
    footer.ty-footer::before {
        /* ... */
        animation-duration: 15s; /* 3 * 5 = 15秒 */
        /* ... */
    }

    @keyframes image-switcher {
        0% { background-image: url("./github-plus/img/图1.gif"); }
        33.33% { background-image: url("./github-plus/img/图2.gif"); }
        66.66% { background-image: url("./github-plus/img/图3.gif"); }
        100% { background-image: url("./github-plus/img/图1.gif"); }
    }
    ```

## 🙏 致谢 (Credits)

* 本主题基于 Typora 官方的 [Github Theme](https://github.com/typora/typora-default-themes)。
* 左下角 GIF 动图功能的设计灵感来源于优秀的 [onelight-theme](https://github.com/upupming/typora-theme-onelight)。

---

希望你喜欢这个主题！
