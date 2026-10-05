---
name: pkgame-month-theme-studio
description: "Create or revise PK.GAME images and icons using the current visual theme, with operator-specified subjects, image ratio and width, and optional style, color, copy and branding overrides."
metadata:
  version: "1.0.1"
---

# PK.Game Month Theme Studio

Make artwork for any use. The operator chooses **image** or **icon**; do not restrict work to signup, Casino, Sports, homepage, or any other placement. Use [the current theme](references/current-theme.json) as an adjustable default. Reply in the operator's language; artwork copy follows the operator's supplied wording or separately requested language.

## Collect a small brief

Reuse information in the current request, attached assets, and conversation. Natural language is sufficient; IDs and forms are not required.

| Input | Rule |
|---|---|
| Output type | Image or icon; infer it when already explicit in the request. |
| Image dimensions | Require aspect ratio and target width in pixels. Derive the height. Explicit width and height also supply a ratio; do not ask again. For multiple ratios, obtain or reuse the requested width for each. |
| Icon dimensions | Default to 1:1, 1024 x 1024, transparent PNG unless the operator specifies another size, shape or background. State these defaults briefly. |
| Content | Ask what the theme is and which main elements must appear. A supplied description such as "a football with boots" already answers this. Do not infer mandatory people, chips, gems, Rio scenery, or a specific game from the visual references. |
| Optional controls | Rendering style, colors, mood, references, copy, branding, composition, output format, and variant count. Apply supplied choices; do not require the operator to fill every field. |

Bundle material missing inputs into one short question. An image request with no ratio or width needs those values before generation. An icon request does not need an extra dimensions question when the defaults work. Do not require a placement, market, CTA, provider, or campaign date unless the actual task needs it.

If the calculated image height is fractional, state the nearest whole-pixel height and resulting approximate ratio before proceeding. Keep the requested width. If an exact mathematical ratio is essential, resolve incompatible dimensions with the operator. Never quietly switch to a historical preset such as 4.9:1 or 2.13:1.

Default to one variant unless a count or comparison is requested. A complete brief plus "generate" / "make it" authorizes generation; no extra confirmation is needed. "Brief only" / "confirm the approach first" means provide the brief and wait. A request to see the style should display relevant bundled references without generating new artwork.

## Apply the theme and operator overrides

Read `references/current-theme.json` and view a relevant bundled style image before generation. These references guide rendering and color, not the subject, layout, copy, identity, clothing, brand, or destination of every output. The theme name describes the default mood; it does not require Brazil, nighttime, or a particular location.

The current operator request takes precedence over the theme defaults. Users may adjust or replace the overall style, palette, subject, lighting, or background during ordinary use. Preserve other approved choices while making the requested revision. Do not force B01/B02/B03 or P/S/T menus from other skills into this workflow.

Summarize the effective brief in one short line: type, dimensions, subject/elements, theme plus any overrides, and branding/text treatment. Continue directly if generation is authorized.

**Branding is optional.** Default to adding no extra PK.GAME, provider, sponsor, or other logo. When requested, add the named brand using the supplied or verified original asset, and follow the requested size and location. A provider-themed image does not itself mandate a logo. Do not inherit a logo solely because it appears in a style reference. For a production final, preserve original logo geometry in a separate layer or exact compositing step; label any generated approximation and unresolved finishing limitation.

No copy is the default when none is supplied. Preserve approved copy exactly when requested. Do not invent bonuses, rankings, dates, odds, or winning outcomes. Only ask for language or wording when needed for requested text. Real interaction buttons remain separate from artwork unless the user explicitly requests an illustrative mockup.

## Compose for this request

- Images: arrange the supplied subject and elements for the requested canvas. Without an overlay requirement, use the whole composition; do not reserve arbitrary empty thirds or darken the right side by default.
- If the operator supplies a text/button layout, account for it with subject placement, calm background regions and local gradients as needed. Do not borrow signup-specific left-copy/right-button rules for unrelated images.
- Multiple ratios: retain subject identity, visual treatment and approved content, but recompose each ratio. Check important faces, hands, props and text at every requested size rather than stretching or blindly cropping one export.
- Icons: keep a clear silhouette and limited detail, about 12% safe margin by default, and no text unless requested. Translate the selected style into an isolated subject instead of placing a miniature full scene inside a square. Check actual alpha transparency and small-size legibility.

## Generate, inspect and deliver

Use the environment's available built-in image generation/editing capability and follow its instructions. Clearly identify edit targets, style references, subject references, and original brand assets. Do not replace requested generated art with a code-drawn placeholder. If generation is unavailable, state that limitation rather than claiming success.

Inspect subject accuracy, anatomy where relevant, requested elements, text/logo fidelity, clipping, background treatment, dimensions and transparency. Fix material issues with focused revisions; default to at most two correction generations per requested asset, honoring a lower operator limit. Report any remaining defect rather than silently continuing to generate.

Distinguish native generation resolution from final delivered dimensions. Deliver the requested width and calculated height using an appropriate export/recomposition workflow without stretching important content; explicitly identify a remaining size or finishing mismatch. Do not call an unchecked output production-ready.

Save artwork with non-destructive version names, the actual prompt, effective brief, theme version, operator overrides, dimensions and relevant source notes in the current workspace. Show the result with usable file links. Keep full prompt details in the delivery files instead of a long chat response.

## Defaults and team portability

Ordinary adjustments affect the current task only. Update the bundled shared defaults only when the user explicitly asks to update the default style or publish a new theme version. Keep the workflow stable; update the theme record and relevant visual references. A local change does not update teammates' installed copies.

Resolve references and assets relative to this skill folder. It must work without the creator's paths, browser storage, website prototype, or earlier chat. Package revisions are snapshots; do not promise automatic team synchronization. Creating artwork does not itself authorize website/Figma edits, tickets, uploads, or messages.

For usage examples, read [operator examples](references/operator-examples.md).
