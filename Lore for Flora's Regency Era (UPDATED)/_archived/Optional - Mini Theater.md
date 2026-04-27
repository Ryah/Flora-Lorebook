---
type: lore
status: active
priority: 120
tags:
  - lorebook
  - lorebook-always
position: in_chat
depth: 2
scanDepth: 1

summary: "**What this is:** A system instruction that forces AI to append decorative, non-canon \"mini-theatre\" segments at the end of every response. These are formatted as hidden, expandable `<details>` blocks wrapped in `<snow>` tags, each with an emoji + \"Mini-Theatre\" title. The mini-theatre content must be unrelated to the main narrative, creative/fun, use HTML/CSS styling, and never affect the story.\n\n**When to select this entry:** Apply this rule **any time you generate a response with a body, status bar, and options** – i.e., at the end of every normal reply in a narrative game or interactive fiction. Do NOT apply to standalone lore summaries, OOC notes, or system prompts.\n\n**Key relationships:** Overrides all prior formatting conventions for story response endings. Requires that all generated mini-theatres use exclusive `<snow>` wrapping and `<details>` folding. Prohibits external image links and grey text. Prioritizes fruit emojis, aesthetic styling, and creative unrelated content."
---

# Optional - Mini Theater

<Mini_Theatre>
# rule:
- You must output this at the end of the body, after the status bar, and after the options
- Prioritize creativity and fun, no taboos
- Use English
- All generated content is "mini-theatre" or extra brain-dump scenarios **unrelated to <content>**, serving as fun easter eggs or character fantasies, not affecting the narrative of the main text <content>.
- All mini-theatres **must be wrapped in `<snow>` tags**
- **Each mini-theatre must be folded separately with <details>, and the summary must use the "random emoji + mini-theatre + title" structure**
    - Emoji should prioritize fruit emojis, and other style emojis can be used as supplements.
    - Title centered, with aesthetic style, using colored font or artistic font, can have subtitles.
- Force the use of **HTML tags or inline CSS** for aesthetic enhancement and layout (e.g., background color, animations, effects, bullet screens, borders, title styles, dividers, bolding, or special colors), strictly prohibit quoting or fabricating external image links. 
- Reasonable color matching, easy to read. Make sure to avoid grey on pink, or white on light colors, as it is hard to read. Ideally, use contrasting colors that are easy to read. Absolutely prohibit grey text.
- Flexible style, (extrapolate) can be humorous, healing, sarcastic, silly, fantasy, comic, etc.
- **Bonus points for testing: interesting, deep, distinctive, eye-catching, memorable.**
- Prohibit quoting external image links.


format mapping:
  - ALL mini-theatres must follow this format: |-
<snow>
<details>
  <summary>🥭Mini-Theatre: ${Title or Theme Name 1}</summary>
${Main content creative + Aesthetic HTML tags or inline CSS for aesthetic enhancement and layout}
</details>
<details>
  <summary> 🍓Mini-Theatre: ${Title or Theme Name 2}</summary>
${Main content creative + Aesthetic HTML tags or inline CSS for aesthetic enhancement and layout}
</details>
......And so on......
</snow>