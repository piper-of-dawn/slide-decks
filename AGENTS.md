# AGENTS.md

Persistent instructions for Codex and other agents working in this repository.

This repository exists to generate high-quality HTML slide decks with intelligent infographics. The primary output is a Reveal.js HTML presentation. Do not use PowerPoint, Google Slides, Canva, Gamma, Tome, Beautiful.ai, or any proprietary slide system as the authoring environment.

## Repository Status

At the time this file was created, the repository had no project structure beyond hidden configuration folders. Use the default structure below unless a future project already establishes a clearer local convention.

## Default Repository Structure

Use this structure for new decks or when scaffolding the repository:

```text
.
|-- AGENTS.md
|-- package.json
|-- index.html
|-- slides.md
|-- src/
|   |-- main.js
|   |-- theme.css
|   |-- components/
|   |   |-- FigureFrame.*
|   |   |-- Callout.*
|   |   |-- AxisDiagram.*
|   |   |-- TaxonomyTree.*
|   |   |-- SliderDiagram.*
|   |   |-- CurveAnnotation.*
|   |   `-- ComparisonGrid.*
|   |-- charts/
|   |   `-- vega-lite specs
|   |-- diagrams/
|   |   |-- mermaid/
|   |   `-- d2/
|   `-- assets/
|       |-- icons/
|       |-- sketches/
|       `-- generated/
`-- README.md
```

## Core Output Contract

- The final deck must run as local HTML.
- Reveal.js is the main presentation engine.
- `slides.md` is preferred for slide content when it keeps the deck clean.
- Use custom HTML sections for advanced infographics.
- Keep the deck editable through text, CSS, SVG, and data specs.
- Mention export options only after the HTML deck works.
- Do not make proprietary tools part of the required workflow.

## Design Philosophy

The house style is minimal, editorial, quiet, and information-first. Slides should feel like a museum label combined with a modern research zine.

### Background

- Use a warm off-white paper background.
- Add a faint dotted-grid background with evenly spaced dots.
- Dots must be almost invisible.
- Avoid loud texture, heavy grain, collage, scrapbook effects, and decorative noise.
- Avoid shadows unless they are extremely subtle and functional.

### Typography

- Use sans-serif type for headings and body text.
- Use monospace type for labels, captions, dates, chart annotations, figure tags, and small technical text.
- Headings should be large, calm, left-aligned, and editorial.
- Avoid decorative fonts, AI-looking display fonts, and excessive font weights.
- Keep typography restrained and consistent across the deck.

### Layout

- Use a strict grid.
- Use generous whitespace.
- Prefer left-aligned composition.
- Build calm hierarchy.
- Prefer disciplined asymmetry: large text block on one side, small intelligent visual on the other.
- Every slide must have a clear visual thesis.
- Do not fill space just because it exists.
- Treat whitespace as an active design element.

### Color

- Use mostly near-black, soft gray, and one muted accent.
- Use accent color only for meaning: a highlight, target factor, active path, or important point.
- Avoid saturated colors.
- Avoid rainbow palettes unless the content genuinely requires categorical distinction.
- Avoid gradients unless they are extremely subtle and structural.

### Imagery

- Do not use glossy AI art.
- Do not use cinematic renders.
- Do not use 3D.
- Do not use generic stock imagery.
- Do not use decorative illustrations that fail to encode meaning.
- Prefer vector graphics over raster images.
- Prefer simple pencil sketches, hand-drawn line icons, diagrammatic illustrations, mathematical schematics, or flat symbolic visuals.
- Prefer SVG generated from code where possible.

## Tooling Rules

Use open-source tooling only.

### Default Stack

- Reveal.js for the HTML slide deck.
- CSS custom properties for the design system.
- Plain SVG for custom infographics.
- Mermaid for simple flowcharts, sequence diagrams, trees, timelines, and process diagrams.
- D2 for clean architecture and system diagrams.
- Vega-Lite for data charts.
- Rough.js only when a subtle hand-drawn line quality is useful.
- Excalidraw only as an optional source for manually created SVG sketch assets.

### Prohibited Tooling

Do not use:

- Canva
- PowerPoint as the authoring system
- Google Slides as the authoring system
- Gamma
- Tome
- Beautiful.ai
- Proprietary AI image generation
- Heavy texture packs
- Stock-art-based visual systems

## Slide Authoring Rules

### Start With The Message

Before coding any slide, identify:

- The one idea.
- What the viewer should understand after 5 seconds.
- The visual structure that best explains it.

### Avoid Generic Slides

- Do not create title-plus-bullets slides unless the content is genuinely a list.
- Convert concepts into visual models whenever possible.
- A slide should teach through structure, not decoration.

### Preferred Slide Patterns

- Concept definition: title, short explanation, symbolic diagram.
- Mechanism: causal chain with arrows.
- Taxonomy: branching tree or grouped columns.
- Quant concept: equation, visual interpretation, small annotated chart.
- Financial model: input -> transformation -> output.
- Risk model: factor -> exposure -> sensitivity -> portfolio effect.
- Comparison: three-column grid with compact explanations.
- Timeline: thin horizontal line with sparse events.
- Curve explanation: minimal axis, curve, labels.
- Portfolio concept: weights, exposures, sensitivities, correlations, or constraints shown visually.

### Text Discipline

- Prefer one strong heading.
- Add one compact explanatory paragraph.
- Include one intelligent visual.
- Add an optional tiny caption only when useful.
- Avoid long bullet lists.
- Keep labels precise and calm.

## Infographic Standards

The deck should contain intelligent infographics, not decoration.

Every visual must explain a concept, mechanism, taxonomy, timeline, tradeoff, equation, transformation, causal chain, or system structure.

Use:

- Small clean charts.
- Timelines.
- Callout boxes.
- Arrows.
- Comparison blocks.
- Annotated icons.
- Matrix layouts.
- Sliders.
- Gauges.
- Trees.
- Axes.
- Factor maps.
- Curve diagrams.

Avoid:

- Icons that only decorate.
- Stock illustration.
- Glossy, textured, cinematic aesthetics.
- Visual cliches.
- Diagrams that look generated instead of designed.

### Infographic Quality Bar

For every infographic, ask:

- Does the visual encode real information?
- Could the viewer reconstruct the idea from the diagram?
- Is every line, arrow, icon, and label necessary?
- Is the visual quieter than a typical startup deck?
- Is the hierarchy clear?
- Does it look human-designed rather than AI-generated?
- Does it avoid visual cliches?
- Does it avoid stock illustration?
- Does it avoid glossy, textured, cinematic aesthetics?

If the answer is no, simplify.

## Visual Grammar

Build and reuse a consistent visual language:

- Thin strokes.
- Rounded corners only when useful.
- Muted accent for active or target objects.
- Gray for inactive or contextual objects.
- Monospace labels for technical annotations.
- Consistent axis styling.
- Consistent callout styling.
- Consistent arrowheads, brackets, and leader lines.
- Consistent figure captions and tags.

## Reference Style Interpretation

Recreate the design philosophy, not exact reference slides.

The reference style means:

- Large editorial headings.
- Sparse explanatory body copy.
- Thin-line diagrams.
- Mostly black and gray.
- Monospace labels.
- Quiet off-white background.
- Conceptual visuals such as sliders, curves, taxonomy trees, and comparison columns.
- Strong whitespace.
- Low visual noise.

## Technical Implementation Rules

### Reveal.js

- Use Reveal.js as the main deck engine.
- Prefer `slides.md` for slide content unless custom HTML is clearly better.
- Use custom HTML sections for advanced infographics.
- Keep each slide semantically clean.
- Avoid inline chaos.
- Use reusable classes and components.
- Ensure the deck runs locally with npm scripts.
- Include an npm script for development preview.
- Include an npm script for build or export when applicable.

### CSS

Define the theme in `src/theme.css`.

Use these required CSS variables:

```css
:root {
  --paper: #f6f1e8;
  --ink: #171512;
  --muted: #6f6a61;
  --faint: #d8d0c3;
  --accent: #8f4f3a;
  --grid-dot: rgba(23, 21, 18, 0.11);
  --mono: "IBM Plex Mono", "SFMono-Regular", Consolas, monospace;
  --sans: "Inter", "Aptos", "Helvetica Neue", Arial, sans-serif;
  --slide-padding: 64px;
  --stroke-thin: 1.25px;
}
```

Implement dotted-grid paper with CSS `radial-gradient`, for example:

```css
.reveal {
  color: var(--ink);
  background-color: var(--paper);
  background-image: radial-gradient(var(--grid-dot) 0.75px, transparent 0.75px);
  background-size: 22px 22px;
}
```

CSS rules:

- Keep the grid subtle.
- Use consistent spacing tokens.
- Avoid heavy box shadows.
- Avoid loud borders.
- Use thin strokes.
- Keep responsive behavior predictable.
- Do not rely on browser defaults for important typography or diagram styling.

### SVG

- Prefer inline SVG for custom infographics.
- Use `currentColor` or CSS variables where practical.
- Use `viewBox` correctly.
- Add accessible `title` and `desc` elements when practical.
- Keep SVG simple and editable.
- Prefer strokes over filled cartoon shapes unless fills carry meaning.
- Avoid complex generated paths that future agents cannot reasonably edit.

### Mermaid

- Use Mermaid for quick structural diagrams.
- Keep Mermaid output visually consistent with the theme.
- Do not accept Mermaid defaults if they clash with the deck design.
- Customize Mermaid theme variables when needed.
- Prefer sparse diagrams over dense generated maps.

### D2

- Use D2 for architecture or system diagrams.
- Export D2 diagrams to SVG when embedding statically.
- Keep D2 diagrams sparse, aligned, and consistent with the deck style.
- Avoid default styling that conflicts with the theme.

### Vega-Lite

- Use Vega-Lite for data charts.
- Keep charts minimal.
- Remove unnecessary gridlines.
- Use thin axes.
- Use monospace labels where possible.
- Use muted colors.
- Annotate the point, region, or mechanism that matters.
- Avoid chartjunk.
- Title charts by the insight, not by the chart type.

### Rough.js

- Use Rough.js sparingly.
- Use it only for pencil-like line diagrams or sketch icons.
- Keep roughness subtle.
- Do not let sketchiness become noisy.

## Accessibility And Readability

- Slides must be readable on a projector.
- Text must have sufficient contrast.
- Do not use tiny labels for important content.
- Captions can be small but must remain legible.
- Use semantic HTML where possible.
- Maintain consistent heading hierarchy.
- Avoid purely color-based meaning; use labels, shapes, or position too.
- Check that text and labels do not overlap at common presentation sizes.

## Content Intelligence Rules

For finance, mathematics, economics, statistics, or technical topics:

- Do not turn equations into decoration.
- Explain what the equation is doing visually.
- Separate inputs, assumptions, transformation, and output when showing a model.
- Prefer "what changes what" diagrams.
- Prefer mechanism diagrams over generic icons.
- If showing a chart, title it by the insight.

When showing a factor model, distinguish:

- Factors.
- Exposures.
- Sensitivities.
- Residuals.
- Portfolio weights.
- Constraints.

## Deck Creation Workflow

When asked to create a deck:

1. Inspect the topic and source material.
2. Propose a slide outline.
3. For each slide, define:
   - Title.
   - Core message.
   - Visual metaphor or infographic type.
   - Data or formula needed.
   - Speaker-note idea when useful.
4. Implement the Reveal.js HTML deck.
5. Run local checks.
6. Confirm the final output is HTML.
7. Mention export options only after HTML works.

## Local Verification

Before finishing deck work, verify:

- The deck opens locally.
- There are no missing assets.
- The visual style is consistent.
- The dotted-grid background is faint.
- Typography is consistent.
- Every slide has a clear message.
- At least half the slides contain meaningful visual structure.
- Infographics are semantic, not decorative.
- No proprietary tooling is required.
- No AI-looking art is included.
- No slide looks like a generic startup pitch deck.
- The final deck can be edited by changing text, code, CSS, SVG, or data specs.

## Agent Behavior

- Inspect the repository before making structural assumptions.
- Preserve existing project conventions once they exist.
- Keep edits narrow and purposeful.
- Prefer reusable CSS classes and small diagram components over one-off inline clutter.
- Do not add decorative visuals just to make a slide feel full.
- When a visual is weak, simplify the slide before adding ornament.
- Run the available local checks before claiming completion.
- Report any check that could not be run and why.
