# 工具脚本说明

## podcast-transcribe.py

播客/视频转录工具，基于 faster-whisper 和 yt-dlp。

### 安装依赖

```bash
pip install faster-whisper yt-dlp
# 系统依赖：ffmpeg
# macOS: brew install ffmpeg
# Ubuntu: sudo apt install ffmpeg
```

### 使用方式

```bash
# 转录播客
python tools/podcast-transcribe.py "https://www.xiaoyuzhoufm.com/episode/xxx" -t "播客标题"

# 转录视频
python tools/podcast-transcribe.py "https://www.bilibili.com/video/xxx" -p video -t "视频标题"

# 转录 YouTube
python tools/podcast-transcribe.py "https://youtube.com/watch?v=xxx" -p video -t "视频标题"
```

### 输出

- 音频文件保存在 `raw/podcasts/` 或 `raw/videos/`
- 转录文本（Markdown 格式）与音频文件同名

### 与 LLM Wiki 集成

转录完成后，直接对我说：**"请摄入 [文件名].md"**，我会：
1. 阅读转录文本
2. 提取关键信息
3. 创建/更新 Wiki 页面
4. 更新索引和日志
