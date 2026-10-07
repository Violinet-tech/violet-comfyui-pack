# Violet ComfyUI pack

> **This repository is archived.** The pack now lives in [Violinet-tech/solar-violet-nodes](https://github.com/Violinet-tech/solar-violet-nodes), which also bundles the image to image workflows. Use that one.

A ComfyUI custom-node pack from [VIOLINET Tech](https://github.com/Violinet-tech): a LoRA loader that shows what you have loaded, and a model and LoRA browser that finds duplicates, fetches CivitAI details and works across every model folder ComfyUI knows about.

## What is in it

- **LoRA loader node.** Stacked LoRAs as strips with preview, base model, trigger words and a strength slider each. Search by name or trigger word, reorder, enable or disable, and the node grows as you load more. The strip size, text size and spacing are adjustable (the **Aa** button).
- **Violet LoRA Browser** (`Ctrl+Alt+L`) and **Violet Model Browser** (`Ctrl+Alt+M`). Click to select, Shift-click for a range, hover for a card. Move to folder with undo, organize loose files by what their metadata says they are, Recycle bin or permanent delete.
- **Duplicate finder.** Identical files, the same CivitAI model across versions, and names that match once version, epoch and precision tags are stripped. Tick suggested, Shift-click a range, and a guard that never lets you remove every copy.
- **Every ComfyUI model folder.** Checkpoints, diffusion models, GGUF, VAE and text encoders are tabs; every other folder ComfyUI or your nodes register (`controlnet`, `clip_vision`, `upscale_models`, `ipadapter`, ...) is in the **More ComfyUI folders** list. **Folders / settings** adds extra paths for any of them, applied at once with no restart.
- **Model libraries.** Use a Stability Matrix or any other model tree as it is, with no moving or symlinks.
- **Network sources.** Browse another computer's ComfyUI models (browse only) over its stock API.
- **Typed model loaders, Violet Text Encoder** (presets and an optional LLM enhancer), **image tools** (Save Image, Size + Resize, Image Compare). See [docs/NODE_REFERENCE.md](docs/NODE_REFERENCE.md).
- **Example workflows** for image to image, including a low VRAM one.

## Install

Clone into ComfyUI's `custom_nodes` folder and restart ComfyUI:

```
cd ComfyUI/custom_nodes
git clone https://github.com/Violinet-tech/violet-comfyui-pack.git
```

Or download the zip from [Releases](https://github.com/Violinet-tech/violet-comfyui-pack/releases) and unpack it there. Requires a current ComfyUI frontend. GGUF loading needs [ComfyUI-GGUF](https://github.com/city96/ComfyUI-GGUF).

## Notes

- CivitAI lookups are by file hash and cached next to each file as `<name>.violet.json`. Add a CivitAI key in the text encoder settings if you want your own rate limit.
- Removed files go to the Recycle bin, a `_violet_duplicates` folder next to them, or are deleted, whichever button you press. Nothing is removed until you confirm.

## License

MIT, see [LICENSE](LICENSE).
