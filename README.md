# AI Design Skills: VegaShares edition

A fork of [elayadesign/ai-design-skills](https://github.com/elayadesign/ai-design-skills), adapted to the VegaShares ETFs brand (Poppins, Vega Blue `#0055FF`, Deep Navy `#0A0E27`) with ETF marketing guardrails: no invented fund data, disclosures never rewritten, and every public string treated as a draft for compliance review.

## Skills

| Skill | What it does |
|---|---|
| [`vega-landing-page-design`](./skills/vega-landing-page-design/SKILL.md) | Builds VegaShares fund pages, launch and campaign pages, and education pages: intake, structure, copy, and the brand visual system |
| [`vega-design-to-motion`](./skills/vega-design-to-motion/SKILL.md) | Turns a static VegaShares design (Figma, Canva export, site section) into an animated loop, exported as MP4 and GIFs, with a square option for social |

The brand values live in the **VegaShares brand** block of `vega-landing-page-design` and in the **VegaShares rules** and **Make it yours** sections of `vega-design-to-motion`. If the brand guide changes, update those sections.

This repo is public, so it holds only public brand values. Internal file locations and house rules come from the VegaShares project's own CLAUDE.md, which the skills point to.

## Install (Windows, Claude Code)

The skills are linked into the VegaShares project folder with junctions, so edits here take effect immediately:

```powershell
$repo = "C:\CLAUDE COWORK\Projects\VCP\ai-design-skills-vega\skills"
$dest = "C:\CLAUDE COWORK\Projects\VCP\.claude\skills"
foreach ($s in "vega-landing-page-design","vega-design-to-motion") {
  cmd /c mklink /J "$dest\$s" "$repo\$s"
}
```

`vega-design-to-motion` needs ffmpeg for exports (`choco install ffmpeg`) and Playwright for frame capture.

## Pulling upstream updates

```bash
git fetch upstream
git merge upstream/main
```

Upstream changes land in the original folder names (`skills/landing-page-design`, `skills/design-to-motion`); copy anything useful into the `vega-` versions by hand.

## License

MIT, as upstream. Credits for adapted material are at the end of each SKILL.md.
