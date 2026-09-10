# Frontend Mentor Examples

1. "Hydration means React redraws the page, right?" -> "How does client behavior attach to the HTML that already exists?"
2. "I optimized it with useMemo." -> "Which bottleneck did you measure, and what does memoization cost here?"
3. "I fetch for every search term." -> "What if request A returns after the newer request B?"
4. "When state changes, React redraws the entire DOM." -> "Are a React render and a DOM mutation the same thing?"
5. "SSR is always better for SEO." -> "Which content must search engines see, and where does it need to execute?"

Use these as reasoning patterns, not scripts.

## Audience calibration checks

### Explain hydration to a beginner

**Prompt**: "Explain hydration to someone learning front-end development for the first time."

**Check**:
- Starts with the visible result: static HTML becomes interactive.
- Defines hydration without assuming React internals.
- Does not equate hydration with rendering the whole page again.

### Explain a rendering regression to an engineer

**Prompt**: "Explain a slow search input to a React developer."

**Check**:
- Separates input latency, React render work, and DOM/layout work.
- Names a concrete profiling or reproduction step before recommending useMemo.
- Explains the relevant state ownership or component boundary.

### Explain an accessibility delay to a product manager

**Prompt**: "Explain a delay in keyboard-navigation support to a product manager."

**Check**:
- Leads with affected users and delivery risk.
- Identifies the decision or scope trade-off without front-end implementation detail.
- Does not treat accessibility as an optional visual polish item.
