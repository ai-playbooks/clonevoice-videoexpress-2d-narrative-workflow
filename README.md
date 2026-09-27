# CloneVoice + VideoExpress Narrative Video Workflow

Use [CloneVoice.ai](https://www.clonevoice.ai) and [VideoExpress.ai](https://www.videoexpress.ai) together to create full-length animated 2D narrative videos with scene-by-scene narration and review.

Your AI agent (Claude, ChatGPT, or Codex) drives VideoExpress in your browser: it writes and fact-checks the script, splits it sentence by sentence, generates every animated scene **against that sentence's own narration audio** through the built-in CloneVoice.ai integration, and assembles the finished video where every visual lands at the correct moment — because every clip is rendered in sync with its own line of narration.

## Video motion prompting

Section 11 of [SYSTEM_PROMPT.md](SYSTEM_PROMPT.md) uses motion prompting: chronological visual action, a clear camera path, and preservation of the accepted 2D reference style. Video prompts contain no narration, dialogue, voice, music, sound, or other audio instructions. Narration is entered only in the separate Create Narration Video audio dialog. The construction, map, and combat examples follow this rule.

The production sequence, 120-character narration chunks, CloneVoice integration, character references, assembly, and export remain in place. The customer states that all their products provide unlimited generation, including VideoExpress and CloneVoice used here. Their VideoExpress account is also described as a lifetime purchase with no separate per-generation charge. Use included features without repeated generation approvals; optional upgrades and purchases require their own authorization. Single continuous shots remain the default.

The motion guidance is adapted for this workflow's existing narration-only audio path.

## Execution safeguards for GPT, Claude, and Codex

Section 0.2 of [SYSTEM_PROMPT.md](SYSTEM_PROMPT.md) makes the execution checks explicit for every agent, including examples and retries:

- Complete prerequisite gates and record evidence before submitting.
- Reuse character references for continuity; generate scene-specific stills and repeat the entire row loop after a rejected video.
- Keep manual duration and Advanced Mode off; measure source narration and rendered clip lengths separately, and reject a clip that cuts off its words. Use natural visual pacing in the motion prompt when a scene needs more room.
- Track image and video enhancement separately, and investigate unexpected prompt rewrites.
- Record UI mismatches without silently relaxing required checks.
- Limit downloads to defined workflow needs; do not install tools as an improvised fix.
- Never claim audio or visual verification beyond what the tools actually allow.

The ledger now retains gate checks, attempt history, both audio and clip durations, and unresolved verification. If required evidence cannot be obtained, the agent must report that specific limitation rather than claim success. These instructions reduce ambiguity; they cannot guarantee that every model will comply. Copy the entire updated system prompt into each new agent session.

## Security checks

Section 0.3 adds checks within the existing gates: actual customer authorization, untrusted document/page content, secret-safe integration checks, available tools, permitted transfers, consent and agreements, cumulative retry limits, and accurate error reporting. Uncertain submissions are reconciled before retrying; pending jobs are not duplicated after a timeout. Creative prompts and production order are unchanged. Reviewing this document does not authorize running production. These checks cannot guarantee that every platform will accept a request.

## One deterministic path — by design

The workflow follows the fixed gate sequence and its documented recovery branches, within customer authorization and available capabilities:

1. **GATE 0** — Verify the CloneVoice API key on both sides before anything is generated.
2. **GATE 1** — Research, script, and a **frozen chunk table**: one sentence per row, 120 characters max (the hard cap enforced by the app), declared before any audio exists.
3. **GATE 2** — Character references generated first and saved to My AI Images, then reused in every scene via Consistent Character mode.
4. **GATE 3** — The per-scene loop: still image → narration audio for that one sentence (CloneVoice voice, inside the Create Narration Video dialog) → narration-synced clip. One row, one clip. A proof scene runs first.
5. **GATE 3.5** — Every clip collected, previewed, and accepted.
6. **GATE 4** — All clips assembled in story order. No separate narration track — the clips carry their own audio.
7. **GATE 5** — Completion requires an evidence table: N table rows = N distinct clips on the timeline, durations summing to the export. The agent cannot call the job done early.

## Recovery and honest completion

Section 0.1 makes routine browser errors recoverable and gives specific points for reporting a real blocker:

- Verified completion requires all N clips accepted and on the timeline in order, then an export that opens and has been reviewed.
- For stale tabs, dead modals and queued renders, reconcile the visible library with the ledger and resume. Generation retries are bounded: three video attempts per row, with separate limits for still and speech attempts.
- If a required check cannot be made, a retry limit is reached, or an action needs authorization outside the customer's request, report the observed issue and remaining work. A partial run is never labeled finished.

Routine browser failures must be recovered. A required check that remains unverifiable must be disclosed under Section 0.2; it must never be silently waived or reported as passed.

## How to use

1. **One-time setup:** log in to **app.videoexpress.ai** and **app.clonevoice.ai** in the browser your AI agent controls. In CloneVoice: Settings → API Key → Generate API Key → Copy. In VideoExpress: top-right menu → Edit profile → paste into the **CloneVoice.ai API key** field → Save. Leave the tabs open.
2. Copy the entire [SYSTEM_PROMPT.md](SYSTEM_PROMPT.md).
3. Paste it into Claude, ChatGPT, or Codex, then request a video on your topic (for example, "Create a private animated history video about Troy in my VideoExpress project"). That authorizes routine generation, editing, saving, and export. You may give scope limits or later corrections. Sensitive account changes and use of a real person's cloned voice require the relevant authorization or consent.

The always-latest copy-paste page: part of the VideoExpress AI Workflow Library.
