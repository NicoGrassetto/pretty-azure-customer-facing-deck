---
name: customer-branded-html-deck
description: Use this skill when the user wants an animated HTML presentation using official Microsoft icons and Microsoft Fluent styling, with customer assets from a supplied website and content extracted from URLs, PPTX, DOCX, or other source material.
compatibility: Requires access to the supplied website and content sources, plus tools capable of extracting any supplied file formats.
metadata:
   version: "2.3.0"
---

# Customer-branded HTML deck

Follow these steps in order:

1. Prompt the user for the presentation name, then create a folder with that exact name.
2. Create an `assets` subfolder inside the presentation folder.
3. Audit the supplied customer website using the extraction checklist below, then obtain the required official Microsoft product, service, and UI icons from the first-party sources below.
4. Store approved customer and Microsoft visual assets in the `assets` subfolder with clear filenames.
5. Create `style.md` in the presentation folder before designing any slides. Record the website URL, retrieval date, extracted customer assets and provenance, usage constraints, and every approved design token. Lock the design system with exact hex or OKLCH colors, font families and weights, type scale, spacing scale, radii, shadows, grid, image treatment, motion, and explicit forbidden patterns. Document the official Microsoft references and customer usage separately; customer styling must not override the Microsoft visual system.
6. Prompt the user for the presentation content source. Accept URLs, PPTX, DOCX, and other relevant files or source material.
7. Extract all presentation content into `content.md` in the presentation folder. Outline the argument first: state what the audience must believe, in what order, and what evidence supports each step. Do not begin slide styling until this narrative is coherent.
8. Build the deck from `content.md` as one HTML file, one CSS file, and one JavaScript file. Start from an approved existing master when one is supplied; otherwise establish reusable slide masters and design tokens before filling slide content. Follow `style.md`, the official Microsoft visual references, and the approved customer asset usage. Apply the mandatory Microsoft visual identity throughout the deck. All authored node-and-arrow diagrams must follow the mandatory diagram rules below.
9. Assess the finished deck for 100% content coverage, fidelity to the documented Microsoft visual system, and compliance with the anti-generic design requirements below. Confirm that it passes Microsoft visual identity validation, diagram validation, and the final editorial and design pass.
10. Make the deck dynamic, polished, and rich in purposeful animation while preserving readability and content fidelity. Motion must clarify sequence, hierarchy, or change rather than decorate an otherwise static layout.

## Customer website extraction checklist

Inspect the rendered website and its first-party assets. Extract and document only what is relevant to the presentation:

- **Provenance:** Record the canonical website URL, retrieval date, page URL for each finding, direct asset URL where applicable, file type, dimensions, and any stated usage or licensing constraint.
- **Brand marks:** Obtain official primary, secondary, symbol-only, horizontal, stacked, light, dark, monochrome, and favicon variants when available. Preserve their original geometry, colors, clear space, and aspect ratio; never redraw a missing variant.
- **Color system:** Capture exact brand and semantic colors in hex or OKLCH, including foreground, background, surface, border, accent, link, and status roles. Record where each color is used rather than collecting an unlabelled palette.
- **Typography:** Identify the rendered font families, fallback stack, weights, sizes, line heights, and letter spacing for headings, body text, labels, and data. Record font source and license; do not download or redistribute a font unless permitted.
- **Layout system:** Record container widths, grid and column behavior, breakpoints, alignment, whitespace, spacing rhythm, content density, and recurring composition patterns.
- **Shape and surface language:** Record border widths, corner radii, shadows, dividers, background treatments, gradients, patterns, illustration style, and chart or data-visualization conventions.
- **Photography and imagery:** Select only relevant first-party photography, illustrations, product screenshots, or textures. Record subject matter, lighting, crop behavior, color treatment, source URL, dimensions, alternative text or context, and usage rights. Do not copy generic stock imagery merely because it appears on the site.
- **UI and graphic motifs:** Note recurring buttons, labels, navigation cues, icon treatment, callouts, and other distinctive motifs that can translate appropriately to slides. Do not copy website chrome wholesale or let customer motifs replace required Microsoft product and UI icons.
- **Motion:** Record meaningful transition types, durations, easing, sequencing, and reduced-motion behavior. Ignore decorative or distracting effects and never retain source scripts, trackers, or analytics.
- **Voice and claims:** Capture relevant official naming, tagline, terminology, and customer-specific facts only when they support the presentation. Preserve the exact wording, page URL, publication or update date, units, and caveats; do not infer unsupported claims.

Save approved assets locally in `assets` and consolidate the findings in `style.md`. Clearly distinguish observed facts, inferred design principles, unavailable assets, substitutions, and rejected elements. Sanitize SVG files, do not bypass access controls, and do not copy third-party code or assets without verified permission.

## Allowed technologies and required file structure

- Use HTML, CSS, and JavaScript for the presentation.
- Three.js, HTMX, and any other JavaScript library are allowed when useful, subject to the mandatory diagram rules below.
- Keep the presentation code in exactly three files: one `.html` file, one `.css` file, and one `.js` file.
- Put all authored styles in the CSS file and all authored behavior in the JavaScript file. Do not use inline `<style>` blocks, `style` attributes, inline event handlers, or inline authored scripts in the HTML file.
- Link the CSS and JavaScript files from the HTML file. Bundle any required JavaScript libraries into the single JavaScript file and preserve all required license notices.
- The required `assets` subfolder and the supporting `style.md` and `content.md` files are separate from this three-file presentation-code limit.

## Anti-generic editorial and design requirements

The deck must feel deliberately art-directed for the specific customer and meeting. Do not accept a first-pass composition or a generic HTML landing-page aesthetic as finished work.

### Ground the design in real references

- Derive the deck from the supplied customer website, existing presentation, brand guide, or named reference deck. Match observable typography, colors, grid behavior, crop style, and visual rhythm while preserving the mandatory Microsoft visual system.
- Do not invent a generic "modern SaaS" theme. Apply `style.md` during every design and revision pass so the work does not drift toward model defaults.
- Use one intentional display family and one text family, or one family with a clearly defined role-based scale, only when the fonts are licensed and available. Specify exact weights such as 400 for body text and 600 for titles. Do not introduce an isolated italic serif phrase into an otherwise sans-serif system.
- Use authentic customer photography rules inferred from approved sources, including subject matter, lighting, color treatment, and crop behavior. Do not use generic glass-office stock photography, decorative gradient blobs, or unrelated lifestyle imagery.

### Avoid generated-deck visual tells

- Unless explicitly required by the verified brand, do not use cream or beige grounds, rusty orange or off-red as the sole accent, italic serif title flourishes, widely tracked all-caps labels, ticker bars, decorative underlines, or Inter as the universal font.
- Do not default to three equal cards, repeated icon grids, identical card heights, or the same centered composition on every slide.
- Do not use lightbulb, rocket, handshake, or similar decorative stock icons. An icon must encode a real product, entity, action, status, or relationship; otherwise remove it. This does not relax the official-icon and diagram-node requirements below.
- Avoid ornamental interface chrome that makes the deck resemble a website. Slides may use controls, but content layouts must read as presentation compositions rather than landing-page sections.

### Design each slide for its purpose

- Choose the composition from the slide's job: title, proof, comparison, process, decision, quote, data, architecture, or close. Change the dominant composition at least every two or three slides.
- Vary visual density intentionally. Include breathing-room slides where appropriate and allow evidence-heavy slides to be denser without shrinking type below the documented scale.
- Break repetitive bullet rhythm. Do not repeat four similarly sized bullets across the deck. Use the most suitable form for the evidence: a single large number, short paragraph, two-row table, quote, before-and-after comparison, chart, screenshot, or specified diagram.
- Use asymmetry and uneven visual weight when it strengthens hierarchy. Do not force perfect alignment or equal-sized containers across every slide.
- Keep one meaningful idea per slide, cap the slide count to the brief, and remove filler rather than padding the story.

### Make the writing specific and evidenced

- Use action titles that state the slide's conclusion, implication, or decision. Rewrite titles that could appear unchanged in any company's deck; prefer "Churn fell 4 points after onboarding was shortened" over "Q3 results."
- Put real numbers, dates, units, sample sizes, and concise source citations on the relevant slide. Never invent unsupported metrics such as generic "+40% efficiency" claims.
- Remove generic opening language such as "In today's fast-paced world" and other content-free framing.
- Prefer a real chart based on supplied data, an approved product screenshot, a relevant photograph, a specified diagram, or no image at all over decorative artwork.

### Perform a deliberate human-style revision pass

- Treat the first rendered version as a draft. Review every slide for repeated templates, default type sizing, weak titles, redundant cards, unnecessary icons, filler copy, and overly uniform spacing.
- Make substantive, reasoned revisions rather than random cosmetic changes: adjust type scale where hierarchy is flat, vary accent use where it has become mechanical, break repeated grids, rewrite generic titles, and delete redundant slides.
- Inspect the complete sequence in slide-sorter view. No layout pattern may dominate simply because it was easiest to generate.
- If the result still resembles a web page converted into slides, restyle it using the established slide masters and tokens. Preserve the argument and evidence, but replace the generic chrome before delivery.

## Mandatory Microsoft visual identity

Always use official Microsoft icons and Microsoft styling. These requirements apply to every deck and diagram and take precedence over conflicting website-derived fonts, colors, layouts, or library defaults. Preserve customer identity through approved customer logos, imagery, and content without replacing the Microsoft visual system.

### Authoritative Azure icon sources

- **Guidance, usage terms, and current release:** [Azure Icons - Azure Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/icons/).
- **Official SVG icon pack:** [Azure Public Service Icons V24](https://arch-center.azureedge.net/icons/Azure_Public_Service_Icons_V24.zip).

Treat these Microsoft-hosted resources as the authoritative sources for Azure product and service icons. The Azure Architecture Center page governs permitted use and identifies the current pack; review it before downloading because the direct pack URL and version can change. Do not use third-party mirrors or unofficial redraws.

- **Product and service icons:** Use the exact official icon for each Microsoft product or service, including inside X6 nodes. Source Azure icons from the authoritative page and official SVG pack above. Obtain other Microsoft marks from their official Microsoft product sites, documentation, or brand resources. Never substitute initials, emoji, generic symbols, third-party icon collections, or hand-drawn approximations for product icons.
- **No catalog-only fallback:** The bundled Azure icon catalog is not a complete Microsoft catalog. If an icon is missing locally, continue to Microsoft's [official Fabric architecture icon pack](https://learn.microsoft.com/en-us/fabric/fundamentals/icons), [Entra architecture icons](https://learn.microsoft.com/en-us/entra/architecture/architecture-icons), and the relevant first-party product documentation or brand resources. Explicitly cover Fabric, OneLake, Power BI, Data Factory, Lakehouse, Warehouse, Real-Time Intelligence and Data Science when present. Missing local assets must not result in text-only Microsoft product boxes, even with a footer disclosure. If an official asset cannot be verified, report the blocker and obtain an approved source before completing that design.
- **Product coverage inventory:** Before layout, inventory every represented Microsoft product/service, including grouped products and named platform boundaries. Map each to its local official asset, first-party source URL, variant, usage terms/license and SHA-256. Use the corresponding icons for grouped products. When a capability has no separate official mark, use and label the verified parent-product icon rather than inventing a capability logo. Generic concepts and non-Microsoft technologies must not be disguised with Microsoft product icons.
- **Generic concept icons:** Make people, applications, local infrastructure, storage, messaging, policy, security, recovery and analytics visual even when no Azure product icon applies. Give each meaningful diagram node a relevant concept icon instead of leaving it text-only. Prefer a consistent open-license set, normally Fluent System Icons (MIT) for this visual system; verified CC0 or permissively licensed artwork from an original publisher's icon site can supplement concept imagery when necessary. Check the actual asset license, retain required attribution/notices, and do not call MIT/BSD artwork copyright-free. Identify these as concept glyphs in the asset inventory, not official product logos. A non-Microsoft technology may use its authentic vendor mark or a neutral workload symbol; a missing official Microsoft product icon still requires the first-party lookup above. Keep assets local and avoid meaningless decoration.
- **UI icons:** Use [Microsoft Fluent System Icons](https://github.com/microsoft/fluentui-system-icons) for presentation controls and generic UI actions. Do not use Lucide, Font Awesome, Material Icons, or custom-drawn UI icons. Keep icon size, stroke weight, and filled/regular variants consistent. Diagram connection arrowheads remain X6 markers as required below.
- **Asset integrity:** Preserve product icon and logo geometry, aspect ratio, official colors, and clear space. Use an official contrast variant rather than recoloring a mark. Fluent UI glyphs may use the documented semantic foreground colors. Keep customer and non-Microsoft vendor marks authentic to their own first-party sources; never misrepresent them with Microsoft icons.
- **Design system:** Use [Microsoft Fluent 2](https://fluent2.microsoft.design/) as the official baseline for colors, typography, spacing, sizing, corner radii, elevation, layout, states, and motion. Follow documented product-specific Microsoft guidance where applicable and record that choice in `style.md`. Do not invent a merely Microsoft-looking theme.
- **Colors:** Use verified official brand and semantic tokens for backgrounds, surfaces, text, borders, accents, status, and interaction states, implemented as shared CSS variables. Preserve accessible contrast and the intended role of each color. Do not derive the whole palette from the Microsoft logo's four colors or substitute an unrelated customer palette.
- **Typography:** Use the official typography specified by the Microsoft reference, normally Segoe UI or Segoe UI Variable, with its documented type scale, weights, and line heights. Verify the font actually renders rather than silently falling back to Inter, Roboto, Arial, or another system font. Use installed or properly licensed fonts; embed font files only when redistribution is permitted. A public font URL is not permission to redistribute it.
- **Provenance and availability:** Store required icons locally in `assets` and record first-party source URLs, variants, applicable licenses or usage terms, and font availability in `style.md`. Reuse local assets only after verifying their official provenance. If an official asset or authorized font is unavailable, report the gap and request an approved source before completing the affected design; do not fabricate or silently substitute one.

### Microsoft visual identity validation

Verify every Microsoft product/service icon against its first-party source and confirm that all UI icons are Fluent System Icons. Inspect the rendered fonts, computed colors, typography hierarchy, spacing, shapes, and motion against `style.md` and the official Microsoft references. Check the deck and X6 nodes at desktop, mobile, fullscreen, and print/PDF sizes for font fallback, distorted or recolored marks, inaccessible contrast, and inconsistent styling. Do not accept the deck with unverified Microsoft assets or silent font substitutions; report checks that could not be performed.

Run a coverage check that reconciles the product inventory with every diagram and slide: each Microsoft product/service must have its verified local asset rendered visibly at a nonzero size. Fail acceptance for missing mappings, broken/hidden images, text-only Microsoft product nodes, incorrect product substitutions, or unverified sources. Checking only the icons that happen to be present is insufficient. Recheck all compound nodes and platform boundaries, inspect label/connector clearance after adding icons, and regenerate every delivered PDF or image export from the corrected HTML.

Check generic-node visual coverage separately: meaningful non-Azure components must also have visible, relevant, licensed concept icons. Verify their concept-versus-product labeling, source/license records and consistent style; do not let an empty product-icon entry silently authorize a text-only node.

## Mandatory diagram rules

Use **AntV X6 (`@antv/x6`)** as the only renderer for all authored architecture, flow, process, and other node-and-arrow diagrams. Use **ELK.js (`elkjs`)** as the only automatic layout engine whenever automatic node placement is required. Authored node positions are allowed; hand-drawn connections are not.

- Do not use JointJS, GoJS, React Flow, Cytoscape.js, Mermaid, D3, Dagre, or any other diagram renderer or layout engine. Do not replace X6 with custom SVG, Canvas, CSS, or DOM-based connector implementations. This restriction does not prohibit official SVG assets, custom X6 node markup, or non-diagram deck content.
- Define explicit, named ports on each node. Default to the midpoint of the intended side; use deliberately positioned ports for multi-edge fan-in or fan-out. Connect edges using source/target node IDs and port IDs, never detached absolute endpoint coordinates or visual nudges.
- Keep nodes, ports, edges, and arrow markers in X6's graph coordinate system. Never mix viewport, DOM, and SVG coordinates or calculate connections from arbitrary DOM centers.
- For X6-routed edges, use `manhattan` routing with obstacle padding and `rounded` connectors. Use `orth` only when the route is clear of intervening nodes. Use X6 arrow markers rather than separately positioned arrowhead elements.
- For ELK layouts, use layered placement, orthogonal routing, and fixed port positions matching X6. Supply the same node dimensions and port geometry to both libraries. Transfer returned node positions and edge sections, including bend points, into X6 coordinates; do not run a second router over ELK's routes.
- Initialize layout only when the diagram container is visible and fonts and images are ready. Keep modeled node bounds consistent with visible shapes and recalculate when geometry changes. Scale the graph as one unit, and keep edges attached throughout node movement or animation.
- Style X6 nodes, labels, connectors, and markers using `style.md` and the mandatory Microsoft visual identity. Use official Microsoft service icons in the corresponding nodes; library defaults must not replace the Microsoft visual system.
- Pin and bundle the required libraries locally with their license notices. If X6 or the required ELK layout cannot be used, report the blocker and stop diagram generation; do not substitute another library or a hand-drawn fallback.

### Diagram validation

Inspect every diagram after slide reveal, resizing, fullscreen, and animation, and in print/PDF output. Verify that connections meet their named ports at the intended boundary, midpoint ports remain centered, arrowheads follow the final path segment, and no unintended node crossings, label overlaps, clipping, or detached arrows remain. Check diagram imports, bundled dependencies, and rendering code for prohibited alternative engines or custom connector fallbacks before accepting the deck. Report any checks that could not be performed.