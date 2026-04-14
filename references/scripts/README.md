# 喜剧素材库 — 文字稿索引

> 通过 Whisper ASR (medium 模型) 从 YouTube 视频音频提取的文字稿

## 完成状态

| 演员/节目 | 视频 | 时长 | 文字稿 | 字数 | 状态 |
|-----------|------|------|--------|------|------|
| 杨雨光 | 小品×2 | 15min+16min | ✅ 2个 | ~14,000字 | ✅ 完成 |
| 张兴朝 | 小品合集 | 41min | ✅ 1个 | ~19,400字 | ✅ 完成 |
| 李诞 | 脱口秀大会 | 43min | ✅ 1个 | ~29,000字 | ✅ 完成 |
| 徐志胜 | 脱口秀合集 | 1h11min | ✅ 1个 | ~38,100字 | ✅ 完成 |
| 蒋龙张弛 | 精选合集 | 1h01min | ✅ 1个 | ~23,700字 | ✅ 完成 |
| 酷酷的天放 | Sketch合集 | 59min | ✅ 1个 | ~31,000字 | ✅ 完成 |
| 四世同堂 | 经典合集 | 2h6min | ✅ 1个 | ~45,800字 | ✅ 完成 |
| 刘同某某某 | 合集 | 2h13min | ✅ 1个 | ~52,700字 | ✅ 完成 |
| 郭德纲 | 相声 | 50min | ❌ 暂跳过 | - | ⏸ 搁置 |

**已完成**: 9/10 视频，~254,000字素材
**搁置**: 1个（郭德纲）

## 目录结构

```
scripts/
├── README.md              ← 本文件
├── 杨雨光/
│   ├── README.md          ← 视频元数据
│   ├── 杨雨光1_*_transcript.txt      ← 纯文字稿
│   ├── 杨雨光1_*_timestamped.txt     ← 带时间戳
│   ├── 杨雨光2_*_transcript.txt
│   └── 杨雨光2_*_timestamped.txt
├── 张兴朝/
│   ├── README.md
│   ├── *_transcript.txt
│   └── *_timestamped.txt
├── 李诞/
│   └── ...
├── 徐志胜/
│   └── ...
├── 蒋龙张弛/
│   └── ...
├── 酷酷的天放/
│   └── ...
├── 四世同堂/
│   └── ...
├── 刘同某某某/
│   └── ...
├── 郭德纲/            ← 暂跳过
└── _audio/             ← 音频文件（临时）
```

## 文件说明

- `*_transcript.txt` — 纯文字稿，连续文本，适合阅读和学习
- `*_timestamped.txt` — 带时间戳的逐句文稿，格式 `[MM:SS-MM:SS] 文字`，适合对照视频

## 视频源

| ID | 链接 |
|----|------|
| 张兴朝 | https://www.youtube.com/watch?v=Y8pOms6RtHI |
| 杨雨光1 | https://www.youtube.com/watch?v=2GqJ14YsMw4 |
| 杨雨光2 | https://www.youtube.com/watch?v=pSMgH06nh6g |
| 李诞 | https://www.youtube.com/watch?v=OMcwCk0a1Eo |
| 徐志胜 | https://www.youtube.com/watch?v=8sbJMd4A92s |
| 郭德纲 | https://www.youtube.com/watch?v=3-Kfi6knGNo |
| 刘同某某某 | https://www.youtube.com/watch?v=zZccrXAHfzc |
| 四世同堂 | https://www.youtube.com/watch?v=pZr5hyb-s8I |
| 蒋龙张弛 | https://www.youtube.com/watch?v=pPdp1kXBiiA |
| 酷酷的天放 | https://www.youtube.com/watch?v=IxEHDTzuWgs |

## 技术方案

- **音频提取**: yt-dlp + Chrome cookies 认证 → MP3
- **语音转文字**: OpenAI Whisper (medium 模型) → 中文
- **环境**: macOS + MPS GPU 加速
