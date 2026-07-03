---
description: Wind down and export this session so a fresh agent can continue cold
argument-hint: "[optional: what to emphasize]"
---

# Export this session

The context is getting bloated, so we're continuing in a fresh session. Finishing the task isn't the point — the point is that a new agent, with none of this conversation in its head, can pick up cleanly from where you are.

So get to a sensible stopping point and make sure the context that matters reaches the next agent. Where it lives is your call: if it's light or one-off, just write it straight into the continuation chip's prompt; if it's substantial or worth keeping, put it somewhere durable (project docs, your memory, a handoff note) and point the chip at it. If it's already written down, don't repeat it. Use your judgment on what's worth capturing and on any light cleanup that makes resuming easier — just don't leave things broken or start new work to round them off.

Then create the continuation chip with the `spawn_task` background-task tool: a self-contained prompt that carries — or points to — everything the next agent needs, and names the next step. If that tool isn't available here, just tell the user where to pick up.

$ARGUMENTS
