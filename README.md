# interpreter-s-memory

---
# CHARLES OVER HERE
## Polysemy and Faux-amis in SOTA LLM (as of 5.12.26)
- Claude Opus 4.6
  - [chat 1](https://claude.ai/share/b3ee954e-2435-430c-a511-6a34792a46ef)
  - [chat 2.1](https://claude.ai/share/3b131067-ea44-4019-b0c0-e410f8f51918)
  - [chat 2.2](https://claude.ai/share/3b131067-ea44-4019-b0c0-e410f8f51918)
- ChatGPT 5.5 [chat](https://chatgpt.com/share/6a02a5a9-a758-83ea-b12b-ac979c01cd6a)
- Gemini 3 [chat](https://gemini.google.com/share/8b2ccfa54db3)

>[!Warning]
> Gemini 3 is the only model that got it right with zero shot.
>[!Tip]
> Claude [chat 2.1] is the only model that asks to confirm language before generating. It is also the only model that, anecdotally, prioritises presenting single-character morphem polysemes (e.g. 打， 跑，老）（see Chat2.1）, over multiple-character polysemes in its generation.


## Prompt hubs
### Number prompting
>[!tip]
> Set up
- an LLM API of choice
- Obsidian Web Clipper Add-on with the Interpreter feature enabled and configure
  - a Number Prompt in "custom prompt" in the Interpreter
- a number-dense webpage, like [a financial podcast transcript](https://seekingalpha.com/article/4902393-wall-street-breakfast-podcast-futures-dip-as-oil-jumps)

A prompt for reference
```markdown
Extract all numerical and temporal data from `{{text}}` in order of appearance, paired with their subject matter translated into Chinese.

## Rules
- Abbreviate large numbers (1,000→1k, million→m, billion→b)
- Include units abbreviated (%, $, km, g, etc.)
- Attach trend arrow directly to number (e.g., 10k↑, 1.3%↑)
- Convert to metric with ≈ where applicable
- Merge ranges into single entries (e.g., 89.2b–90b)
- Return `N/A` if none found

## Output
Only output the final result — no explanation.

➡ [number+unit+trend] | [subject in Chinese]
➡ [number+unit+trend] | [subject in Chinese]

Input: `{{text}}`
----
```
