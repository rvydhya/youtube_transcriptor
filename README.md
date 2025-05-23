# YouTube Transcriptor MCP Tool

This is a Model Context Protocol (MCP) tool for transcribing YouTube videos using the `youtube-transcript-api`.

## Features
- Extracts and transcribes from YouTube videos (manual or autogenerated). Enables retrieval of transcripts from YouTube videos.
- Exposes a single tool: `transcribe_video(video: str)`.

## Usage

### 1. Prerequisites
- Python 3.12+
- Install dependencies:
  ```sh
  pip install -r requirements.txt
  ```

### 2. Running the Tool
You can run the tool directly:
```sh
python youtube.py
```

### 3. Using with VS Code (Manual MCP Config)
To use this tool as an MCP server in VS Code, add the following to your `.vscode/settings.json` or your MCP client configuration:

```json
"youtube_transcriptor": {
  "type": "stdio",
  "command": "python",
  "args": ["PATH\\transcription\\youtube.py"]
}
```
Replace `PATH` with the absolute path to your workspace root.

### 4. Using the Tool
Once configured, you can call the `transcribe_video` tool from your MCP client or compatible VS Code extension, passing a YouTube video URL as the argument.

---

**Example:**
```python
result = transcribe_video("https://www.youtube.com/watch?v=VIDEO_ID")
print(result)
```

---

## License
MIT
