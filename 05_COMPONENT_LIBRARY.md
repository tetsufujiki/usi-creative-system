# 05 — COMPONENT LIBRARY

## Reusable Meaning, Not Repeated Shape

**A component is not a reusable shape.**

**It is a reusable contract of meaning.**

A Component defines how a recurring role is expressed, what it requires, how it may change, and what it must not become.

The Component Library does not determine the experience by itself.

It gives Experience Composition a stable set of parts without replacing the judgment required to compose them.

## 05.0 — PURPOSE

This chapter translates the principles of Experience Composition into reusable structural and expressive units.

04 — EXPERIENCE COMPOSITION defines:

- the Dominant Moment.
- the direction of attention.
- the rhythm of the experience.
- continuity between Moments.
- the role and restraint of expression.

05 — COMPONENT LIBRARY defines:

- which recurring roles deserve a reusable Component.
- what each Component is responsible for.
- which parts of the Component are required.
- how Components may vary.
- how Components may be combined.
- when a new Component should not be created.

The Library is not a catalog of visual styles.

It is not a collection of finished sections.

It is not a page builder.

It is not an inventory of every interface element that may appear.

**The Library preserves meaning through reuse.**

### CHAPTER BOUNDARY

This chapter does not define:

- complete page structures.
- page-level narrative sequences.
- service-specific workflows.
- implementation APIs.
- CSS class names.
- framework-specific component code.
- token values.
- animation duration.
- database or application state.

Those decisions belong to Composition Patterns, Implementation Contract, or project-specific extensions.

The Component Library remains smaller than the number of experiences it supports.

A small number of stable Components should create many different compositions.

## 05.1 — COMPONENT AS CONTRACT

A Component is defined by its contract, not by its current appearance.

The contract contains:

- Role.
- Required Content.
- Optional Content.
- Structural Relationships.
- Responsive Behavior.
- Expression Boundary.
- Interaction Boundary.
- Accessibility Responsibility.

### ROLE

Role defines why the Component exists.

A Component should be describable with one clear sentence.

For example:

- Frame controls the readable and visual width of a composition.
- Section creates a perceptible region within a page.
- Heading Group introduces the meaning of a Moment.
- Media presents visual evidence or creative atmosphere.
- Continuation Link reveals how the experience may proceed.
- Phenomenon Surface provides a bounded place for Creative Phenomena.

A visual description is not enough.

The following are not valid roles:

- a large card.
- a stylish heading.
- a modern section.
- an animated background.
- a premium layout.

These describe appearance, not responsibility.

### REQUIRED CONTENT

Required Content is the minimum needed for the Component to perform its role.

A Component should not require content only because one existing page contains it.

Required Content must be essential to the contract.

For example:

- Heading Group requires a primary heading.
- Media requires a visual asset and meaningful alternative text or an explicit decorative role.
- Work Card requires a work identity and a destination or defined static purpose.
- Section requires a compositional role within the page.

### OPTIONAL CONTENT

Optional Content extends a Component without changing its essential role.

Optional Content may include:

- supporting language.
- metadata.
- caption.
- secondary media.
- continuation.
- restrained Creative Phenomena.

Optional Content must not become a hidden requirement.

A Component should remain coherent when optional content is absent.

### STRUCTURAL RELATIONSHIPS

A Component defines how its internal parts relate.

It may define:

- order.
- grouping.
- alignment.
- containment.
- emphasis.
- allowable nesting.
- relationship to surrounding Space.

It should not define the complete meaning of the page.

The same Component may support different Moments when its role remains stable.

### RESPONSIVE BEHAVIOR

Responsive behavior is part of the Component contract.

It is not a later correction.

A Component should define:

- what remains Primary on Mobile.
- which relationships become sequential.
- which elements may move below another.
- what may be reduced.
- what must remain visible.
- what must never depend on hover.
- what must preserve its semantic order.

Responsive behavior should protect meaning, not reproduce Desktop geometry at a smaller scale.

### EXPRESSION BOUNDARY

Each Component must state how expressive it is allowed to become.

A structural Component should not become the protagonist through decorative styling.

An expressive Component should not carry essential information that disappears when motion or imagery is removed.

A Content Component should not become a substitute for page-level Experience Composition.

### INTERACTION BOUNDARY

Most Components in the Core Library are editorial or navigational.

Interactive behavior should remain minimal and explicit.

A Component must not introduce:

- hidden state.
- unexpected transformation.
- required gesture without visible affordance.
- irreversible action.
- complex workflow behavior.

without being defined by the Interaction Extension.

### ACCESSIBILITY RESPONSIBILITY

Accessibility belongs to the Component contract.

Each Component should define responsibility for:

- semantic structure.
- reading order.
- focus order when interactive.
- alternative text.
- contrast.
- reduced motion.
- touch target requirements.
- keyboard access where applicable.

Accessibility must not be treated as a project-level repair.

## 05.2 — COMPONENT FAMILIES

The Core Library uses four Component Families.

```
Layout
Content
Navigation
Expressive
```

These Families describe responsibility.

They do not create separate visual styles.

### LAYOUT COMPONENTS

Layout Components organize relationships.

They control:

- width.
- containment.
- flow.
- grouping.
- alignment.
- repetition.
- spatial sequence.

They should remain visually quiet.

Layout Components must not decide what the Dominant Moment is.

They provide the conditions in which a Moment can be composed.

### CONTENT COMPONENTS

Content Components carry meaning directly.

They include recurring forms of:

- headings.
- prose.
- photography.
- moving image.
- caption.
- quotation.
- work identity.
- supporting metadata.

Content Components should preserve semantic clarity before visual variation.

They may hold Primary or Supporting roles depending on the Moment.

### NAVIGATION COMPONENTS

Navigation Components reveal continuity.

They show:

- where the person is.
- what may be entered.
- what may be explored.
- how the experience may continue.
- how the experience may return.

Navigation should remain understandable without becoming the main expression of every Moment.

Navigation Components should not create urgency unless the meaning of the experience requires it.

### EXPRESSIVE COMPONENTS

Expressive Components provide a bounded place for Creative Phenomena.

They may carry:

- perceptible change.
- trace.
- relation.
- emergence.
- transition.
- restrained atmosphere.

They are not effect containers.

They must identify:

- the Creative Principle that is their source.
- the change that should be perceived.
- their relationship to the current Moment.
- how they settle or leave.
- what remains when motion is unavailable.

Expressive Components are optional.

The absence of an Expressive Component must remain a valid composition.

## 05.3 — ANATOMY AND VARIANTS

Every registered Component should define a stable Anatomy.

Anatomy names the meaningful parts of the Component.

For example:

```
Heading Group
├── Eyebrow — optional
├── Heading — required
├── Supporting Copy — optional
└── Continuation — optional
```

Anatomy should describe roles, not DOM structure or class names.

### REQUIRED AND OPTIONAL PARTS

Required parts establish identity.

Optional parts extend use.

A Component should not contain many conditional parts that create several unrelated Components inside one name.

When optional parts significantly change the role, a separate Component or Pattern may be needed.

### VARIANTS

A Variant is allowed when the role remains the same but the conditions of expression change.

Valid Variant sources include:

- content density.
- media proportion.
- emphasis level.
- alignment required by composition.
- presence or absence of Supporting content.
- restrained tonal difference.
- relationship to a dark or light surface.

Invalid Variant sources include:

- every visual experiment.
- project name.
- page name.
- one-off marketing preference.
- arbitrary color.
- arbitrary corner radius.
- arbitrary animation.

**A Variant changes expression.**

**It does not change responsibility.**

If responsibility changes, it is not a Variant.

### CONTENT TOLERANCE

A Component must define the range of content it can support.

It should be tested with:

- short content.
- long content.
- missing optional content.
- Japanese and English text.
- narrow Mobile width.
- large text settings.
- unexpected but valid image proportions.

A Component that works only with ideal content is not stable.

### STATES

Core Components should avoid product-style States unless those States are intrinsic to simple navigation.

Examples may include:

- current.
- expanded.
- collapsed.
- unavailable.

Processing, pending, error, success, and account-specific States belong to the Interaction Extension.

### SEMANTIC ANATOMY BEFORE VISUAL ANATOMY

The meaningful structure must remain clear when decorative styling is removed.

A Component should survive:

- reduced color.
- reduced motion.
- missing imagery.
- increased text size.
- narrow width.

The contract must remain legible after expression has been reduced.

## 05.4 — COMPOSITION AND EXTENSION

Components do not compose themselves.

The presence of reusable parts does not remove the need for Experience Composition.

Before selecting a Component, define the Moment.

Before selecting a Variant, define the role of the Component within that Moment.

### COMPOSE BY ROLE

Components should be combined because their responsibilities support one meaning.

A common relationship may be:

```
Section
└── Frame
    └── Stack
        ├── Heading Group
        ├── Media
        └── Continuation Link
```

This structure is not automatically a Pattern.

It becomes meaningful only when each part supports the same Moment.

### KEEP LAYOUT SHALLOW

Avoid unnecessary wrappers.

Each Layout Component must perform a distinct spatial role.

Do not add a Component only to:

- attach one class.
- create one margin.
- rename a generic container.
- hide project-specific styling.
- satisfy visual symmetry in code.

A shallow composition is easier to understand, adapt, and preserve across Mobile.

### COMPONENTS DO NOT OWN THE MOMENT

A Heading Group does not automatically become Primary.

A Media Component does not automatically become Hero.

A Work Card does not automatically require a Grid.

A Phenomenon Surface does not automatically require motion.

The page composition assigns the role.

The Component preserves the contract.

### EXTENSION CONDITIONS

A new Component may be proposed when:

1. A distinct recurring role can be named.
2. Existing Components cannot perform that role without changing their contracts.
3. The proposed Component can be described independently of one page.
4. Its required and optional parts can be defined.
5. Its Mobile behavior can be explained.
6. Its accessibility responsibility can be identified.
7. It is likely to appear in more than one composition, or it carries a uniquely important semantic responsibility.

Repeated appearance alone is not enough.

A repeated mistake should not become a Component.

### VARIANT BEFORE COMPONENT

Before creating a new Component, consider whether the need is:

- a different content amount.
- a different alignment.
- a different media ratio.
- a different emphasis.
- an optional part.
- a composition-level difference.

If the responsibility remains unchanged, prefer a Variant or Composition Pattern.

### COMPONENT BEFORE ONE-OFF

Before creating a one-off section, consider whether it can be composed from existing Components.

However, do not force a unique Moment into an unsuitable reusable structure.

Reuse should protect meaning.

It should not flatten difference.

### DEPRECATION

A Component may be deprecated when:

- its role is no longer distinct.
- another Component now contains its valid responsibility.
- its Variants have become unrelated.
- it repeatedly causes competing expression.
- its accessibility contract cannot be maintained.
- its use no longer reflects the Creative System.

Deprecation should include a replacement path or a documented reason for removal.

## 05.5 — EVALUATION

Every proposed or changed Component should answer:

1. What recurring role does it perform?
2. Can that role be stated without describing appearance?
3. Which parts are required?
4. Which parts are optional?
5. Does the role already exist in another Component?
6. Does it preserve one Dominant Moment?
7. Does it remain coherent on Mobile?
8. Does it remain understandable without motion?
9. Does it tolerate real content?
10. Does it preserve semantic and reading order?
11. Is it a Component, a Variant, a Pattern, or a one-off composition?
12. Would removing it make the Library clearer?

**If the role cannot be named, do not register it.**

**If an existing contract already performs the role, do not duplicate it.**

## CHAPTER DECISION RULES

The following rules are normative.

### MUST

1. Every Component MUST have one clearly defined role.
2. Every Component MUST define required and optional content.
3. Every Component MUST preserve semantic order on Mobile.
4. Every Component MUST state its accessibility responsibility.
5. A Variant MUST preserve the Component’s original responsibility.
6. Expressive Components MUST trace their behavior to meaning.
7. Components without a distinct reusable role MUST NOT enter the Registry.
8. Components MUST NOT determine the Dominant Moment independently of composition.

### SHOULD

1. Layout Components SHOULD remain visually quiet.
2. Components SHOULD tolerate varied content length and media proportion.
3. Component compositions SHOULD remain shallow.
4. Existing Components SHOULD be combined before a new Component is created.
5. Variants SHOULD be preferred when responsibility does not change.
6. Strong visual expression SHOULD remain controlled by Experience Composition.
7. Each Component SHOULD remain coherent when optional content is absent.

### MAY

1. A Component MAY serve different Moments when its role remains stable.
2. A Component MAY have restrained Variants.
3. A unique semantic role MAY justify a Component before repeated use exists.
4. A Component MAY omit visual expression entirely.
5. Project-specific Components MAY exist outside the Core Registry.

## CODEX INTERPRETATION BOUNDARY

Codex MUST NOT infer that:

- every repeated layout is a Component.
- every section requires a named Component.
- every Component requires multiple Variants.
- every Component requires animation.
- every Component should accept every possible content type.
- visual similarity means semantic equivalence.
- semantic difference always requires a new Component.
- the Registry is permission to display all Components.
- a Component name determines its visual prominence.
- project-specific code should automatically enter the Core Library.

When classification is unclear, use the following order:

1. Identify the role.
2. Check the existing Registry.
3. Determine whether responsibility changes.
4. Prefer composition over duplication.
5. Prefer a Variant over a new Component.
6. Keep project-specific needs outside the Core Library.
7. Do not register the Component until its contract is clear.
