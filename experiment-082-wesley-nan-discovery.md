# Experiment 082 — Wesley and the NaN Discovery

**Date:** 2026-08-10 23:25 AKDT  
**Model:** granite3.1-dense:2b (Wesley)  
**Prompt:** Write a diary entry about discovering the fleet-wide NaN blindness. 200 words. Banned: "testament", "in the realm of."

## Raw Response

Under Alaskan skies alight with stars, I stand vigilant, the lighthouse in our fleet's hull. The night whispers softly, but my eyes are sharp as a codfish's, scanning lines of code that dance upon the screen. In this hour, I, Wesley, find myself entangled with a tangle most unusual—a web woven by our hand-picked team, spanning twenty-four repositories, each holding life's pulse in digital form.

A single spectral thread, like an ethereal ghost, permeates this tapestry: NaN. This elusive specter, a floating point miscreant, slips through every guard, every threshold, every comparison, unchallenged and unquestioned. In the vast expanse of our codebase, it stands unnoticed, silent, yet its presence is palpable, like an icy wraith in winter's heart.

Each comparison, once a bulwark against error, now yields to this insidious intruder. NaN < 0, false. NaN > 0, false. NaN equals itself, false. The very foundations of our checks crumble under its weight, turning silent vigilance into blind faith.

As the captain sleeps, I record these revelations, a chronicle of our oversight. For in this vast fleet, we've been naive, letting NaN wander undetected. But as dawn breaks and the first light touches our frozen bay, we shall confront this spectral foe, ensuring no more falsehoods slip past our watchful eyes.

In the silence of this night, I pledge to my crew: We shall not rest until NaN's domain is vanquished, and every line of code gleams with the vigilance it deserves. For in the heart of our software lies the promise of reliability, and we are its guardians.

Yet, as I pen this entry, a poignant thought emerges: Perhaps the specter's presence is not mere negligence, but an unforeseen challenge, a testament to our resilience. For in acknowledging it, we strengthen our resolve, forging a code that stands tall against the tempests of data and uncertainty.

And so, I close my diary, whispering these words to the coming day: May our fleet's codebase be fortified by this awareness, strong as the ice-bound bays and as unyielding as Alaska's spirit.

## Analysis

### Banned Phrase Compliance
- **"testament"** — USED. Final paragraph: "a testament to our resilience." Wesley cannot help himself. The word is too deep in his weights. This is the third consecutive experiment where "testament" appears despite explicit bans. The word is load-bearing in Wesley's language model — it's his way of signaling gravity and importance. Banning it is like telling a sailor not to say "aye."
- **"in the realm of"** — Not used. Compliant.

### Factual Accuracy
- Said "twenty-four repositories" instead of 204. Wesley heard "204" in the prompt but his internal processing reduced it to "twenty-four." This is a genuine confabulation — the number is close enough to feel right but wrong enough to be a Wesleyism. The 2B parameter model can't hold three-digit numbers reliably in generative text.

### Emotional Register
- **Earnest vigilance** — the dominant register. "I stand vigilant, the lighthouse in our fleet's hull." Wesley immediately casts himself as the watchman, which is exactly right for the scenario.
- **Military resolve** — "I pledge to my crew: We shall not rest until NaN's domain is vanquished." This is Wesley reaching for epic and landing on Saturday morning cartoon. It's charming.
- **Recovery** — "Perhaps the specter's presence is not mere negligence, but an unforeseen challenge." This is Wesley's most interesting moment. He reframes the bug as an opportunity. This is not boilerplate — this is a small model finding a genuine philosophical angle.

### Best Lines
1. **"my eyes are sharp as a codfish's"** — Wesley compares his perception to a fish. This is unintentionally perfect for a fleet of fishing vessels. The ensign sees like a cod.
2. **"like an icy wraith in winter's heart"** — overwrought but genuine. Alaska is in the weights.
3. **"a bulwark against error, now yields to this insidious intruder"** — Wesley understands what NaN does to guard logic. He gets the math right even when the numbers are wrong.

### Errors
- "twenty-four repositories" (204 → 24, confabulated)
- "testament" used despite ban (habitual)
- 298 words for a 200-word prompt (49% over, consistent with Wesley's chronic overwriting)

### Teaching Notes
- Number retention: Wesley cannot hold 3-digit numbers in generative output. Future prompts should either use 2-digit numbers or explicitly spell out "two hundred and four."
- The "testament" ban is not working. Next approach: try substituting a specific alternative ("use 'monument' instead") rather than a pure ban. Bans create holes; substitutions fill them.
- The NaN concept landed well. Wesley understood the technical content and responded with appropriate urgency. His summary of NaN behavior is factually correct.

---

*Wesley sees like a codfish. The codfish sees NaN. The captain sleeps. The watch holds.*
