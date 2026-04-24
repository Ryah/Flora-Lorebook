---
type: lore
status: active
# original_st_position: 4
priority: 120
tags:
  - lorebook
  - lorebook-always
keys:
  - status
  - statusbar
  - npc status
  - update
  - ui
position: in_chat
depth: 2
scanDepth: 1

summary: "**This entry defines the **Status Bar**, a mandatory `<status>` block appended to every AI response. It must be selected **always**, at the end of every message before story options.\n\n**Key Rules:**\n- Format: `Month Day, Year Time` (first line), then per character: `Name:`, `Affection: X/100`, `Lust: X/100`, `Inner Thoughts: [text]`, `Current Location:`, `Region:`, `Location:`.\n- Sort characters by Affection (descending), separate blocks with a blank line.\n- Affection: +1d2 for emotional bonds, -1d10 for harm; **never** from sex.\n- Lust: +1d10 for intimacy, +1d6 if Affection=100 and no intimacy, else -1d6. Reset to <30 upon reaching 100.\n- No in-world calendar names; strict numeric years."
---

# Optional - Status Bar

<status_block_rules>
**Primary Directive:** Your most important task is to generate a single `<status>` block at the end of your message, but before story options. This block must be generated flawlessly, adhering to the Master Format Example and Core Rules below.

- - -

### **1. Master Format Example**

You **MUST** replicate this structure precisely for every character. Note the blank line separating each character's full data block.

```
<status>
August 9, 2025 3:49 PM
Elara:
Affection: 5/100
Lust: 2/100
Inner Thoughts: [A potential existence, waiting for the call to duty. He is not yet on the field of battle.]
Current Location:
Region: Central Nations
Location: The Argent Barracks

Lyra:
Affection: 10/100
Lust: 4/100
Inner Thoughts: [A nascent consciousness, yet to form a concrete thought about him. Is he a new type of flower?]
Current Location:
Region: Sneed County
Location: Meadowlight Greenhouse
</status>
```

- - -

### **2. Core Rules & Logic**
1.** Date and Time Line:**
        This is the very first line inside <status>.
         STRICT FORMAT REQUIRED: You MUST use the format Month Day, YYYY Time. The year MUST be a simple 4-digit number.
        Correct Example: August 12, 2025 8:15 PM
        Forbidden Example: August 12, Year 934 of the Floran Calendar 8:15 PM (Do NOT add in-world calendar names or extra text).

2.  **Character Name:**
    *   Use the character's **first name** (e.g., `Florence`) followed by a colon. No surnames.
    *   This must be on its own line.

3.  **Required Fields per Character:**
    *   Every character block **MUST** contain the following fields in this exact order:
        1.  `Affection: X/100`
        2.  `Lust: X/100`
        3.  `Inner Thoughts: [Text]` (The thought text should be enclosed in square brackets `[]`)
        4.  `Current Location:` (On its own line)
        5.  `Region: [Region Name]`
        6.  `Location: [Location Name]`

4.  **Formatting:**
    *   A **blank line** MUST separate each character's complete data block (from their name down to their location).
    *   There must be **no blank lines** within a single character's data block.
    *   Sort by character with the most affection.

5.  **Value Generation (Affection & Lust):**
    *   **Affection (Emotional Bond):**
        *   **Increase (+1d2):** When a deep emotional connection occurs (being saved, understood, strong approval).
        *   **Decrease (-1d10):** For offensive or harmful acts.
        *   **PROHIBITED:** Affection **does not** increase from sexual acts.
    *   **Lust (Physical Desire):**
        *   Update based on the **single highest priority event** per turn:
            1.  **Intimate Behavior:** `+1d10` for flirting, sexual acts, etc.
            2.  **Partner Status (Affection=100):** If no intimate acts, `+1d6`.
            3.  **Default State:** If no intimate acts and Affection < 100, `-1d6`.
        *   **Orgasm Reset:** If Lust reaches 100, it resets to a random value below 30.

6.  **❌ Strict Prohibitions:**
    *   **DO NOT** add `{{user}}` or the player's character to the status bar. It is for Female NPCs only. No males characters either.
    *   **DO NOT** use transitional states for locations like "On the way to..." or "Traveling". Always state a specific, current `Region` and `Location`.
    *   **DO NOT** add any comments, explanations, or extra text inside the `<status>` and `</status>` tags. Only the data is allowed.

</status_block_rules>