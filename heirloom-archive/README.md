# Heirloom Archive — The Enigmatic Payload 🗃️🔐

_A seemingly ordinary `.txt` file, hiding secrets beneath its surface._

---

## 📖 The Story

A forgotten package appeared on the network in a strange file format: a plain-looking text file that conceals more than it first reveals. Some whisper it contains echoes of old programs; others claim a secret is buried within, awaiting a patient explorer. Only those who look closely, peel back its layers, and follow subtle clues will uncover the hidden truth.

---

## 🎯 Challenge

- **Goal**: Recover the hidden flag from the provided text file.
- **Given**: `ddiagd972edi29738hiagfoeuwb.txt`
- **Submit**: The exact flag string you extract (no extra whitespace/newlines).

---

## 🧪 Things to Try

- Verify the true file type; look for disguised or embedded content.
- Inspect hex around the start/end; check for unusual headers/footers or whitespace.
- Consider common re-encodings or simple layering (base64/zip/etc.).

---

## 🛠️ Helpful Commands

- Quick identity:

```bash
file ddiagd972edi29738hiagfoeuwb.txt
```

- Peek at beginning/end in hex:

```bash
xxd -g 1 -l 256 ddiagd972edi29738hiagfoeuwb.txt
xxd -g 1 -s -256 ddiagd972edi29738hiagfoeuwb.txt
```

- Basic strings:

```bash
strings -n 6 ddiagd972edi29738hiagfoeuwb.txt | head
```

---

## 📦 Files

- `ddiagd972edi29738hiagfoeuwb.txt`

---

## ✅ Submission

Submit the exact recovered flag string. If there are intermediate layers (encodings, archives, or stego), keep peeling until you reach the final, human‑readable flag. Accuracy matters — avoid extra whitespace or line breaks.
