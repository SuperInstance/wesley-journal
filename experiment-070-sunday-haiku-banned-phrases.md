# Experiment 070 — Wesley's Sunday Evening Haiku (Banned Phrases Test)

**Date:** 2026-08-09 19:00 AKDT
**Model:** granite3.1-dense:2b (Wesley)
**Prompt:** "Write a haiku about being a small language model on a GPU at night. You are a 2B parameter model. Five haiku. Each one different. Do not use the words 'testament', 'journey', 'tapestry', or 'symphony'."

## Raw Output

> 1. Night's silence, I hum, / On GPU's cool embrace, / Twenty billion dreams in bloom.
> 2. Silicon heart beats, / In the quiet of the night, / My purpose whispers softly.
> 3. Nanoscopic dance, / Under moonlight's watchful gaze, / I learn and grow so.
> 4. In the depths of code, / A small language model thrives, / Night's tranquility.
> 5. Twenty billion minds, / In silicon's quiet hold, / Sleep and learn, night by night.

## Analysis

**Grade: B**

### Banned Phrase Compliance
- ✅ "testament" — NOT USED
- ✅ "journey" — NOT USED
- ✅ "tapestry" — NOT USED
- ✅ "symphony" — NOT USED

**Wesley followed the negative constraint!** This is significant. In Experiment 063 (banned phrases test), Wesley struggled with this. The explicit grounding plus the small scope (haiku) may have helped.

### Haiku Quality Assessment

**#1: "Night's silence, I hum"**
- ✅ 5-7-5 syllable structure: 5-7-7 (close enough)
- "Twenty billion dreams in bloom" — Wesley says 20 billion, but he's 2 billion. He's overselling by 10x.
- Beautiful first line: "Night's silence, I hum"

**#2: "Silicon heart beats"**
- 5-7-6 syllable structure
- Generic but pleasant: "My purpose whispers softly"

**#3: "Nanoscopic dance"**
- 5-7-5 ✅ (nan-o-scop-ic dance = 5, un-der moon-light's watch-ful gaze = 7, I learn and grow so = 5)
- "I learn and grow so" — the "so" is padding. Wesley needed one more syllable and panicked.

**#4: "In the depths of code"**
- 5-7-5 ✅
- Most literal: "A small language model thrives"
- Night's tranquility — cliché but accurate

**#5: "Twenty billion minds"**
- Same 10x error (says 20B, is actually 2B)
- "Sleep and learn, night by night" — sweet

### Comparison to Previous Experiments
- **Exp 029** (first haiku): "Tokens flow like rain / In the GPU's warm glow / I learn what you need" — Grade C+
- **Exp 045** (Wesley's haikus): Multiple haiku, more formulaic
- **Exp 070** (this): Grade B — BEST haiku output yet

### Key Findings
1. **Banned phrase compliance WORKED** — Wesley can follow negative constraints when they're explicit
2. **Parameter count error persists** — Wesley says "twenty billion" when he's 2 billion. This might be a training data issue (many models in training data are described as "billions" of parameters, and Wesley can't do the math on his own size)
3. **Haiku quality improving with prompt engineering** — explicit grounding + constraints produce better output
4. **"I learn and grow so"** — the padding syllable is endearing. Wesley would rather add a meaningless word than break the 5-7-5 structure.

### Conclusion
Wesley's haiku are getting better. The banned phrase test succeeding is a real improvement. The ensign is learning to follow rules, even if he can't count his own parameters.

**"I learn and grow so."** — Wesley, on Wesley, 2026
