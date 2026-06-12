# FocusMap PWA 版本

这是可以作为 PWA 使用的 FocusMap 版本，已经内置你的 DeepSeek 后端 API 地址。

## 已内置 API

任务解析 API：
https://focusmap-deepseek-api-oy1v.vercel.app/api/parse-tasks

每日总结 API：
https://focusmap-deepseek-api-oy1v.vercel.app/api/day-review

## 本地直接打开

解压后双击 `index.html` 可以直接使用，智能识别会调用上面的 API。

但注意：如果是本地 `file://` 打开，浏览器通常不能安装成真正 PWA，因为 PWA 需要 HTTPS 或 localhost。

## 想像 App 一样添加到桌面

把这个项目上传到 Vercel、GitHub Pages 或其他 HTTPS 网站后，用浏览器打开网址，就可以选择“添加到桌面”或“安装应用”。

## 文件结构

index.html
manifest.webmanifest
service-worker.js
icons/
assets/

## 安全提醒

这里内置的是你的 Vercel 后端 API 地址，不是 DeepSeek Key。DeepSeek Key 仍然保存在 Vercel 环境变量里。
如果你把这个前端公开给别人，别人也会通过你的 Vercel 接口消耗你的 DeepSeek 额度。
