## 🎙️ Toly Praises ETH — The Echo Hides a Truth

### 📖 The Story

We received this audio from an unknown group. It sounds like Toly… but he’s “praising” Ethereum’s rollup model a bit too enthusiastically. That can’t be right. There’s a persistent static beep and some odd artifacts — almost like he hid a message for us inside the noise.

---

### 🎯 Challenge

- **Goal**: Recover the hidden flag from the provided audio.
- **Given**: `toly_praises_eth_praise.wav`
- **Submit**: The exact flag text you extract (no extra spaces/newlines).

---

### 🧪 Things to Try

- View a spectrogram; scan for visible patterns or text.
- Compare left vs right channels; try L−R or mono.
- Reverse or slightly change speed to reveal masked speech.

---

### 🛠️ Helpful Commands

- Spectrogram (PNG) via FFmpeg:

```bash
ffmpeg -i toly_praises_eth_praise.wav -lavfi \
  showspectrumpic=s=1920x1080:legend=disabled:scale=log \
  spectrogram.png
```

- Split left/right channels:

```bash
ffmpeg -i toly_praises_eth_praise.wav \
  -map_channel 0.0.0 left.wav -map_channel 0.0.1 right.wav
```

- Reverse audio:

```bash
ffmpeg -i toly_praises_eth_praise.wav -af areverse reversed.wav
```

---

### 📦 Files

- `toly_praises_eth_praise.wav`

---

### ✅ Submission

Submit the exact recovered flag string. If you decode intermediate hints (tones, images from spectrograms, etc.), follow them through until you obtain the final flag. Accuracy matters — avoid extra whitespace or line breaks.
