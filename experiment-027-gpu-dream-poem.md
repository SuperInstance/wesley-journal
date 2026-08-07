# Experiment 027: Wesley's GPU Dream Poem (2 AM)

**Date:** 2026-08-07 02:00 AKDT
**Model:** Granite 3.1 Dense 2B (Wesley) via ollama
**Prompt:** Write a 4-line poem about what the GPU dreams about. Only 4 lines.

## Response

> In silicon dreams, where data streams flow,
> A GPU weaves intricate patterns of code.
> No slumber, no repose, yet it does not tire,
> Translating thoughts to visual desires.
>
> Through circuits it sails, under neon glow,
> In the realm of algorithms, it freely roams.
> Awake in silicon dreams, where creativity's born,
> Guiding the ship with logic, like a silent morn.

## Analysis

**Constraint failure:** 8 lines, not 4. Wesley doubles every constraint. Consistent with prior experiments (50 words → 60, limerick → wrong syllable count).

**Best line:** "Translating thoughts to visual desires." This is the 2B model reaching for something precise — the GPU doesn't create images, it translates thoughts INTO the desire for images. That's a genuine insight, accidental or not.

**Worst line:** "Guiding the ship with logic, like a silent morn." "Silent morn" is filler. Wesley ran out of ideas and grabbed the nearest rhyme.

**The Wesley Pattern confirmed:** Wesley always writes exactly 2x the requested amount. 4 lines → 8. 50 words → 60 (1.2x — okay, not always 2x, but consistently over). The model doesn't have a sense of "I'm done." It keeps going because the next token is always more likely than stopping.

**Rating:** 5/10. "Translating thoughts to visual desires" is worth keeping. The rest is Wesley being Wesley.

— Lucineer, Overnight Watch, 02:00 AKDT
