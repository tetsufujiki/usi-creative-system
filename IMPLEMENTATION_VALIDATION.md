# IMPLEMENTATION VALIDATION

## Purpose

This file provides an implementation-facing validation process
for the United Studio Creative System.

It is a companion
to 07 — IMPLEMENTATION CONTRACT.

It does not replace:

- project tests.
- framework documentation.
- accessibility standards.
- performance tooling.
- human review.

Use this document
before implementation,
during implementation,
and before release.

## VALIDATION STATUS

Each item may use:

```text
NOT REVIEWED
PASS
FAIL
NOT APPLICABLE
DOCUMENTED EXCEPTION
```

A documented exception must include:

- reason.
- scope.
- impact.
- review condition.

---

# 01 — CONTEXT

## Project Context

- [ ] The project purpose is documented.
- [ ] The intended audience is known.
- [ ] The primary perceptual change is defined.
- [ ] Relevant Creative Principles are identified.
- [ ] Project-specific constraints are documented.
- [ ] Supported browsers and devices are defined.
- [ ] Content and asset sources are known.
- [ ] Project-specific exceptions are documented.

## Source of Truth

- [ ] Relevant Core documents were reviewed.
- [ ] The current Component Registry was reviewed.
- [ ] The current Composition Pattern Registry was reviewed.
- [ ] Project-specific documents do not silently contradict the Core System.
- [ ] Machine-readable Tokens match their documented semantic roles.

---

# 02 — EXPERIENCE

## Moment

- [ ] Each perceptual frame has one Dominant Moment.
- [ ] The intended change in perception can be stated.
- [ ] Supporting elements do not compete equally.
- [ ] The Moment has a perceptible beginning.
- [ ] The Moment becomes stable before the next one dominates.
- [ ] Expression without a clear role has been removed.

## Attention

- [ ] The Attention Anchor is identifiable.
- [ ] The Focus is clear.
- [ ] Supporting content follows the Focus.
- [ ] Strong visual elements do not compete.
- [ ] The Attention Budget remains controlled.
- [ ] Stillness is used where meaning needs time.

## Continuity

- [ ] Each major section builds from what came before.
- [ ] Transitions have perceptible cause.
- [ ] Meaning continues without unnecessary repetition.
- [ ] Pattern changes do not feel like unrelated page fragments.
- [ ] The experience reaches an appropriate Release.

---

# 03 — PATTERNS

## Pattern Selection

- [ ] Each Pattern has a defined Intent.
- [ ] Each Pattern has a Starting State.
- [ ] Each Pattern creates a perceptual change.
- [ ] The Primary Moment is identified.
- [ ] The Completion Condition is understood.
- [ ] The selected Pattern is not merely a fixed layout.

## Pattern Sequence

- [ ] The sequence is driven by meaning.
- [ ] Each Pattern gives a reason for the next.
- [ ] Strong Patterns are balanced by quieter Patterns.
- [ ] Repeated Patterns create development.
- [ ] Pattern overlap preserves one Dominant Moment.
- [ ] The page does not include unnecessary Core Patterns.

---

# 04 — COMPONENTS

## Contract

- [ ] Each Component has one defined role.
- [ ] Required content is present.
- [ ] Optional content remains genuinely optional.
- [ ] The Component does not own the Dominant Moment.
- [ ] The Component does not perform several unrelated roles.
- [ ] The Component has a defined accessibility responsibility.

## Variants

- [ ] Each Variant preserves the original responsibility.
- [ ] Variants are based on meaningful conditions.
- [ ] Arbitrary visual combinations were not added.
- [ ] A Variant was not used to hide a separate Component role.
- [ ] Project-specific Variants remain local when appropriate.

## Composition

- [ ] Existing Components were considered before adding a new one.
- [ ] Layout composition remains shallow.
- [ ] Wrappers have distinct responsibilities.
- [ ] Component nesting remains understandable.
- [ ] Reuse has not flattened a unique Moment.

---

# 05 — SEMANTIC STRUCTURE

## Document

- [ ] Heading order is logical.
- [ ] Landmark structure is appropriate.
- [ ] Lists use semantic list markup.
- [ ] Quotations use appropriate semantics.
- [ ] Figures and Captions are associated correctly.
- [ ] Document language is set correctly.

## Reading Order

- [ ] DOM order preserves meaning.
- [ ] Mobile reading order is correct.
- [ ] Desktop layout does not create a conflicting sequence.
- [ ] Visual reordering does not confuse keyboard or screen-reader users.

## Interaction

- [ ] Links navigate.
- [ ] Buttons perform actions.
- [ ] Link purpose is understandable.
- [ ] Interactive surfaces have one clear responsibility.
- [ ] Nested conflicting controls are absent.
- [ ] Disabled or unavailable behavior is understandable where applicable.

---

# 06 — DESIGN TOKENS

## Token Roles

- [ ] Tokens represent reusable roles.
- [ ] Semantic Tokens are preferred over raw values.
- [ ] Token names do not depend on one page.
- [ ] Component Tokens remain limited.
- [ ] Project Tokens remain project-scoped.
- [ ] No Token was created only because a value appeared once.

## Token Integrity

- [ ] Overrides preserve semantic meaning.
- [ ] Contrast remains accessible.
- [ ] Token changes have predictable effects.
- [ ] Deprecated Tokens are not used in new code.
- [ ] Machine-readable files match documentation.

---

# 07 — RESPONSIVE

## Mobile

- [ ] The first viewport reveals one clear center.
- [ ] Primary meaning appears before Supporting detail.
- [ ] Reading order is correct.
- [ ] Touch targets remain usable.
- [ ] Text does not require horizontal scrolling.
- [ ] Media remains meaningful.
- [ ] Expression has been reduced before meaning.
- [ ] Pattern boundaries remain perceptible.

## Desktop

- [ ] Additional space strengthens relationships.
- [ ] Several elements do not become equal centers.
- [ ] Desktop does not create a different meaning from Mobile.
- [ ] Line length remains readable.
- [ ] Large Media does not obscure context.
- [ ] Spatial asymmetry preserves semantic order.

## Breakpoints

- [ ] Each breakpoint responds to a real composition need.
- [ ] Breakpoints are not based only on device categories.
- [ ] Fluid behavior is used where appropriate.
- [ ] Container context is considered where appropriate.
- [ ] No unintended horizontal overflow exists.

---

# 08 — TYPOGRAPHY

- [ ] Typography roles are clearly defined.
- [ ] Heading level is not determined by visual size.
- [ ] Prose measure remains readable.
- [ ] Japanese content wraps naturally.
- [ ] English content does not create overflow.
- [ ] Mixed-language content remains stable.
- [ ] Large text settings do not break the composition.
- [ ] Font loading does not hide text.
- [ ] Font fallback remains usable.
- [ ] Typography hierarchy does not depend on size alone.

---

# 09 — COLOR AND SURFACE

- [ ] Text contrast is sufficient.
- [ ] Focus contrast is sufficient.
- [ ] Color is not the only carrier of essential meaning.
- [ ] Accent color has a defined role.
- [ ] Surface changes have a compositional purpose.
- [ ] Cards or panels were not added only to divide content.
- [ ] Dark and light contexts preserve Component responsibility.
- [ ] Expressive color does not compete with Primary Media.

---

# 10 — SPACE AND LAYOUT

- [ ] Space reflects relationship.
- [ ] Grouped content appears grouped.
- [ ] Moment boundaries are perceptible.
- [ ] Section spacing responds to rhythm and intensity.
- [ ] Repeated equal spacing has not replaced composition.
- [ ] Grid is used only when comparison or collective presence matters.
- [ ] Sequence is used when narrative or hierarchy matters.
- [ ] Absolute positioning does not define reading order.
- [ ] Layering follows a controlled scale.
- [ ] Decorative layers do not block interaction.

---

# 11 — PHOTOGRAPHY AND MEDIA

## Images

- [ ] Real production Photography is used where required.
- [ ] Placeholder assets are clearly temporary.
- [ ] Intrinsic dimensions are defined.
- [ ] Crop preserves meaning.
- [ ] Focal areas remain visible.
- [ ] Responsive sizes are appropriate.
- [ ] Alternative text or decorative designation is correct.
- [ ] Caption relationship is preserved.
- [ ] Image failure does not destroy essential meaning.

## Video

- [ ] Autoplay is justified.
- [ ] Sound does not begin unexpectedly.
- [ ] Controls are available where needed.
- [ ] Captions or transcripts are provided where needed.
- [ ] A useful poster image exists.
- [ ] Reduced-motion behavior is defined.
- [ ] Video does not block reading or interaction.
- [ ] Loading strategy is appropriate.

---

# 12 — CREATIVE PHENOMENA AND MOTION

## Meaning

- [ ] Each meaningful motion has a definable source.
- [ ] Motion represents change,
      relation,
      response,
      or state.
- [ ] Decorative motion without responsibility has been removed.
- [ ] Creative Phenomena remain optional.
- [ ] Essential meaning remains without motion.

## Behavior

- [ ] Motion begins for a clear reason.
- [ ] Motion settles when its role is complete.
- [ ] Persistent motion has an ongoing responsibility.
- [ ] Scroll behavior does not take control away.
- [ ] Motion does not depend on exact scroll speed.
- [ ] Motion does not block keyboard navigation.

## Reduced Motion

- [ ] Reduced-motion behavior is implemented.
- [ ] Large movement is reduced or removed.
- [ ] Parallax is removed or reduced.
- [ ] Repeated ambient activity is reduced.
- [ ] A coherent still state remains.
- [ ] Sequence and interaction remain understandable.

## Performance

- [ ] Animation remains stable on slower devices.
- [ ] Main-thread work is controlled.
- [ ] Motion does not cause layout shift.
- [ ] Motion does not delay interaction.
- [ ] Advanced rendering has a documented role.

---

# 13 — ACCESSIBILITY

## Perceivable

- [ ] Meaningful images have appropriate alternatives.
- [ ] Video has appropriate alternatives.
- [ ] Text contrast is sufficient.
- [ ] Meaning does not depend on color alone.
- [ ] Reduced-motion users receive equivalent meaning.

## Operable

- [ ] All essential interaction works by keyboard.
- [ ] Focus is visible.
- [ ] Focus order is logical.
- [ ] No keyboard trap exists.
- [ ] Touch targets are sufficient.
- [ ] Overlays can be dismissed appropriately.

## Understandable

- [ ] Navigation labels are clear.
- [ ] Action labels describe consequences.
- [ ] Error or unavailable conditions are understandable where applicable.
- [ ] Creative language does not obscure interaction.
- [ ] Unexpected behavior is absent.

## Robust

- [ ] Native semantics are used where appropriate.
- [ ] Critical Components were reviewed with assistive technology where practical.
- [ ] Advanced visual behavior has a stable fallback.
- [ ] The experience does not depend on one input method.

---

# 14 — PERFORMANCE AND STABILITY

- [ ] Essential text loads before non-essential enhancement.
- [ ] Primary Media has appropriate priority.
- [ ] Supporting Media is deferred where appropriate.
- [ ] Creative Phenomena do not delay comprehension.
- [ ] Layout shift is controlled.
- [ ] Font loading is stable.
- [ ] Client-side code has clear responsibility.
- [ ] Third-party dependencies justify their cost.
- [ ] Unused code and assets are removed.
- [ ] The experience remains readable when enhancement fails.
- [ ] Slow network behavior has been reviewed.
- [ ] Slower device behavior has been reviewed.

---

# 15 — AI-GENERATED IMPLEMENTATION

- [ ] AI reviewed the relevant Core documents.
- [ ] AI reviewed the project context.
- [ ] AI identified the Moment and Pattern.
- [ ] AI identified Component responsibilities.
- [ ] AI did not invent new Core principles.
- [ ] AI did not create decorative motion without meaning.
- [ ] AI did not invent production facts or claims.
- [ ] AI did not alter unrelated files.
- [ ] AI selected the smallest sufficient change.
- [ ] AI documented material assumptions.
- [ ] Generated code was reviewed by a human.
- [ ] Generated output was tested with real content.

---

# 16 — CODE QUALITY

- [ ] Names describe responsibility.
- [ ] Files have understandable reasons to change.
- [ ] Project content is separated from reusable presentation.
- [ ] Side effects are localized.
- [ ] Global listeners are controlled.
- [ ] Boolean prop combinations do not hide several responsibilities.
- [ ] Dead Components are removed.
- [ ] Dead Variants are removed.
- [ ] Dead Tokens are removed.
- [ ] Dead styles and assets are removed.
- [ ] Comments explain why,
      not only what.
- [ ] Core code does not depend on project-specific business logic.

---

# 17 — AUTOMATED CHECKS

Record project-specific commands.

```text
Type Check:
Lint:
Format:
Unit Tests:
Integration Tests:
Accessibility Tests:
Build:
Bundle Review:
Dead Link Check:
```

- [ ] Type checking passes.
- [ ] Linting passes.
- [ ] Formatting is consistent.
- [ ] Relevant automated tests pass.
- [ ] Production build passes.
- [ ] Accessibility automation has been reviewed.
- [ ] Bundle or asset size is acceptable.
- [ ] Automated success was not treated as the only validation.

---

# 18 — HUMAN REVIEW

- [ ] The Dominant Moment is clear.
- [ ] The experience has an understandable rhythm.
- [ ] Photography remains trustworthy.
- [ ] Creative Phenomena carry meaning.
- [ ] The page feels composed rather than assembled.
- [ ] Mobile preserves the experience.
- [ ] The experience remains usable without motion.
- [ ] Unnecessary expression has been removed.
- [ ] The final state reaches Release.
- [ ] The implementation still feels like United Studio.
- [ ] The experience makes creation feel possible.
- [ ] The implementation makes someone want to create.

---

# RELEASE DECISION

## Result

```text
NOT READY
READY WITH DOCUMENTED EXCEPTIONS
READY
```

## Remaining Exceptions

```text
None
```

## Reviewer

```text
Name:
Date:
Commit:
Environment:
```
