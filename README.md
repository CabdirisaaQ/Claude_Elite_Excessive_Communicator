# Claude_Elite_Excessive_Communicator

A three-prompt system for drafting very professional emails to a coworker or manager, written on behalf of the sender while weighing everyone in CC.

| Prompt | File | Runs in | Role |
|---|---|---|---|
| Pu$$y_Grab v1.0 | [prompts/pu55y_grab_v1.0.md](prompts/pu55y_grab_v1.0.md) | Claude, Gemini, DeepSeek, any AI | The user's first assistant. Runs `Pu$$y_GrabStep 1–6`, manages PG-Scout and Pu$$y_Banger, returns Outputs 1–9. |
| Pu$$y_Banger v1.0 | [prompts/pu55y_banger_v1.0.md](prompts/pu55y_banger_v1.0.md) | Same AI, managed by Pu$$y_Grab | Research tool. Reads the Google Drive documents, creates "elite Professors", and produces referenced research, SOPs and manuals. |
| PG-Scout v1.0 | [prompts/pg_scout_v1.0.md](prompts/pg_scout_v1.0.md) | Outlook Copilot | Data gatherer. Runs `Pu$$y_GrabStep 1–4` and returns threadJest, the retrieval log, refList and deadPool. |

## Workflow
1. **First run:** paste Pu$$y_Grab plus the email/thread into your AI. It runs `Pu$$y_GrabStep 1→6`. Output 8 gives you the ready-to-paste PG-Scout prompt.
2. **Future runs:** paste PG-Scout into the Outlook Copilot button with the thread open, then copy its full response.
3. Paste that response into Pu$$y_Grab. It skips Steps 1–4 and runs Pu$$y_Banger: upload the refList documents to Google Drive, then type `done`. It then starts from `Pu$$y_GrabStep 5` (Master Draft → Final Draft).

## Known limits
- Claude, Gemini and DeepSeek usually can't read Outlook. That's why PG-Scout exists.
- Reading Google Drive and saving a Google Doc needs a model with Drive access, such as Claude with the Google Drive connector or Gemini in Workspace. Otherwise, attach the files and save the copyable text yourself.
- The "elite Professors" are simulated specialist personas unless your platform supports sub-agents.

## Version log
- **v1.0:** first release of Pu$$y_Grab, Pu$$y_Banger and PG-Scout.
