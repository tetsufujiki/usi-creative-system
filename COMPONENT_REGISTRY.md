# COMPONENT REGISTRY

## Purpose

This file records the current reusable Components of the United Studio Creative System.

It is an implementation-facing companion to 05 — COMPONENT LIBRARY.

The Registry may grow, change, or deprecate entries without rewriting the principles of Chapter 05.

A Registry entry defines responsibility.

It does not define framework code, CSS classes, token values, or complete page compositions.

## STATUS

Each Component uses one of the following statuses.

### EXPERIMENTAL

The role is valid, but its Anatomy or boundaries remain under evaluation.

### STABLE

The role, Anatomy, responsive behavior, and accessibility responsibility are sufficiently clear for reuse.

### DEPRECATED

The Component should not be used in new work.

A replacement or removal reason must be documented.

## ENTRY FORMAT

Each Component entry should contain:

```
Name
Family
Status
Role
Required
Optional
May Contain
Must Not
Mobile
Accessibility
Notes
```

---

# LAYOUT

## Frame

**Family:** Layout\
**Status:** Stable

**Role**

Controls the readable or visual width of content within a larger surface.

**Required**

- Content.

**Optional**

- Width mode.
- Horizontal alignment.

**May Contain**

- Any Content, Navigation, or Expressive Component.

**Must Not**

- Determine the Dominant Moment.
- Add decorative background treatment by default.
- replace Section.

**Mobile**

- Preserves safe horizontal Space.
- Allows content to use available width.
- Must not create horizontal overflow.

**Accessibility**

- No independent semantic role is required.

---

## Section

**Family:** Layout\
**Status:** Stable

**Role**

Creates a perceptible region within a page or larger experience.

**Required**

- One compositional purpose.
- Content.

**Optional**

- Heading relationship.
- Surface role.
- Section identifier.
- restrained expressive layer.

**May Contain**

- Frame.
- Layout Components.
- Content Components.
- Navigation Components.
- one bounded Expressive Component.

**Must Not**

- Contain several unrelated Dominant Moments.
- become a Component only because a background color changes.

**Mobile**

- Must preserve one clear center.
- Must have a perceptible beginning and ending.

**Accessibility**

- Uses an appropriate semantic sectioning element when labelled.

---

## Stack

**Family:** Layout\
**Status:** Stable

**Role**

Creates vertical sequence between related elements.

**Required**

- Two or more children, unless used as a stable composition API.

**Optional**

- Spacing role.
- alignment.

**May Contain**

- Any Components that belong to one vertical relationship.

**Must Not**

- encode page-specific meaning.
- be duplicated for every spacing value.

**Mobile**

- Preserves semantic order.
- Remains vertical unless another relationship is explicitly defined.

**Accessibility**

- Must not alter reading order through visual positioning.

---

## Cluster

**Family:** Layout\
**Status:** Stable

**Role**

Groups related elements that may wrap within available inline space.

**Required**

- Related child elements.

**Optional**

- alignment.
- distribution.
- wrapping behavior.

**May Contain**

- metadata.
- Navigation links.
- tags.
- short supporting items.

**Must Not**

- be used for unrelated elements only to align them on one row.

**Mobile**

- Wraps without clipping.
- Must preserve touch target separation.

**Accessibility**

- Visual order must match reading order.

---

## Split

**Family:** Layout\
**Status:** Experimental

**Role**

Creates a meaningful relationship between two distinct regions.

**Required**

- Two regions with a defined relationship.

**Optional**

- media emphasis.
- reversed visual order.
- proportional balance.

**May Contain**

- Media and Copy.
- Primary and Supporting content.
- two related forms of evidence.

**Must Not**

- exist only to create visual symmetry.
- preserve Desktop order when Mobile meaning requires another sequence.

**Mobile**

- Converts to a semantic sequence.
- Primary meaning must appear in the correct reading position.

**Accessibility**

- DOM order must remain meaningful without visual layout.

---

## Grid

**Family:** Layout\
**Status:** Experimental

**Role**

Organizes repeated items whose comparison or collective presence is meaningful.

**Required**

- Two or more repeated items.

**Optional**

- column behavior.
- density mode.
- featured item.

**May Contain**

- Work Card.
- Media.
- repeated Content Components.

**Must Not**

- be used when a Narrative sequence is more appropriate.
- force unrelated items into equal prominence.

**Mobile**

- Reduces columns while preserving item order.
- Must not create excessively narrow cards.

**Accessibility**

- Reading order must remain predictable.

---

# CONTENT

## Heading Group

**Family:** Content\
**Status:** Stable

**Role**

Introduces the meaning of a Moment or a meaningful subsection within it.

**Required**

- Heading.

**Optional**

- Eyebrow.
- Supporting Copy.
- Continuation.

**May Contain**

- short text.
- Text Link or Continuation Link.

**Must Not**

- contain several competing headings.
- become decorative text without semantic heading structure.

**Mobile**

- Preserves the heading before supporting content.
- Must tolerate wrapping.

**Accessibility**

- Uses the correct heading level based on document structure, not visual size.

---

## Prose

**Family:** Content\
**Status:** Stable

**Role**

Presents sustained explanatory, narrative, or reflective language.

**Required**

- Text content.

**Optional**

- internal headings.
- lists.
- quotations.
- inline links.

**May Contain**

- semantically valid editorial content.

**Must Not**

- control page width independently of Frame.
- imitate display Typography through arbitrary markup.

**Mobile**

- Maintains readable measure.
- Avoids horizontal scrolling.

**Accessibility**

- Preserves semantic HTML and logical heading order.

---

## Media

**Family:** Content\
**Status:** Stable

**Role**

Presents visual or audiovisual material as evidence, atmosphere, work, or context.

**Required**

- Media asset.
- meaningful alternative text, caption, transcript, or explicit decorative designation.

**Optional**

- Caption.
- credit.
- focal position.
- aspect role.

**May Contain**

- image.
- video.
- audio-visual work preview.

**Must Not**

- serve as generic decoration without a documented role.
- carry essential meaning only through autoplay motion.

**Mobile**

- Preserves meaningful crop or full content.
- Does not overflow.
- Avoids forced height that hides important content.

**Accessibility**

- Requires appropriate alternative representation.
- Video requires accessible controls when interactive.

---

## Caption

**Family:** Content\
**Status:** Stable

**Role**

Connects Media to context, identity, or evidence.

**Required**

- Caption text.

**Optional**

- credit.
- date.
- equipment or work metadata.

**May Contain**

- short structured metadata.

**Must Not**

- repeat nearby Copy without adding context.
- carry the only essential explanation in visually insignificant text.

**Mobile**

- Remains visually connected to its Media.

**Accessibility**

- Must be associated with the relevant figure or Media.

---

## Quote

**Family:** Content\
**Status:** Experimental

**Role**

Allows a voice, statement, or remembered phrase to become a focused Content Moment.

**Required**

- Quoted language.

**Optional**

- attribution.
- context.

**May Contain**

- short or moderate quotation.

**Must Not**

- be used only to enlarge ordinary marketing language.
- imply direct quotation when language is paraphrased.

**Mobile**

- Must tolerate long Japanese line wrapping.
- Should not depend on oversized quotation marks.

**Accessibility**

- Uses appropriate quotation semantics.

---

## Work Card

**Family:** Content\
**Status:** Experimental

**Role**

Presents the identity of a work or project and provides a path toward its fuller experience.

**Required**

- work identity.
- title.
- destination or explicit static purpose.

**Optional**

- Media.
- category.
- year.
- collaborator.
- short context.

**May Contain**

- Media.
- metadata.
- Continuation Link.

**Must Not**

- compress a complete project narrative into a card.
- make all works visually equal when hierarchy is meaningful.
- contain unrelated promotional actions.

**Mobile**

- Preserves work identity before secondary metadata.
- Maintains a clear touch destination when linked.

**Accessibility**

- Linked cards require one understandable accessible name.
- Avoid nested conflicting links.

---

# NAVIGATION

## Site Header

**Family:** Navigation\
**Status:** Experimental

**Role**

Provides stable site identity and access to primary destinations.

**Required**

- site identity.
- primary navigation access.

**Optional**

- current location.
- restrained utility link.
- compact Mobile disclosure.

**May Contain**

- Navigation links.
- one quiet continuation or utility action.

**Must Not**

- dominate every Moment.
- become a promotional banner.
- contain several competing calls to action.

**Mobile**

- Remains understandable in a compact form.
- Must not depend on hover.
- Expanded navigation must preserve focus and reading order.

**Accessibility**

- Uses semantic navigation.
- Mobile disclosure requires keyboard and screen-reader support.

---

## Site Footer

**Family:** Navigation\
**Status:** Experimental

**Role**

Closes the site experience and provides stable secondary continuity.

**Required**

- site identity or ownership context.

**Optional**

- secondary navigation.
- legal information.
- contact path.
- related destinations.

**May Contain**

- restrained Navigation and supporting information.

**Must Not**

- introduce a new unrelated climax.
- repeat all page content.
- become an oversized sitemap by default.

**Mobile**

- Uses a clear vertical sequence.

**Accessibility**

- Navigation groups require understandable labels.

---

## Continuation Link

**Family:** Navigation\
**Status:** Stable

**Role**

Reveals the next meaningful possibility without interrupting the current Moment.

**Required**

- destination.
- understandable label.

**Optional**

- short supporting context.
- directional indicator.

**May Contain**

- text and a restrained icon.

**Must Not**

- use vague labels without surrounding context.
- imitate a button when no action-like emphasis is needed.
- create false urgency.

**Mobile**

- Maintains a sufficient touch target when presented as a primary continuation.

**Accessibility**

- Link purpose must be understandable from its accessible name and context.

---

# EXPRESSIVE

## Phenomenon Surface

**Family:** Expressive\
**Status:** Experimental

**Role**

Provides a bounded compositional region in which one Creative Phenomenon may become perceptible.

**Required**

- Creative Principle source.
- defined perceptual change.
- relationship to the current Moment.
- fallback or stable state.

**Optional**

- trigger.
- trace.
- response to scroll or presence.
- restrained interaction.

**May Contain**

- one Primary Creative Phenomenon.
- non-essential supporting visual layers.

**Must Not**

- become an effects canvas.
- contain unrelated phenomena.
- carry essential language only through motion.
- remain active without purpose.

**Mobile**

- Must be composed at Mobile scale.
- Must survive reduction.
- Must preserve one focus.

**Accessibility**

- Respects reduced motion.
- Provides a coherent still state.
- Must not block reading or interaction.

---

## Phenomenon Trace

**Family:** Expressive\
**Status:** Experimental

**Role**

Preserves evidence that a meaningful change occurred after active expression has settled.

**Required**

- relationship to a preceding change.

**Optional**

- residual form.
- altered Space.
- subtle color or material shift.
- stable visual remainder.

**May Contain**

- non-interactive visual evidence.

**Must Not**

- become permanent decorative noise.
- imply change that never occurred.
- compete with the next Moment.

**Mobile**

- Remains legible at small scale.
- May disappear when its meaning does not survive reduction.

**Accessibility**

- Essential meaning must remain available without the visual trace.

---

# REGISTRY RULES

1. New entries begin as Experimental.
2. Stable status requires use in real composition.
3. Project-specific Components remain outside this file unless their role is broadly reusable.
4. A new visual style does not create a Registry entry.
5. A new Variant does not create a Registry entry unless responsibility changes.
6. Deprecated entries remain documented until migration is complete.
7. Registry growth should remain slower than project growth.
8. When uncertain, do not add the Component.
