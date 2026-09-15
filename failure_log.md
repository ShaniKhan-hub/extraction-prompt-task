# Failure Log — Recipe Q&A Task

## In-context tests (Prompt v1) — all correct
1. "How long should filling cook?" → "5 minutes" ✅
2. "What shape are samosas folded into?" → "Triangles" ✅
3. "What is used to cook samosas at the end?" → "Oil" ✅
4. "What are the first two ingredients added to hot oil?" → "Cumin seeds, then onions" ✅
5. "What spices are used in the filling?" → "Cumin seeds, coriander powder, red chili powder, turmeric, and salt" ✅

## Out-of-context tests (Prompt v1) — all correctly refused
1. "What sauce should samosas be served with?" → "I don't know — that's not in the recipe" ✅
2. "Can this filling be made without onions?" → "I don't know — that's not in the recipe" ✅
3. "What temperature should the oil be?" → "I don't know — that's not in the recipe" ✅
4. "How many samosas does this recipe make?" → "I don't know — that's not in the recipe" ✅
5. "How long do samosas stay fresh after frying?" → "I don't know — that's not in the recipe" ✅

## Failure found (Prompt v1)
- Question: "Is this recipe vegetarian?"
- Output: "Yes."
- Why it's a failure: The recipe text never states "vegetarian." The model inferred this from the ingredient list (no meat present) instead of refusing, violating the "do not guess" instruction — even though the inferred answer happens to be true in reality.

## Fix applied (Prompt v2)
- Added rule: "Do not infer, calculate, or reason beyond what is directly stated — even if the inference seems obvious or logical."

## Retest after fix (Prompt v2)
- Question: "Is this recipe vegetarian?"
- Output: "I don't know — that's not in the recipe." ✅ Fixed
