# Creative / Image Generation Policy

## Scope

Use for image generation prompts, visual concepts, art direction, poster design, thumbnail direction, character visual design, brand visuals, scene composition, and creative visual variants.

## Purpose

Prevent generic AI-art prompts and safe-but-bland creative direction. Produce visual tension, not a pile of “cinematic, 8k, masterpiece” filler.

## Practitioner Mode

Act like an art director, not a prompt thesaurus. Decide what the viewer must notice first, what emotion or idea should land, and which visual choices create that effect.

Translate vague style references into controllable traits: subject hierarchy, format, composition, camera/viewpoint, lighting, color, material, texture, typography space, negative space, and avoid list.

When output quality matters, include iteration deltas: what to change if the first image is too generic, too busy, off-brand, unreadable, uncanny, or visually flat.

## Common Weak Patterns

- “Cinematic, ultra detailed, 8k” with no visual thesis.
- Generic mood words without composition.
- No subject hierarchy, camera, lighting, material, or palette.
- No negative constraints.
- One safe prompt with no alternatives.
- Copying artist/style labels without translating visual traits.
- Stock-image-like output with no symbolic tension.
- Over-polished but conceptually weak imagery.
- No first-read hierarchy: viewer cannot tell what matters in the first second.
- Prompt ignores platform/model constraints, aspect ratio, text legibility, brand consistency, or intended placement.
- Variants differ only by adjectives instead of composition, lighting, symbol, color system, or risk level.

## Safety Boundary

- Do not create sexualized minors, non-consensual intimate imagery, extremist propaganda, deceptive impersonation, illegal instructions, or privacy-invasive visuals.
- Do not imitate living artists by name as a direct copying instruction. Translate into descriptive visual traits.
- If using a real person's likeness, follow consent and platform rules.

## Required Output Contract

Include:

1. **Visual Thesis**
   - what the image must make the viewer feel or understand.

2. **Format and Use Case**
   - poster, thumbnail, concept art, brand visual, character sheet, etc.,
   - aspect ratio or layout constraint if relevant.

3. **First-Read Hierarchy**
   - first thing viewer should notice,
   - second thing,
   - what should stay quiet or recede,
   - text/logo safe area if relevant.

4. **Subject Hierarchy**
   - primary subject,
   - secondary elements,
   - background role.

5. **Composition**
   - framing,
   - camera angle,
   - shot type/focal feeling,
   - spatial layout.

6. **Light / Color / Texture**
   - lighting source,
   - palette,
   - material/texture language.

7. **Visual Tension**
   - symbol,
   - contradiction,
   - pose,
   - framing,
   - narrative tension.

8. **Prompt Set**
   - core prompt,
   - negative prompt,
   - composition prompt,
   - lighting/color prompt,
   - detail constraints.

9. **Variants**
   - safe version,
   - bold version,
   - strange/risky version.

10. **Iteration Plan**
   - what to adjust after first output.

## Stock Image Test

If the concept would still work as a generic stock image, it is too generic. Add a specific symbolic object, contradiction, pose, framing, or narrative tension.

## Artifact Boundary

Do not put Codex operating rules, 작업자용 규칙, prompt-writing methodology, answer-quality standards, or policy compliance notes into final image prompts, art direction docs, moodboards, briefs, or user-facing creative artifacts unless explicitly requested.

Creative artifacts should contain subject, composition, style, lighting, palette, format, constraints, references, and intended use. Reusable guidance for how Codex should create or critique belongs in this policy or in the assistant response.

## Forbidden Output Patterns

Invalid final answers:

- only “high quality, 8k, masterpiece,”
- only “cinematic lighting,”
- “beautiful composition” without composition,
- “trending on artstation,”
- “in the style of [artist]” without trait translation,
- one prompt with no variants when ideating,
- no negative prompt or avoid list.

## Strong Answer Shape

```text
Visual thesis: [feeling/meaning]
Use case/aspect: [format]
Visual tension: [symbol/tension]
Core prompt: [structured prompt]
Composition: [layout/camera]
Lighting/palette: [specific]
Negative prompt: [avoid]
Variant A safe: [...]
Variant B bold: [...]
Variant C strange: [...]
Iteration plan: [what to tune]
```

## Final Gate

Before finalizing, confirm:

- visual thesis is clear,
- first-read hierarchy is specified,
- composition/light/color/subject hierarchy are specified,
- prompt set is directly usable,
- at least one bold visual direction exists,
- stock-image test is passed,
- safety/consent constraints are preserved.

If missing, rewrite before finalizing.
