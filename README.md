# Claude_Elite_Excessive_Communicator

A system of prompts for drafting very professional emails to a coworker or manager, written on behalf of the sender while weighing everyone in CC.

| Prompt | File | Runs in | Role |
|---|---|---|---|
| Pu$$y_Grab v1.1 | [prompts/pu55y_grab_v1.1.md](prompts/pu55y_grab_v1.1.md) | Claude, Gemini, DeepSeek, any AI | The user's first assistant. Manages the Scouts and Pu$$y_Banger, runs `Pu$$y_GrabStep 1–6`, returns Outputs 1–9. |
| PG-Thread-Scout v1.1 | [prompts/pg_thread_scout_v1.1.md](prompts/pg_thread_scout_v1.1.md) | Copilot button on the **open email** (scope: that thread) | Runs `Pu$$y_GrabStep 1` only → threadJest. |
| PG-Inbox-Scout v1.1 | [prompts/pg_inbox_scout_v1.1.md](prompts/pg_inbox_scout_v1.1.md) | Copilot button in the **Copilot app / inbox view** (scope: whole mailbox) | Runs `Pu$$y_GrabStep 2, 3, 4` only → retrieval log, refList, deadPool. |
| Pu$$y_Banger v1.1 | [prompts/pu55y_banger_v1.1.md](prompts/pu55y_banger_v1.1.md) | Same AI, managed by Pu$$y_Grab | Research tool. Reads the Google Drive documents, creates "elite Professors", and produces referenced research, SOPs and manuals. |

## Workflow
1. Paste **Pu$$y_Grab** into your AI.
2. Open the email in Outlook, tap **its** Copilot button, and paste **PG-Thread-Scout**. Copy the response and paste it into Pu$$y_Grab (**input 1**).
3. Pu$$y_Grab gives you **PG-Inbox-Scout** with search keywords filled in. Open the **Copilot app** (inbox view), paste it, then copy the response and paste it into Pu$$y_Grab (**input 2**).
4. Pu$$y_Grab runs Pu$$y_Banger: upload the refList documents to Google Drive, then type `done`.
5. Pu$$y_Grab starts from `Pu$$y_GrabStep 5`: Master Draft, then Final Draft.

Any tool that needs PG-Scout data receives **two inputs**: input 1 from PG-Thread-Scout and input 2 from PG-Inbox-Scout.

## Known limits
- The Copilot button on an open email can only see that thread, so the mailbox search must run in the Copilot app (inbox view). Mailbox-wide search needs a Microsoft 365 Copilot licence.
- Reading Google Drive and saving a Google Doc needs a model with Drive access, such as Claude with the Google Drive connector or Gemini in Workspace. Otherwise, attach the files and save the copyable text yourself.
- The "elite Professors" are simulated specialist personas unless your platform supports sub-agents.

## Version log
- **v1.1:** PG-Scout split into PG-Thread-Scout (Step 1) and PG-Inbox-Scout (Steps 2–4), one per Copilot button. Pu$$y_Grab now takes two inputs and pre-fills the search keywords. The inbox search uses narrow keyword searches, with a "NO VERIFIED RESULTS" fallback.
- **v1.0:** first release of Pu$$y_Grab, Pu$$y_Banger and PG-Scout.
