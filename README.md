# QR Strobe

Offline, air-gapped file transfer between devices using animated QR codes (camera + strobing display). No server, no network required.

🔗 **Try it**: https://hemi-taro.github.io/qr-strobe/

## Usage

### Sending
1. Open the "Send" tab and choose a file
2. Adjust frame rate, chunk size, and QR size if needed
3. Tap "Start" to begin displaying the animated QR sequence

### Receiving
1. Open the "Receive" tab and tap "Start Camera"
2. Point the camera at the sending device's screen (get close enough that the QR fills the frame for best results)
3. Once all chunks are received, tap "Save File"

### Install on iPhone
Open the link above in Safari, tap Share → **Add to Home Screen**. Works offline once installed.

## Fountain Mode

By default, files are split into numbered chunks and sent in a fixed loop — the receiver waits for every chunk, including whichever one it missed last.

Fountain mode instead sends an endless stream of randomly-combined chunks, so the receiver can reconstruct the file from *any* sufficiently large set of frames, in any order. No more waiting for one stubborn missed frame to loop back around. Useful for large or unreliable transfers; adds a small overhead in frame count.

## Compression

The "Compress" toggle gzips the file before sending, and previews how much it actually saves before you commit to it.

- **Big win**: plain text — GPX, KML, CSV, JSON, logs
- **No real benefit**: already-compressed formats — JPEG, PNG, MP4, ZIP, and also DOCX/XLSX/PPTX (these are ZIP containers internally, so they're already compressed)

Check the preview; if it says compression makes the file bigger, leave it off.

## Disclaimer

Use at your own risk.
