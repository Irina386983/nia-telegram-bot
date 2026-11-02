# Nia: keep the AI agent under control

A fairy-tale Telegram game for beginners of any age. AI agents are starting to spend money and act for us, so a human has to stay in control. In Nia you practise exactly that: the agent suggests, YOU decide.

Built at NEAR HACKATHON (1-14 Nov 2026). Solo project.

Bot: https://t.me/IronClawPlaygroundBot

## Try it (do X, see Y)

1. Open the bot and tap START. You see a greeting from Nia, Queen of the Emerald Kingdom, and three buttons.
2. Tap Quick Demo for a 30-second preview, or tap Start Simulation. You see a short situation with three moves: Agree with the agent's plan, Ask the agent to clarify, or Allow a risky shortcut.
3. Tap one move. You see the outcome, a page from the Queen's Notebook with the rule behind it, and her verdict.
4. Tap "What would the AI agent do?". You see a duel: your move against the move of a real AI agent running on NEAR AI Cloud. The Queen comments on who chose better.
5. Tap 📊 Compare Results to see your points, rank and choices, then 🏆 Leaderboard to see the Emerald Leaderboard.
6. Tap Next situation to play another one. There are 12 situations in total.

## Why Nia?

AI agents act on their own. They can be tricked, rushed or simply wrong, so a human has to know when to say "stop, verify first". Nia practises the skill this agent economy needs: a human who stays in control of an agent that handles money.

The AI agent in the duel is a real model. It gets no hints and it can be wrong. That is the point of the game: the agent suggests, the human decides, and the agent's mistakes are the vulnerabilities you learn to catch.

## NEAR technologies used

- NEAR AI Cloud: the duel sends the situation to a model on NEAR AI Cloud (chat completions API, model Qwen/Qwen3.6-35B-A3B-FP8) and shows its decision next to yours.

No other NEAR technology is used in this version.

## How it works

- The bot is built in Make.com (no custom code). `blueprint.json` is the exported scenario.
- Player points, ranks and results are stored in a Make data store.
- The API key for NEAR AI Cloud is kept in Make and is not part of this repository. In `blueprint.json` it is replaced by `YOUR_NEAR_AI_KEY`.
- If the AI call fails, the player sees a polite message and the owner gets an alert.

## Before / during the hackathon

Before 1 Nov 2026 (the baseline, see `BASELINE.md`, tag `pre-hackathon`): the idea and an early Telegram prototype with 8 situations, three moves, the Queen's verdicts, points and ranks.

Built during the hackathon (from 1 Nov 2026):

- The AI duel: the player's move is compared with a real AI agent on NEAR AI Cloud, with a reference answer for each situation and the Queen's comment.
- 4 new situations (9 to 12), 12 in total, each with its own Notebook page, outcomes and points.
- Points that depend on the situation, so asking is not always the best move.
- Error handling for the AI call.
- Updated Compare Results texts.

## Origin

Nia grows out of my idea "IronClaw Playground: Sandbox Agent Simulation", which was approved in the NEAR Builder Visionary programme. I keep building it along my own roadmap.

## Roadmap

- More situations, then harder branching levels for experienced AI users.
- Try other agents as the opponent in the duel, including IronClaw, which is now part of Near.com. For this hackathon the duel uses a model on NEAR AI Cloud because it is stable and reproducible.

## Notes

Nia is an independent community project, not an official NEAR or IronClaw product. Music in the demo video: "Music by Roman Orekhov from Pixabay".

License: MIT.
