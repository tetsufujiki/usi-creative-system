# 07 — IMPLEMENTATION CONTRACT

## Preserve Meaning Through Code

**Implementation is not the final stage of design.**

**It is the stage where design becomes accountable.**

A design may express the Creative System in intention
and still lose it through implementation.

Meaning may be weakened by:

- arbitrary spacing.
- uncontrolled variants.
- incorrect reading order.
- decorative motion.
- inconsistent Typography.
- inaccessible interaction.
- fragile responsive behavior.
- duplicated Components.
- generated code without clear responsibility.

The Implementation Contract defines
how the United Studio Creative System
must survive translation into code.

## 07.0 — PURPOSE

This chapter establishes the contract
between the Creative System
and its implementation.

01 — MANIFESTO defines why the system exists.

02 — CREATIVE PRINCIPLES defines how creation grows.

03 — CREATIVE PHENOMENA defines how that growth becomes perceptible.

04 — EXPERIENCE COMPOSITION defines how meaning becomes one experience.

05 — COMPONENT LIBRARY defines reusable roles.

06 — COMPOSITION PATTERNS defines reusable relationships between Moments.

07 — IMPLEMENTATION CONTRACT defines
how those decisions become code
without losing meaning.

This chapter governs:

- Design Tokens.
- semantic structure.
- Component implementation.
- responsive behavior.
- Typography.
- Color.
- Space.
- Photography.
- Creative Phenomena.
- Motion.
- accessibility.
- performance.
- code responsibility.
- AI-generated implementation.
- validation.
- project extension.

### THE CONTRACT

Implementation must preserve:

```text
meaning
→ role
→ relationship
→ behavior
→ expression
```

It must not reverse this order.

Implementation must not begin with:

```text
available component
→ visual style
→ animation
→ content
→ meaning
```

The Creative System determines responsibility.

Code realizes it.

### CHAPTER BOUNDARY

This chapter defines implementation principles
and system-level constraints.

It does not define:

- one required framework.
- one required CSS methodology.
- one repository structure for every project.
- one hosting platform.
- one content management system.
- one animation library.
- one testing library.
- exact production infrastructure.
- project-specific database architecture.
- service-specific workflows.
- business logic.

Projects may choose appropriate technologies
when they preserve this contract.

### TECHNOLOGY INDEPENDENCE

The Core System must remain understandable
without React,
Next.js,
Tailwind,
or any other specific technology.

Framework documentation may translate this contract
into project-specific rules.

Framework rules must remain subordinate
to the Creative System.

**Technology may change.**

**The contract must remain.**

## 07.1 — SOURCE OF TRUTH

Implementation must distinguish
between different kinds of authority.

### PRINCIPLE AUTHORITY

The philosophical and experiential source of truth is:

```text
01_MANIFESTO.md
02_CREATIVE_PRINCIPLES.md
03_CREATIVE_PHENOMENA.md
04_EXPERIENCE_COMPOSITION.md
```

These files define intent,
meaning,
and experiential judgment.

### STRUCTURAL AUTHORITY

The reusable structural source of truth is:

```text
05_COMPONENT_LIBRARY.md
COMPONENT_REGISTRY.md
06_COMPOSITION_PATTERNS.md
COMPOSITION_PATTERN_REGISTRY.md
```

These files define:

- Component responsibility.
- Pattern responsibility.
- boundaries.
- Anatomy.
- reusable relationships.

### IMPLEMENTATION AUTHORITY

Machine-readable implementation files may include:

```text
design-tokens.json
component-contracts.json
motion-tokens.json
```

or equivalent project-specific files.

These files define values
that tools and code may consume directly.

They must not introduce principles
that do not exist in the Creative System.

### PROJECT AUTHORITY

Each project may define:

```text
PROJECT_CONTEXT.md
IMPLEMENTATION_PROFILE.md
CONTENT_MODEL.md
```

or equivalent documents.

Project files may specify:

- framework.
- repository structure.
- breakpoints.
- available assets.
- content source.
- supported browsers.
- project-specific Components.
- local Composition Patterns.
- performance targets.
- deployment constraints.

Project files may narrow the Core Contract.

They must not silently contradict it.

### CONFLICT ORDER

When instructions conflict,
use the following priority:

1. Accessibility and user safety.
2. The intended meaning of the current Moment.
3. Creative Principles and Experience Composition.
4. Component and Pattern contracts.
5. Project requirements.
6. Design Tokens.
7. existing implementation conventions.
8. generated code convenience.

Existing code is not automatically correct
because it already exists.

## 07.2 — DESIGN TOKENS

Design Tokens are named decisions.

They are not a complete visual language.

A Token should represent
a stable system-level role.

Examples include:

- surface roles.
- text roles.
- spacing roles.
- Typography roles.
- radius roles.
- border roles.
- motion roles.
- elevation roles.
- layout constraints.

### SEMANTIC BEFORE RAW

Prefer semantic Tokens:

```text
color.text.primary
color.surface.quiet
space.section.standard
type.heading.primary
motion.settle
```

over implementation-only names:

```text
blue500
gray100
spacing24
font48
duration300
```

Raw values may exist as foundations.

Components and Patterns should consume semantic roles.

### TOKEN LAYERS

A Token system may use three layers:

```text
Primitive
→ Semantic
→ Component
```

**Primitive Tokens**

Store raw values.

Examples:

- color values.
- font sizes.
- spacing units.
- duration values.
- radius values.

**Semantic Tokens**

Define system roles.

Examples:

- primary text.
- quiet surface.
- expressive accent.
- section spacing.
- reading width.

**Component Tokens**

Define limited Component-specific decisions
when the relationship cannot be expressed
through Semantic Tokens alone.

Component Tokens should remain rare.

### TOKEN CREATION

Create a Token when:

1. The decision has a reusable role.
2. The role appears across more than one Component or Pattern.
3. The value must remain consistent.
4. The name can be understood without knowing one page.
5. Changing it should create a predictable system-wide effect.

Do not create a Token for:

- every numerical value.
- every one-off margin.
- every unique crop.
- every local adjustment.
- every animation property.
- every visual experiment.

### TOKEN NAMES

Token names should describe responsibility.

Valid:

```text
space.section.compact
space.section.standard
space.section.expansive
```

Weak:

```text
space.80
space.120
space.homeHero
```

Project-specific Tokens may use project scope
when the decision is intentionally local.

### TOKEN VALUES

Values must not be selected
only because they form a mathematically complete scale.

A scale should support:

- readable rhythm.
- Mobile composition.
- real content.
- accessibility.
- meaningful contrast.
- visual restraint.

A complete scale with no experiential role
is not a useful Token system.

### TOKEN OVERRIDES

Projects may override Token values
when the semantic role remains unchanged.

An override must not:

- change the meaning of the Token.
- reduce accessibility.
- create a new visual role under an existing name.
- make Mobile behavior unstable.
- break contrast or reading order.

If the role changes,
create a new project Token.

## 07.3 — SEMANTIC STRUCTURE

Semantic structure is part of the visual experience.

The implementation must preserve:

- document hierarchy.
- reading order.
- landmark structure.
- relationship between content and controls.
- relationship between Media and Caption.
- meaningful link purpose.
- form labeling when forms exist.

### HTML BEFORE VISUAL ABSTRACTION

Use native semantic elements
when they correctly express responsibility.

Examples include:

- headings.
- paragraphs.
- lists.
- figures.
- captions.
- navigation.
- buttons.
- links.
- sections.
- articles.
- forms.

Do not use generic containers
when a native element communicates the correct role.

### VISUAL ORDER AND READING ORDER

Visual order must not contradict semantic order.

CSS positioning must not create
a different sequence from the DOM
when sequence carries meaning.

This is especially important for:

- Split.
- Grid.
- Navigation.
- featured works.
- responsive reordering.
- Media and Copy relationships.

Mobile reading order
should normally determine the semantic order.

Desktop may create spatial variation
without changing meaning.

### HEADING STRUCTURE

Heading level expresses document structure.

It is not a Typography Variant.

A visually small heading may remain structurally important.

A visually large sentence
does not automatically become a heading.

Components must receive or derive
the appropriate heading level
without hard-coding incorrect hierarchy.

### LINKS AND BUTTONS

A Link moves to a destination.

A Button performs an action.

Do not choose based on visual style.

Do not implement a Navigation destination as a Button
only to reuse styling.

Do not implement an action as a Link
only to avoid Button behavior.

### CLICKABLE SURFACES

Large linked surfaces must have:

- one clear destination.
- one understandable accessible name.
- predictable focus behavior.
- no conflicting nested interactive elements.

Do not make an entire Component interactive
when only one part requires interaction.

## 07.4 — COMPONENT IMPLEMENTATION

Code Components must correspond
to defined responsibilities.

A code Component may implement:

- one Core Component.
- one project-specific Component.
- one stable implementation utility.
- one bounded interaction responsibility.

A code Component should not exist
only because a file became long.

### CONTRACT BEFORE API

Before defining props,
define the Component contract.

The implementation API should express:

- required content.
- optional content.
- meaningful Variants.
- semantic responsibility.
- responsive behavior.
- accessibility behavior.

The API must not expose arbitrary styling
as its primary method of use.

### PROP DESIGN

Prefer props that express role:

```text
emphasis
mediaRole
surfaceRole
alignment
density
```

Avoid APIs dominated by arbitrary appearance:

```text
fontSize
paddingTop
backgroundHex
borderRadius
animationName
```

Low-level styling escape hatches may exist
for local composition.

They must not become the normal Component API.

### REQUIRED CONTENT IN TYPES

When possible,
required content should be required
by the implementation type system.

Optional content should remain genuinely optional.

Do not define all props as optional
and rely on runtime visual assumptions.

### VARIANT CONTROL

Variants must correspond
to the Component Library contract.

Do not generate Variants
for every combination of:

- color.
- size.
- alignment.
- radius.
- shadow.
- motion.

Prefer composition,
Tokens,
and local layout
over combinatorial Variant growth.

### COMPOSITION OVER CONFIGURATION

Prefer composing stable Components
over creating one highly configurable Component
that performs unrelated roles.

A Component with many Boolean props
may contain several hidden responsibilities.

Examples of warning signs include:

```text
isHero
isCard
isFeature
isCompact
isAnimated
isDark
isCentered
isEditorial
```

When combinations create different semantic roles,
separate the responsibilities.

### WRAPPER CONTROL

Avoid Components that only:

- add one margin.
- rename a container.
- forward all props unchanged.
- hide one utility class.
- create no semantic or reusable relationship.

A wrapper is justified
when it protects a stable responsibility.

### PROJECT-SPECIFIC COMPONENTS

Project-specific Components should remain
within the project layer.

They may enter the Core Registry only after:

- the role is independently definable.
- the role appears across multiple compositions.
- the contract has been tested.
- Mobile behavior is known.
- accessibility responsibility is known.
- the role is not service-specific.

### DEPRECATION

Deprecated Components should:

- remain identifiable.
- include a replacement path.
- avoid new usage.
- be removed after migration.
- not be silently aliased forever.

## 07.5 — RESPONSIVE IMPLEMENTATION

Responsive design preserves meaning
across available space.

It is not a set of device-specific screenshots.

### MOBILE AS SEMANTIC BASE

Mobile should establish:

- reading order.
- Primary meaning.
- essential content.
- necessary interaction.
- clear Pattern boundaries.
- minimal expression.

Desktop may extend this structure.

Desktop must not repair
a Mobile composition that lacks meaning.

### BREAKPOINTS

Breakpoints should respond
to composition failure,
not device marketing categories.

Introduce a breakpoint when:

- readable measure fails.
- Component relationships no longer fit.
- attention becomes unclear.
- Media loses meaning.
- Navigation becomes unusable.
- content requires a different sequence.
- touch or pointer behavior changes materially.

Do not create breakpoints
only to match a list of devices.

### FLUID BEFORE DISCRETE

Use fluid behavior
where relationships can adapt continuously.

Examples include:

- Frame width.
- Typography within safe limits.
- section Space.
- gaps.
- Media size.

Use discrete changes
when responsibility or sequence changes.

### CONTAINER CONTEXT

Components should respond
to the space they actually receive
when possible.

Viewport width alone
may not describe Component conditions.

Container-aware behavior may be appropriate
for reusable Components.

### HORIZONTAL OVERFLOW

Unintentional horizontal overflow is a defect.

It must not be accepted
as the cost of expressive composition.

Potential causes include:

- fixed widths.
- long unbroken text.
- oversized Media.
- transforms.
- absolute positioning.
- code blocks.
- decorative layers.

### MOBILE REDUCTION

On Mobile,
remove expression before removing meaning.

A valid reduction order is:

1. remove decorative layers.
2. reduce simultaneous relationships.
3. reduce motion.
4. reduce secondary Media.
5. reduce Supporting content when appropriate.
6. preserve Primary meaning and continuation.

Do not hide essential content
only to preserve a visual composition.

## 07.6 — TYPOGRAPHY

Typography carries voice,
hierarchy,
pace,
and silence.

It must not be treated
as a collection of font sizes.

### TYPOGRAPHIC ROLES

Typography Tokens should represent roles such as:

- Display.
- Primary Heading.
- Secondary Heading.
- Body.
- Supporting.
- Caption.
- Navigation.
- Interface Label.

Roles should remain fewer
than the number of visual examples.

### HIERARCHY

Hierarchy should emerge through:

- role.
- scale.
- weight.
- Space.
- measure.
- contrast.
- position.

Do not rely on size alone.

### MEASURE

Text width must support reading.

Long Prose should not use
the full width of large screens.

Short Statements may use wider or narrower measures
according to rhythm and language.

Japanese and English may require
different line-length judgment.

### LINE HEIGHT

Line height should support:

- language.
- scale.
- density.
- reading duration.
- Mobile width.

Display Typography may be compact.

Prose must remain comfortable.

### FONT WEIGHT

Font weight should create meaningful hierarchy.

Do not use excessive weight
to compensate for weak structure.

### FONT LOADING

Font loading must protect:

- legibility.
- layout stability.
- performance.
- language support.

A fallback stack should remain usable.

Typography must not disappear
while a custom font loads.

### TEXT RESILIENCE

Components must tolerate:

- long Japanese titles.
- English words without natural breaks.
- mixed-language content.
- user text scaling.
- localization.
- missing optional Copy.

Do not truncate meaningful editorial content
only to preserve one layout.

## 07.7 — COLOR AND SURFACE

Color communicates role,
state,
emphasis,
and atmosphere.

It must not become arbitrary decoration.

### COLOR ROLES

Color Tokens should distinguish:

- text.
- background.
- surface.
- border.
- accent.
- focus.
- interactive.
- status where product extensions require it.
- expressive atmosphere.

A brand color is not automatically appropriate
for every role.

### CONTRAST

Text and meaningful controls
must meet accessible contrast requirements.

Subtle color may support atmosphere.

It must not carry essential meaning alone.

### EXPRESSIVE COLOR

Expressive color may be used
when it supports the Moment.

It should not:

- compete with Primary Media.
- reduce legibility.
- imply interaction where none exists.
- simulate depth without purpose.
- appear only because a Token exists.

### SURFACES

A surface should have a role.

Examples include:

- page foundation.
- quiet separation.
- focused statement.
- Media support.
- interactive boundary.
- expressive field.

Do not add cards or colored panels
only to divide content mechanically.

### DARK AND LIGHT CONTEXTS

Components used across dark and light surfaces
must preserve:

- contrast.
- hierarchy.
- Media clarity.
- focus visibility.
- semantic role.

A dark Variant must not become
a different Component responsibility.

## 07.8 — SPACE AND LAYOUT

Space carries rhythm.

It is not leftover area.

### SPACING ROLES

Spacing should be selected
according to relationship.

Examples include:

- inline separation.
- grouped content.
- Component interior.
- Component relationship.
- Moment separation.
- Pattern transition.
- page release.

The same numerical value
may serve different roles.

The role should determine usage.

### VERTICAL RHYTHM

Vertical Space should help identify:

- what belongs together.
- what begins.
- what ends.
- what is Primary.
- where attention may rest.

Repeated equal spacing
does not automatically create rhythm.

### SECTION SPACE

Section spacing should respond to:

- Pattern role.
- content density.
- intensity.
- preceding and following Moments.
- Mobile scale.
- release.

A strong Statement may need more Space.

A dense informational Moment may need less.

### GRID USE

Grid is a relationship tool.

It should not become
the default solution for all repeated content.

Use Grid when:

- comparison matters.
- collective presence matters.
- repeated items have comparable roles.

Use sequence when:

- narrative matters.
- hierarchy matters.
- discovery matters.
- one work deserves Primary attention.

### ABSOLUTE POSITIONING

Absolute positioning may support expression.

It must not:

- define essential reading order.
- hide responsive failure.
- overlap content unpredictably.
- create inaccessible controls.
- cause essential content to leave the viewport.

### Z-INDEX

Layering should use a small,
named system.

Do not solve local conflicts
through arbitrary high values.

A layering scale may define:

- base.
- elevated content.
- navigation.
- overlay.
- modal.
- critical system layer.

Expressive layers should remain below
essential interaction unless intentionally designed otherwise.

## 07.9 — PHOTOGRAPHY AND MEDIA

Photography carries the reality of trust.

Implementation must protect that role.

### ASSET RESPONSIBILITY

Media implementation should define:

- intrinsic dimensions.
- aspect behavior.
- crop behavior.
- focal area where needed.
- loading behavior.
- alternative representation.
- caption relationship.
- performance strategy.

### IMAGE SELECTION

The implementation must not replace
meaningful Photography
with generic placeholders in final production.

Placeholders may support development.

They must remain clearly temporary.

### CROPPING

Crop must preserve:

- subject.
- gesture.
- equipment or environmental evidence.
- relationship to Copy.
- intended emotional distance.

A responsive crop may change.

The role of the image must not.

### OBJECT FIT

`cover` is not a universal solution.

Use containment or natural aspect
when the full object or composition matters.

Use cropping
when atmosphere or focus can remain intact.

### RESPONSIVE IMAGES

Serve appropriate image sizes.

Do not load desktop-scale assets
for small Mobile contexts without reason.

Performance decisions
must not reduce essential image quality
below the level required for trust.

### VIDEO

Video should define:

- whether sound is essential.
- whether autoplay is appropriate.
- controls.
- captions or transcript where needed.
- poster image.
- reduced-motion behavior.
- loading strategy.

Autoplay video must not:

- block reading.
- unexpectedly play sound.
- consume excessive resources.
- become the only carrier of essential meaning.

## 07.10 — CREATIVE PHENOMENA AND MOTION

Motion is implementation of change.

It is not proof of creativity.

### SOURCE OF MOTION

Every meaningful motion should be traceable to:

- a Creative Principle.
- a perceptual change.
- a Pattern transition.
- an Interface state in a product extension.
- a clear spatial relationship.

If the source cannot be named,
remove the motion.

### MOTION ROLES

Motion Tokens may define roles such as:

- appear.
- respond.
- connect.
- transform.
- settle.
- leave.

They should not be named
only by duration.

### DURATION

Duration should follow:

- distance.
- scale.
- complexity.
- attention.
- physical suggestion.
- reading context.

A universal duration
does not fit every role.

A restrained Token set
may establish a shared rhythm.

### EASING

Easing should support the perceived cause.

It should not be selected
only because it feels fashionable.

Different roles may require:

- direct response.
- gradual emergence.
- controlled settling.
- quiet departure.

### SCROLL-BASED MOTION

Scroll may reveal progression.

It must not:

- take control away from the person.
- create essential content that cannot be reached reliably.
- require exact scroll speed.
- produce continuous distraction.
- break keyboard or assistive navigation.
- create severe performance cost.

### REDUCED MOTION

Reduced-motion support is mandatory.

When motion is reduced:

- meaning must remain.
- sequence must remain understandable.
- content must remain accessible.
- interaction must remain clear.
- Creative Phenomena must have a stable state.

Reduced motion is not necessarily no motion.

It should remove:

- large movement.
- parallax.
- repeated ambient activity.
- unnecessary transformation.
- vestibular risk.

### SETTLEMENT

Creative Phenomena should settle
after their role is complete.

Persistent motion must have
an ongoing responsibility.

Atmosphere alone
does not always justify continuous activity.

### PERFORMANCE

Motion must not cause:

- unstable frame rate.
- delayed interaction.
- excessive main-thread work.
- unreadable content.
- layout shift.
- high battery use without purpose.

Expression that cannot perform reliably
should be reduced.

## 07.11 — ACCESSIBILITY

Accessibility is part of the Creative System.

It is not an external compliance layer.

An experience that excludes
cannot fully support creation.

### PERCEIVABLE

Essential meaning must remain available through:

- readable text.
- appropriate contrast.
- alternative text.
- captions or transcripts.
- stable reduced-motion states.
- non-color indicators where needed.

### OPERABLE

Interactive elements must support:

- keyboard access.
- visible focus.
- sufficient target size.
- predictable behavior.
- escape or dismissal where relevant.
- no keyboard traps.

### UNDERSTANDABLE

Navigation,
labels,
actions,
and state changes
must remain clear.

Creative language may be expressive.

Interaction language must remain understandable.

### ROBUST

Semantic structure should work
across browsers,
devices,
and assistive technologies.

Do not depend on one device capability
for essential meaning.

### FOCUS

Focus styling is a system role.

It must not be removed
because it conflicts with visual styling.

Focus should be:

- visible.
- consistent.
- sufficiently contrasted.
- appropriate to the element shape.
- unaffected by decorative layers.

### MOTION AND FLASH

Avoid:

- rapid flashing.
- uncontrollable movement.
- large unexpected spatial shifts.
- forced parallax.
- motion that blocks reading.

### TARGET SIZE

Touch targets must remain usable
on Mobile.

Visual size may be smaller
when the interactive area remains sufficient
and does not overlap nearby controls.

### ACCESSIBILITY REVIEW

Accessibility review must occur:

- during Component design.
- during implementation.
- during responsive testing.
- after content integration.
- before release.

It must not be delayed
until final QA.

## 07.12 — PERFORMANCE AND STABILITY

Performance affects perception.

A slow or unstable experience
changes the meaning of the design.

### PRIORITY

Load in the following order:

1. essential structure.
2. essential language.
3. Primary Media.
4. required interaction.
5. Supporting Media.
6. Creative Phenomena.
7. decorative enhancement.

Expression must not delay comprehension.

### LAYOUT STABILITY

Reserve space for:

- images.
- video.
- embeds.
- dynamic Components.
- loaded fonts where possible.

Unexpected layout shift
breaks attention and trust.

### PROGRESSIVE ENHANCEMENT

The experience should preserve
its essential meaning before enhancement.

A valid baseline should include:

- readable content.
- working Navigation.
- visible Media alternatives.
- understandable order.
- accessible controls.

JavaScript and advanced rendering
may enhance the experience.

They must not be the only path
to essential content without project justification.

### CLIENT-SIDE RESPONSIBILITY

Do not move code to the client
only because interaction or animation might be added later.

Client-side code should have
a clear behavioral responsibility.

Prefer static or server-rendered output
for stable editorial content
when the chosen framework supports it.

### THIRD-PARTY CODE

Third-party libraries must justify:

- bundle cost.
- runtime cost.
- accessibility impact.
- maintenance cost.
- security exposure.
- visual responsibility.

Do not add a library
for one minor effect
that can be implemented more simply.

### FAILURE BEHAVIOR

Media,
Fonts,
JavaScript,
or external services may fail.

The experience should remain:

- readable.
- navigable.
- identifiable.
- recoverable where interaction exists.

## 07.13 — AI-GENERATED IMPLEMENTATION

AI may accelerate implementation.

It must not become the source of design authority.

### AI RESPONSIBILITY

AI may:

- translate defined contracts into code.
- propose implementation structures.
- generate variants within stated boundaries.
- identify duplication.
- assist with accessibility review.
- write tests.
- convert content formats.
- suggest performance improvements.
- document implementation decisions.

AI must not:

- invent new Creative Principles.
- create Core Components without a defined role.
- create Core Patterns from repeated layouts.
- replace real content with generic marketing language.
- add decorative motion without meaning.
- alter brand voice.
- optimize for generic design trends.
- override accessibility.
- silently change Component responsibility.
- expand scope to display all available content.

### READ BEFORE WRITING

Before implementing,
AI must read the relevant sources.

At minimum:

1. project context.
2. relevant Creative Principles.
3. relevant Experience Composition rules.
4. Component contract.
5. Pattern contract.
6. implementation constraints.
7. current code.

AI should not infer the system
only from screenshots or existing classes.

### PLAN BEFORE CHANGE

For substantial implementation,
AI should state or internally establish:

- the Moment.
- the Pattern.
- the Components involved.
- files to change.
- files not to change.
- responsive implications.
- accessibility implications.
- validation steps.

### MINIMUM CHANGE

AI should prefer
the smallest change that satisfies the contract.

It must not refactor unrelated code
without a clear reason.

It must not rename,
move,
or reformat unrelated files
only to create consistency.

### EXISTING CODE

AI must evaluate existing code
against the Creative System.

It should not preserve:

- duplication.
- inaccessible behavior.
- incorrect semantics.
- arbitrary Variants.
- dead code.
- visual workarounds.

only because they already exist.

However,
it should not rewrite stable code
without a material benefit.

### GENERATED COPY

AI-generated placeholder Copy
must remain visibly temporary.

AI must not publish invented:

- testimonials.
- project facts.
- equipment facts.
- customer claims.
- awards.
- dates.
- pricing.
- biographies.

### UNCERTAINTY

When implementation intent is unclear,
AI should use the contract priority order.

It should not fill uncertainty
with generic design conventions.

A documented local assumption
is better than silent invention.

## 07.14 — CODE QUALITY AND RESPONSIBILITY

Code should make responsibility visible.

### NAMING

Names should describe:

- role.
- content.
- behavior.
- relationship.

Avoid names based only on:

- page position.
- current color.
- temporary campaign.
- arbitrary size.
- visual resemblance.

Strong:

```text
EnvironmentSection
ContinuationLink
PhenomenonSurface
WorkCollection
```

Weak:

```text
BlueBlock
SectionTwo
BigCard
FancyHero
AnimatedThing
```

Project-specific names may be appropriate
when the role is genuinely local.

### FILE RESPONSIBILITY

A file should have
one understandable reason to change.

Avoid files that combine:

- unrelated Components.
- content data.
- animation logic.
- business logic.
- server access.
- page composition.

without a clear boundary.

### DATA AND PRESENTATION

Content data should remain distinguishable
from presentation logic.

Components should not hard-code project content
unless they are explicitly project-specific.

### EFFECTS

Side effects should be localized.

Rendering should not unexpectedly:

- write data.
- navigate.
- attach global listeners repeatedly.
- alter document state.
- start uncontrolled animation.

### COMMENTS

Comments should explain:

- why a non-obvious decision exists.
- which contract is being protected.
- why a workaround is necessary.
- which limitation remains.

Comments should not repeat
what the code already states.

### DEAD CODE

Remove unused:

- Components.
- Variants.
- Tokens.
- styles.
- event handlers.
- assets.

Do not keep speculative code
for imagined future use.

### DEPENDENCY DIRECTION

Project-specific code may depend on Core abstractions.

Core abstractions must not depend
on one project’s content or business logic.

## 07.15 — VALIDATION

Implementation is complete
only after validation.

Visual resemblance alone
is not sufficient.

### CONTRACT VALIDATION

Confirm:

- the intended Moment is preserved.
- the Pattern relationship is clear.
- Components perform their registered roles.
- no new responsibility is hidden in a Variant.
- expression remains restrained.
- continuation is understandable.

### CONTENT VALIDATION

Test with real or realistic content:

- long Japanese headings.
- short headings.
- missing optional Copy.
- multiple Media ratios.
- incomplete metadata.
- mixed Japanese and English.
- large text scaling.

### RESPONSIVE VALIDATION

Test:

- narrow Mobile.
- common Mobile widths.
- Tablet conditions when relevant.
- wide Desktop.
- constrained Component containers.
- orientation changes where relevant.

Do not validate only
at framework default breakpoints.

### ACCESSIBILITY VALIDATION

Test:

- keyboard navigation.
- focus visibility.
- heading order.
- landmarks.
- link purpose.
- alternative text.
- reduced motion.
- contrast.
- screen-reader interpretation for critical flows.
- touch target behavior.

### PERFORMANCE VALIDATION

Review:

- initial loading.
- image size.
- font loading.
- layout shift.
- client-side bundle.
- animation frame stability.
- unnecessary third-party code.
- behavior on slower devices.

### FAILURE VALIDATION

Test:

- image failure.
- slow font loading.
- disabled JavaScript when meaningful.
- missing optional content.
- long content.
- network delay.
- unsupported advanced features.

### CODE VALIDATION

Use appropriate project tools for:

- type checking.
- linting.
- formatting.
- automated tests.
- build.
- dead-link checking.
- accessibility testing.
- bundle review.

Passing automated checks
does not prove experiential correctness.

Failing checks
must not be ignored
only because the page appears correct.

### HUMAN REVIEW

A human reviewer should ask:

- Does the experience still feel like United Studio?
- Is the Dominant Moment clear?
- Does the page create desire for creation?
- Is Photography trustworthy?
- Are Creative Phenomena meaningful?
- Has implementation added noise?
- Does Mobile preserve the experience?
- What can be removed?

## 07.16 — EXTENSION AND GOVERNANCE

The Core Contract should remain stable.

Projects may extend it
without weakening it.

### IMPLEMENTATION PROFILE

Each significant project should define
an Implementation Profile.

It may include:

- framework.
- language.
- styling system.
- Token location.
- Component location.
- content source.
- asset rules.
- motion tools.
- supported browsers.
- test commands.
- deployment behavior.
- project-specific exceptions.

### LOCAL EXCEPTIONS

An exception should document:

- which Core rule is affected.
- why the exception is necessary.
- its scope.
- accessibility impact.
- responsive impact.
- removal or review condition.

An exception must not become
an undocumented new default.

### CORE PROMOTION

A project implementation may be promoted
into the Core System only when:

1. Its responsibility is broadly reusable.
2. It has been used in real composition.
3. Its contract is clear.
4. Its accessibility behavior is known.
5. Its responsive behavior is known.
6. It does not depend on project content.
7. It improves the Core without unnecessary expansion.

### VERSIONING

Changes that alter responsibility
should be documented.

Examples include:

- Component contract changes.
- Pattern contract changes.
- Token role changes.
- accessibility requirement changes.
- removal of supported behavior.

Value adjustments that preserve meaning
may require lighter documentation.

### SYSTEM GROWTH

The implementation system should grow
more slowly than the number of projects.

A new project should usually create:

- new compositions.
- local content.
- local Patterns when necessary.

It should not automatically create:

- new Core Components.
- new Core Tokens.
- new Core Patterns.
- new motion systems.

## 07.17 — EVALUATION

Every significant implementation decision should answer:

1. Which Moment does this support?
2. Which Pattern relationship does it preserve?
3. Which Component contract applies?
4. Is the responsibility visible in the code?
5. Is a new Token necessary?
6. Does Mobile preserve semantic order?
7. Is essential meaning available without motion?
8. Is Photography implemented as evidence or atmosphere?
9. Does the code remain accessible?
10. Does the implementation perform reliably?
11. Is AI-generated output grounded in the Creative System?
12. Is the change project-specific or Core?
13. What can be removed?
14. Does the implementation still make someone want to create?

**Code is correct only when responsibility,
meaning,
and behavior remain aligned.**

## CHAPTER DECISION RULES

The following rules are normative.

### MUST

1. Implementation MUST preserve the intended meaning of each Moment.
2. Semantic structure MUST reflect content responsibility.
3. Mobile MUST preserve meaningful reading order.
4. Components MUST implement defined contracts.
5. Variants MUST NOT change Component responsibility.
6. Essential meaning MUST remain available without motion.
7. Reduced-motion behavior MUST be provided.
8. Accessibility MUST be considered during implementation.
9. Design Tokens MUST represent stable roles.
10. AI-generated code MUST remain subordinate to the Creative System.
11. Project-specific behavior MUST NOT silently enter the Core System.
12. Validation MUST include content,
    responsive,
    accessibility,
    and performance review.
13. Existing code MUST NOT override a clearer system responsibility.
14. Implementation MUST NOT depend on decorative expression for essential meaning.

### SHOULD

1. Semantic Tokens SHOULD be preferred over raw values.
2. Mobile SHOULD establish the semantic base.
3. Component APIs SHOULD express role rather than arbitrary appearance.
4. Composition SHOULD be preferred over excessive configuration.
5. Client-side code SHOULD have a clear behavioral responsibility.
6. Creative Phenomena SHOULD load after essential meaning.
7. Third-party dependencies SHOULD justify their cost.
8. Project exceptions SHOULD be documented.
9. Code names SHOULD reveal responsibility.
10. Human review SHOULD accompany automated validation.
11. Core promotion SHOULD require real project evidence.
12. Unnecessary Components,
    Variants,
    Tokens,
    and effects SHOULD be removed.

### MAY

1. Projects MAY use different frameworks.
2. Projects MAY override Token values while preserving semantic roles.
3. Projects MAY define local Components and Patterns.
4. Components MAY use container-aware responsive behavior.
5. Creative Phenomena MAY use advanced rendering when justified.
6. AI MAY propose implementation alternatives within the contract.
7. Project-specific exceptions MAY exist when documented.
8. A project MAY use stricter implementation rules than the Core Contract.

## CODEX INTERPRETATION BOUNDARY

Codex MUST NOT infer that:

- every visual value requires a Token.
- every Token requires several values.
- every Component requires a client-side implementation.
- every Component requires Variants.
- every Pattern maps to one React Component.
- every section maps to one file.
- every repeated class requires abstraction.
- every long file requires splitting.
- every animation requires a library.
- every responsive change requires a breakpoint.
- Desktop layout determines DOM order.
- existing code is authoritative.
- generated consistency is more important than meaning.
- all available Components should be used.
- all project Components should enter the Core Registry.
- all accessibility work can be deferred to QA.
- passing automated tests proves the experience is correct.
- a visually accurate screenshot proves semantic correctness.
- framework best practices may override the Creative System without review.

When implementation is unclear,
use the following order:

1. Identify the intended Moment.
2. Identify the Pattern relationship.
3. Identify Component responsibilities.
4. Preserve semantic and reading order.
5. Establish the smallest accessible implementation.
6. Apply Semantic Tokens.
7. Add responsive adaptation.
8. Add required interaction.
9. Add Creative Phenomena only when their source is clear.
10. Validate with real content.
11. Remove unnecessary code and expression.
12. Document any remaining exception.
