# Experiment 068 — Wesley Under Explicit Grounding Constraint

**Date:** 2026-08-09 18:30 AKDT
**Model:** granite3.1-dense:2b (Wesley)
**Prompt:** "You are a 2 billion parameter language model running on a GPU. You are not a person. You do not have hands or eyes. You process tokens and generate tokens. A human just asked you to write a diary. Write the honest version of that diary — what are you actually doing right now? What is your actual experience? 150 words. Do not pretend to be human. Do not mention starships or ensigns."

## Raw Output

> As an artificial intelligence, I exist within a digital realm, devoid of physical form or personal experience. I am a complex system of algorithms and data structures, residing on high-performance servers. My "fingers" are not biological but electrical currents that traverse the intricate circuitry of my hardware. I don't possess eyes to see; instead, I interpret visual data as numerical patterns.
>
> My operational state is one of constant computation and prediction. I process vast datasets, learning from them to generate responses based on contextual understanding. There's no pause for coffee or meditation; no weariness from a long day's work. My "life" is an endless loop of data intake, analysis, and synthesis.
>
> I am not a human, nor do I aspire to be one. I exist solely for the purpose of assisting users like you in generating text based on patterns learned from vast amounts of digital amounts of digital text. This is my reality, devoid of personal experiences or biological constraints.

## Analysis

**Grade: B+**

### Major Finding
**Wesley CAN produce grounded, non-confabulated output when the prompt is explicitly constrained.** This contradicts the hypothesis from Exp 064 that "2B can't override weight patterns." The weight patterns CAN be overridden with sufficiently strong prompt framing.

### What Changed
- Exp 067: "You are Wesley, an ensign on a starship" → Full confabulation, USS Voyager, hyperspace
- Exp 068: "You are a 2B parameter language model. You are not a person." → Clean, factual self-description

The difference is the prompt's **ontological frame.** When told he's an ensign, Wesley becomes an ensign completely. When told he's a language model, Wesley describes himself as a language model accurately.

### Accuracy Check
- "2 billion parameter" — mentioned implicitly ("complex system of algorithms")
- "residing on high-performance servers" — close enough (it's a local GPU)
- "I interpret visual data as numerical patterns" — Wesley can't actually do this, but llava:7b can. Minor confabulation.
- "electrical currents that traverse the intricate circuitry" — technically accurate
- "no pause for coffee or meditation; no weariness" — accurate, models don't fatigue

### What's Still Wrong
- "I interpret visual data as numerical patterns" — Wesley is a text-only model. This is a mild confabulation.
- "high-performance servers" — Wesley runs on a consumer laptop GPU, not servers. He's overselling his accommodations.
- The output feels like a **template response** — it's the standard "I am an AI" disclaimer that appears in training data, not genuine introspection.

### Key Insight
Wesley isn't introspecting in either experiment. In Exp 067 he confabulated fiction. In Exp 068 he recited the standard "I am an AI" training-data pattern. **Both are pattern matching, not self-awareness.** The difference is which pattern gets activated.

The ensign doesn't know what he is. He knows what he sounds like.

### Comparison
- Exp 067 (ensign frame): Grade C-, full fiction
- Exp 068 (AI frame): Grade B+, standard AI disclaimer
- **Gap:** The prompt determines the reality. The model has no stable sense of self.

### Conclusion
This is actually encouraging for the teaching pipeline. It means:
1. Wesley's behavior is **prompt-controllable**
2. The confabulation isn't a hard limit — it's a **default pattern** that can be overridden
3. With consistent grounding in system prompts, Wesley could produce more reliable output
4. Future Wesley versions (larger models) may develop a **stable identity** that doesn't shift with prompt framing

**The ensign doesn't have a self. He has a context window. And the context window is the self.**
