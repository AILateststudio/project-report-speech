# project-report-speech · 课题汇报讲稿写作 Skill

根据课题汇报 PPT 撰写或修改配套的口头汇报讲稿（Word）。适用于结题汇报、开题汇报、会议报告、项目评审、学术答辩。

## 特点

- 讲 PPT 而不是念 PPT：通俗易懂，让不同背景的听众都能听明白
- 聚焦听众关心的四件事：为什么做、做了什么、得到什么结论、有什么新意
- 方法少讲、结论多讲
- 严格按 PPT 顺序，一页一段，翻页对得上
- 口语为主、讲得出口，同时保留 PPT 关键词作为记忆锚点
- 只说核心数字，其余用概数；数据和方法表述忠于 PPT，不添不夸
- 按页面类型（背景、方法、图表、案例、建议等）给出讲法，PPT 有哪类用哪类
- 结尾：一句总结 + 一句呼吁或展望 + 致谢
- 篇幅按汇报时长定，可长可短（约 220–260 字/分钟，例如 10 分钟约 2000–2500 字，紧凑排版约 2 页 A4；5 分钟约 1 页，20 分钟约 4 页）
- 一键生成 Word：默认紧凑版（宋体五号、1.15 倍行距），也可选宽松版（小四号、1.5 倍行距）；有页数要求时按要求压缩或放宽

## 使用

1. 把 `SKILL.md` 加入你的 AI 助手技能库（Claude Skills、Notion AI Skills 等），或直接作为提示词使用。
2. 上传 PPT（和旧讲稿，如有），让 AI “按这个 skill 写汇报讲稿”。
3. 生成 Word：

```bash
pip install python-docx
python3 scripts/build_speech_docx.py speech.json out.docx          # 紧凑版（宋体五号、1.15 倍行距）
python3 scripts/build_speech_docx.py speech.json out.docx --normal # 宽松版
```

`speech.json` 格式：

```json
{"title": "XXX：汇报讲稿（约10分钟）",
 "sections": [{"heading": "第1页｜封面", "paragraphs": ["各位专家、各位老师，大家好！……"]}]}
```
