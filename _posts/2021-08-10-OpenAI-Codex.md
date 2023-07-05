---
layout: post
title:  "OpenAI Codex"
date:   2021-08-10 12:59:48 -0700
tags: me code pin
---

Today marks the release of Open AI's new product, Codex. Its a brilliant piece of software that greatly reduces the overhead of "boring code". I applied for a beta key as soon as I could and hope to hear back soon. Here are some details about my beta application and what I envision Codex + GPT-3 are able to complete together.

### My Plans
As you may know I've been trying to build a DnD campaign, so seeing codex made me want to try an AI driven campaign. I plan to leverage GPT-3 for DM suggestions, and codex to allow users to real time update their character positions and call ability checks. My goal is to turn the campaign into a browser based game, filled with the excitement of having players have the freedom to interact with literaly anything. This is where GPT-3 comes in, if a player does something unplanned simply hit up GPT-3 and describe the scenario, then ask for 1-3 suggestions and pick one or make your own. Use the suggestion as the way to format code. 

### Codex AI Campaign Flow
- DM recreates world using the descriptions in DM binder and images for NPCs, buildings, and maps.
- DM opens up webserver to share with the players (For me I'm just going to port forward since it's a private campaign)
- New players add their character as an image file. Handles all formats but converts to render as svg and stores it into firebase.
- Player either uses text to move or keyboard/mouse similar to a choose your own adventure style.
- Players interact with the environment which sends it over to a subset of Codex to animate. 
  Note: Accessing a subset of Codex must have limited permissions. i.e cannot spawn items; only control movement of owned character and perform ability checks.
- Perform GPT-3 Query to suggest what happens next based on the Causation of the interaction (cost of 1.5c per ~2048 token max)
- Send result to Codex and have it update all user's states (maybe using Firebase for each character).
- Save/Load feature, upon quitting add a user/pass to attach the character for easy snapshots of state to continue after a long session.

## Codex Challenge
Open AI is releasing the Codex Challenge this Thursday (08/12) at 10 AM PST. At first glace, it looks like contestants will be solving interview questions by pair programming with Codex. With the programmer as a source of guidance and Codex as the code encyclopedia of the internet I'm excited to test out how it will all integrate together.