# Lab 4: Tutor Agent (LangGraph vs n8n vs Hermes)

## Files

- `tutor-agent-lab.html`: the GUI (demo, results, comparison, checklist). One self-contained file.
- `tutor_graph.py`: the LangGraph version of the agent.

n8n and Hermes are not files. The n8n workflow lives in your n8n Cloud account (workflow "Tutor Agent"), and the Hermes skill and memory live in `C:\Users\HP\AppData\Local\hermes\` (`skills\tutor-agent\SKILL.md` and `memories\USER.md`).

## Open the GUI in VS Code

1. Put both files in one folder and open it in VS Code (File, Open Folder).
2. Easiest: right-click `tutor-agent-lab.html` in the Explorer panel and choose "Reveal in File Explorer", then double-click it to open in your browser.
3. Or install the "Live Server" extension, right-click the file, and choose "Open with Live Server".

No install or internet is needed. Without internet the page falls back to a system font.

## Run the LangGraph script

In the VS Code terminal (PowerShell):

```
python -m pip install langgraph langchain-openai
$env:OPENROUTER_API_KEY="your-new-key"
python tutor_graph.py
```

- Create a new OpenRouter key first (openrouter.ai, API Keys). Do not reuse keys that appeared in screenshots or chats.
- The model is `xingchen-agi/xing4.0-29b-a4b:free`. If it returns 429 errors, the script waits and retries. You can also swap in another `:free` model.
- The key only lasts for that terminal window. Set it again if you reopen the terminal.

## Before the discussion

- Delete the old exposed API keys (Gemini in AI Studio, old OpenRouter keys).
- Take the n8n screenshots (canvas and `tutor_results` table) and the Hermes screenshots.
- n8n Cloud trial lasts 14 days from sign-up (about 18 October), so export or screenshot the workflow before it ends.
