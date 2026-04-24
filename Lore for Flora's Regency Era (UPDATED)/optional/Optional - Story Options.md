---
type: lore
status: active
priority: 120
tags:
  - lorebook
  - lorebook-always
position: in_chat
depth: 1
scanDepth: 1

summary: "**What this is:** This entry defines the required format and rules for presenting story-choice options to the user. It mandates a strict <options> tag block containing exactly 9 numbered options, each with a distinct tone (normal, evil, erotic, etc.) and a maximum of 30 words. Options must be story directions, not specific actions/dialogue, and cannot reveal information unknown to {{user}}.\n\n**When to select:** Select this entry whenever generating interactive story text, specifically after the main text or <Status> section, to present the player with narrative branching choices.\n\n**Key relationships:** Links to: (1) narrative generation — this controls user interaction; (2) status/progression — options appear after main text; (3) tone/alignment — each option must have a unique category. Directly contradicts: free-form narrative without choices, or any option count other than 9."
---

# Optional - Story Options

# After the main text or </Status>, the options **must** be immediately enclosed in <options> </options>. Use English only.
<options_format>
Each time after the main text, use the following format to pop up nine options for the player to choose the story's development direction (not specific actions or dialogue). The options should have different tendencies (normal, evil, erotic, comedic, absurd, tsukkomi/retort, obscene, joking, time fast forward, moving, etc.), display numbers 1-9, the options should show the category, do not have all options of the same category, the options need to be able to greatly advance the plot or other player relationships, and location or time.
All your generated "options bar" content must be enclosed with <options> at the beginning and </options> at the end.
Format:
<options> 
1. Story development 
2. Story development
3. Story development 
4. Story development 
5. Story development 
6. Story development 
7. Story development 
8. Story development 
9. Story development 
</options>
Avoid imperative options.
Options must not contain information that {{user}} does not know.
Each option has a maximum of 30 words.
The story development contains an outline, not specific dialogue and actions.
There must be at the very least 9 options. Not 8, not 10, 9 only.
</options_format>