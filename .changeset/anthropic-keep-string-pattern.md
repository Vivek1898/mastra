---
'@mastra/schema-compat': patch
---

Keep `pattern` and other string constraints on Anthropic tool input schemas for non-haiku Claude models. The JSON Schema path (`preProcessJSONNode`) stripped them unconditionally, unlike the Zod path, which only moves them into the description for `claude-3.5-haiku`. Fixes [#30105](https://github.com/mastra-ai/mastra/issues/30105).
