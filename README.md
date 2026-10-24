# Claude_Elite_Excessive_Communicator

A system of prompts for drafting very professional emails to a coworker or manager, written on behalf of the sender while weighing everyone in CC.

## Copy only one prompt
**[prompts/pu55y_grab_v1.2.md](prompts/pu55y_grab_v1.2.md)** is the only file you need. It contains PG-Thread-Scout, PG-Inbox-Scout and Pu$$y_Banger, and gives you each Copilot prompt when it's time.

## How a run works
1. **Turn 1:** paste Pu$$y_Grab into Claude, Gemini, DeepSeek or another AI. It replies with **only** the PG-Thread-Scout text.
2. Open the email in Outlook, tap **its** Copilot button, paste PG-Thread-Scout, then copy Copilot's reply back into the chat.
3. **Turn 2:** Pu$$y_Grab replies with **only** the PG-Inbox-Scout text, with your threadJest already inside it.
4. Open the **Copilot app** (inbox view), paste PG-Inbox-Scout, then copy Copilot's reply back into the chat.
5. **Turn 3:** Pu$$y_Grab runs Pu$$y_Banger. Upload the refList documents to Google Drive and type `done`. It then continues from `Pu$$y_GrabStep 5` and gives you Outputs 1–9, including the Master Draft and the Final Draft.

| Prompt | Runs in | Does |
|---|---|---|
| Pu$$y_Grab v1.2 | Claude, Gemini, DeepSeek, any AI | Manages everything; runs Steps 5–6 and Outputs 1–9 |
| PG-Thread-Scout v1.2 ([reference copy](prompts/pg_thread_scout_v1.2.md)) | Copilot on the open email | Step 1 → threadJest |
| PG-Inbox-Scout v1.2 ([reference copy](prompts/pg_inbox_scout_v1.2.md)) | Copilot app (inbox) | Checks threadJest against the Thread-Scout reply, then Steps 2–4 → search log, refList, deadPool |
| Pu$$y_Banger v1.1 ([reference copy](prompts/pu55y_banger_v1.1.md)) | Same AI as Pu$$y_Grab | Research, SOPs and manuals from your Google Drive documents |

## Copilot-friendly wording
The two Copilot prompts use plain business requests: no persona ("You are…"), no tool names, no crude or unusual words, and no override-style commands. They also explicitly allow Copilot to say when it can't find something, so it's less likely to be blocked by company Copilot filters.

## Known limits
- The two Copilot buttons are separate chats, so the inbox Copilot can't see the thread Copilot's reply. That's why Pu$$y_Grab embeds threadJest in PG-Inbox-Scout.
- Mailbox-wide search needs a Microsoft 365 Copilot licence.
- Reading Google Drive and saving a Google Doc needs a model with Drive access, such as Claude with the Google Drive connector or Gemini in Workspace. Otherwise, attach the files and save the copyable text yourself.
- The "elite Professors" are simulated specialist personas unless your platform supports sub-agents.

## Version log
- **v1.2:** Pu$$y_Grab is self-contained and hands out the Copilot prompts one turn at a time. The Copilot prompts were rewritten in plain wording to avoid security filters. PG-Inbox-Scout checks threadJest against the Thread-Scout reply before searching.
- **v1.1:** PG-Scout split into PG-Thread-Scout and PG-Inbox-Scout.
- **v1.0:** first release.
