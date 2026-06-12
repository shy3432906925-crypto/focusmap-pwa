# FocusMap v3 专注图谱

直接双击 `index.html` 即可运行，不需要安装依赖。

## v3 新增内容

- 默认每日任务为空
- 每日任务支持自然语言导入
- 没有 API 时使用本地关键词识别
- 可填写自己的任务解析 API 和每日总结 API
- 专注时间和休息时间可自定义
- 单个任务也可以设置专注和休息时长
- 专注页面会随时间阶段变化，并弹出主题化文字
- 今日图谱改为发散式地图，不再是时间轴
- 增加能量值、休息盲盒、完成动画、主题化节点名称
- 三套动态主题：宇宙航行风、中国武侠风、原创奶龙可爱风

## API 接入说明

不要把 OpenAI API Key 写在前端。建议用 Vercel、Netlify、Cloudflare Worker 或 Node 后端做转发。

前端任务解析接口建议返回：

```json
{
  "tasks": [
    {
      "subject": "C/C++",
      "content": "复习指针和 fread/fwrite",
      "estimatedMinutes": 90,
      "taskType": "复习",
      "difficulty": "中等"
    }
  ]
}
```

每日总结接口建议返回：

```json
{
  "summary": "今天 C++ 用时超过预计，建议明天先复盘指针。",
  "tomorrowSuggestions": [
    {"subject":"C/C++", "content":"返回指针复盘", "estimatedMinutes":20}
  ]
}
```
