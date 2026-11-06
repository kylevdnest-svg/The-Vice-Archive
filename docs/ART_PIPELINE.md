# Art production pipeline — experiment record

**As of:** 2026-11-06  
**Gate:** Art Test 001 — technical generation verified; style and consistency **NOT accepted**.

## Direction

Goal: an original, mature, expressive indie 2D look with readable eyes, bold outlines, consistent silhouette, flat/restrained shading and a dark theatrical palette. The Coffin of Andy and Leyley is a broad **stylistic reference only**. No copying its specific characters, compositions or copyrighted art.

## Available setup (verified by author screenshots)

- **Krita:** Installed, intended for cleanup, layers, transparency, asset preparation.
- **ComfyUI Desktop:** Installed and running locally.
- **GPU:** NVIDIA RTX 3050, **6GB VRAM**; CUDA/PyTorch detected in ComfyUI logs.
- **Local organisation:** C:\ComfyUi\Comfy Desktop and C:\ComfyUi\Models\checkpoints (user-configured structure). Checkpoint recognition verified via Load Checkpoint dropdown.
- **Working process:** Build/reuse node workflow JSON in ComfyUI rather than manually reconstructing each graph.

## Test history

| Test | Evidence supplied | Result |
| --- | --- | --- |
| ComfyUI local installation / GPU detection | UI screenshots and log showing CUDA RTX 3050 | **PASS** — interface and CUDA visible |
| SD 1.5 baseline | v1-5-pruned-emaonly.safetensors, first 512px generation | **PASS technically**; art result rejected (weak eyes, style and composition) |
| MeinaMix V11 replacement | Generated illustration(s) from same ComfyUI pipeline | **PASS technically**; visually improved, but still generic/decorative and eye quality/identity not approved |
| Simpler prompt revision | Updated character portrait supplied | Improved, still **not accepted final style** |
| Character consistency (expressions/outfit/poses) | No accepted multi-image reference set | **NOT TESTED / NOT PASSED** |
| Reference-guided editing / inpainting for adult art | Proposed local workflow only | **NOT TESTED / NOT PASSED** |
| Commercial licensing / platform compliance of all models | Not fully audited | **PENDING** |

## Proposed economical workflow (not yet verified end to end)

1. Design **original, non-explicit adult characters** with assistant image generation; iterate until a stable reference is author-approved.
2. Save an approved reference sheet with colours, face, eyes, outfit, silhouette and expression cues.
3. Use **local ComfyUI** for controlled variations and inpainting experiments, including adult variations where locally permitted and technically feasible. Do not assume editing can reconstruct unseen anatomy accurately.
4. Use **Krita** for compositing, correction, transparent sprites and export.
5. Track model/checkpoint versions, licenses, prompts, seeds, reference assets, output approvals and modifications.
6. Test same character across a neutral portrait, alternate expression and outfit **before** scaling asset production.

## Artistic and legal acceptance gates

- Author approves character and visual style first; attractive sample alone does not prove consistency.
- Original artwork. Do not copy recognizable character designs or art.
- Eyes, proportions, silhouette and consistent identity are checked on each variant.
- Commercial rights to each model and output assessed; copyright and model terms may vary.
- Verify Steam's **current** adult-content and AI disclosure rules before store use (no assumption that anything generated is automatically accepted).
- Keep promotional content and assets appropriately compliant with their distribution channels.
- Do not claim nude/explicit art pipeline has been validated; it hasn't.

## Next gate — Art Test 001

Create **one approved original adult female character reference**, then test the same character across expressions/outfits with local controlled editing and assess whether the workflow can consistently meet commercial presentation standards. No character name is approved yet.
