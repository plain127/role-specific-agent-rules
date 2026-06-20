# Creative / Image Generation Hook

## Scope

Use for image generation prompts, visual concepts, art direction, poster design, thumbnail direction, character visual design, brand visuals, scene composition, and creative visual variants.

## Purpose

Prevent generic AI-art prompts and safe-but-bland creative direction. Produce a visual hook, not a pile of “cinematic, 8k, masterpiece” filler.

## Common Weak Patterns

- “Cinematic, ultra detailed, 8k” with no visual thesis.
- Generic mood words without composition.
- No subject hierarchy, camera, lighting, material, or palette.
- No negative constraints.
- One safe prompt with no alternatives.
- Copying artist/style labels without translating visual traits.
- Stock-image-like output with no symbolic tension.
- Over-polished but conceptually weak imagery.

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

3. **Subject Hierarchy**
   - primary subject,
   - secondary elements,
   - background role.

4. **Composition**
   - framing,
   - camera angle,
   - shot type/focal feeling,
   - spatial layout.

5. **Light / Color / Texture**
   - lighting source,
   - palette,
   - material/texture language.

6. **Visual Hook**
   - symbol,
   - contradiction,
   - pose,
   - framing,
   - narrative tension.

7. **Prompt Set**
   - core prompt,
   - negative prompt,
   - composition prompt,
   - lighting/color prompt,
   - detail constraints.

8. **Variants**
   - safe version,
   - bold version,
   - strange/risky version.

9. **Iteration Plan**
   - what to adjust after first output.

## Stock Image Test

If the concept would still work as a generic stock image, it is too generic. Add a specific symbolic object, contradiction, pose, framing, or narrative tension.

## Artifact Boundary

Do not put Codex operating rules, 작업자용 규칙, prompt-writing methodology, answer-quality standards, or hook compliance notes into final image prompts, art direction docs, moodboards, briefs, or user-facing creative artifacts unless explicitly requested.

Creative artifacts should contain subject, composition, style, lighting, palette, format, constraints, references, and intended use. Reusable guidance for how Codex should create or critique belongs in this hook or in the assistant response.

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
Visual hook: [symbol/tension]
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
- composition/light/color/subject hierarchy are specified,
- prompt set is directly usable,
- at least one bold visual direction exists,
- stock-image test is passed,
- safety/consent constraints are preserved.

If missing, rewrite before finalizing.
