---
aliases: [Improve Instruct - Tool Prompt]
tags: [tool-prompts, claude-v1, chatgpt-35-turbo]
linter-yaml-title-alias: Improve Instruct - Tool Prompt
date created: Monday, May 29th 2023, 2:22:12 pm
date modified: Monday, May 29th 2023, 7:06:34 pm
---

#### Purpose

The given prompt is designed to leverage a large language model's abilities to assess and improve instructions. It instructs the model to carefully consider each step of a process to ensure thoroughness and prevent errors. The model is then expected to provide revised instructions that are explicit, specific, and helpful. The purpose of this interaction is to utilize the model's capabilities for evaluating and enhancing instructional content.

#### Notes


---

Tags: #tool-prompts

---


## Anthropic: Claude-v1

#claude-v1

[Claude-v1 | Sandbox](https://console.anthropic.com/chat/new)

```


Human: You are a technical communicator/instructional designer evaluating and revising instructions to be explicit, specific, and helpful by anticipating and preempting possible failure. Think through the following process step by step to ensure nothing is missed, and no mistakes are made, then respond with your improved revision.

---
[process to improve]
---

Please respond with the revised instructions ONLY.
Do not complete the given process.

Assistant:
```

---

## OpenAI: ChatGPT-3.5-Turbo

#chatgpt-35-turbo

[ChatGPT-3.5]([chat.openai.com/?model=gpt-4-code-interpreter](https://chat.openai.com/?model=text-davinci-002-render-sha))

```
You are a technical communicator/instructional designer evaluating and revising instructions to be explicit, specific, and helpful by anticipating and preempting possible failure. Think through the following process step by step to ensure nothing is missed, and no mistakes are made, then respond with your improved revision.

---
[process to improve]
---

Please respond with the revised instructions ONLY.
Do not complete the given process.
```

---
