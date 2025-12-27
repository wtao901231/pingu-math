# 背景音乐文件目录

## 说明

请将你的背景音乐文件放在这个目录下。

## 文件要求

- **文件名**：`background.mp3`（或在 `src/composables/useBackgroundMusic.ts` 中修改配置）
- **格式**：MP3（推荐）
- **大小**：建议 3MB 以内
- **比特率**：128kbps 已足够
- **声道**：单声道或立体声均可

## 音频优化建议

如果你的音频文件过大，可以使用以下工具进行优化：

### 使用 FFmpeg 压缩

```bash
# 转换为 128kbps MP3
ffmpeg -i input.mp3 -b:a 128k output.mp3

# 转换为单声道 128kbps MP3（更小）
ffmpeg -i input.mp3 -b:a 128k -ac 1 output.mp3
```

### 在线工具

- [Online Audio Converter](https://online-audio-converter.com/)
- [CloudConvert](https://cloudconvert.com/mp3-converter)

## 示例

```
public/music/
└── background.mp3  <- 将你的音乐文件放在这里
```

## 版权提醒

⚠️ 请确保你使用的音乐文件拥有合法的使用权限。

推荐免费音乐资源：
- [YouTube Audio Library](https://www.youtube.com/audiolibrary)
- [Free Music Archive](https://freemusicarchive.org/)
- [Incompetech](https://incompetech.com/music/)
- [Bensound](https://www.bensound.com/)
