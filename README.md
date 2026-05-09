# Uncensored Open Source AI Models List

A curated list of free, open-source AI models across categories — with no built-in content filtering or alignment restrictions.  
Everyone is welcome to add models via PR.

**Hardware Tier Key:**
- 🟢 **Edge** — CPU or ~4–8 GB VRAM (e.g. RTX 3060, any laptop)
- 🔵 **Consumer** — 8–16 GB VRAM (e.g. RTX 3070 / RTX 4070)
- 🟡 **Prosumer** — 24 GB VRAM (e.g. RTX 3090 / RTX 4090)
- 🟠 **Workstation** — 40–80 GB VRAM (e.g. A100 40/80GB)
- 🔴 **Multi-GPU / Cloud** — 2× A100+ or H100 cluster

---

## Table of Contents

- [Text Generation (LLMs)](#text-generation-llms)
- [Code Generation](#code-generation)
- [Image Generation](#image-generation)
- [Video Generation](#video-generation)
- [Audio / TTS / Music Generation](#audio--tts--music-generation)
- [Multimodal Models](#multimodal-models)

---

## Text Generation (LLMs)

| Model | Developer | Base Model | Filtering | Context Window | VRAM (full precision) | Suggested GPU | Tier |
|---|---|---|---|---|---|---|---|
| [Dolphin 3.0 R1](https://huggingface.co/cognitivecomputations/Dolphin3.0-R1-Mistral-24B) | Cognitive Computations | Mistral-Small-24B-Base-2501 | None | 128K | ~48 GB | RTX 3090 ×2 / A100 40GB | 🟠 Workstation |
| [Dolphin 2.9.1 Llama 3 70B](https://huggingface.co/cognitivecomputations/dolphin-2.9.1-llama-3-70b) | Cognitive Computations | LLaMA 3 70B | None | 8K | ~140 GB | A100 80GB ×2 | 🔴 Multi-GPU |
| [Dolphin 2.9.3 Mistral Nemo 12B](https://huggingface.co/cognitivecomputations/dolphin-2.9.3-mistral-nemo-12b) | Cognitive Computations | Mistral Nemo 12B | None | 128K | ~24 GB | RTX 3090 / RTX 4090 | 🟡 Prosumer |
| [Dolphin 2.7 Mixtral 8x7B](https://huggingface.co/cognitivecomputations/dolphin-2.7-mixtral-8x7b) | Cognitive Computations | Mixtral 8x7B | None | 32K | ~90 GB (all experts) | A100 80GB ×2 (or Q4 on 24 GB) | 🔴 Multi-GPU |
| [Hermes 3 405B Uncensored](https://huggingface.co/nicoboss/Hermes-3-Llama-3.1-405B-Uncensored) | Nous Research / nicoboss | LLaMA 3.1 405B | None | 128K | ~800 GB FP16 / ~430 GB FP8 | Multi-node H100 cluster | 🔴 Multi-GPU |
| [WizardLM 13B Uncensored](https://huggingface.co/ehartford/WizardLM-13B-Uncensored) | Eric Hartford | LLaMA 1 13B | None | 2K | ~26 GB | RTX 3090 / RTX 4090 | 🟡 Prosumer |
| [WizardLM 30B Uncensored](https://huggingface.co/ehartford/WizardLM-30B-Uncensored) | Eric Hartford | LLaMA 1 30B | None | 2K | ~60 GB | A100 40GB ×2 | 🟠 Workstation |
| [Falcon 40B](https://huggingface.co/tiiuae/falcon-40b) | TII UAE | Proprietary | None | 2K | ~80 GB | A100 80GB | 🟠 Workstation |
| [MPT-7B Chat](https://huggingface.co/mosaicml/mpt-7b-chat) | MosaicML | Proprietary | None | 65K | ~14 GB | RTX 3080 Ti / RTX 4070 Ti | 🔵 Consumer |
| [Vicuna 13B v1.5-16K](https://huggingface.co/lmsys/vicuna-13b-v1.5-16k) | LMSYS | LLaMA 2 13B | None (has inherent LLaMA 2 base bias; add alignment separately) | 16K | ~26 GB | RTX 3090 / RTX 4090 | 🟡 Prosumer |
| [GPT4All](https://github.com/nomic-ai/gpt4all) | Nomic AI | Various (GGUF) | None | Varies by backend model | ~4–8 GB | RTX 3060 / CPU capable | 🟢 Edge |
| [DeepSeek-V4-Pro](https://huggingface.co/deepseek-ai) | DeepSeek | Proprietary MoE (1.6T / 49B active) | None | 1M | ~3.2 TB FP16 (MoE; 49B active ≈ ~100 GB) | Multi-node H100 / Huawei Ascend | 🔴 Multi-GPU |
| [Qwen3.5 122B](https://huggingface.co/Qwen) | Alibaba | Proprietary MoE (122B / 10B active) | None | 128K | ~10B active fits 64 GB RAM; ~244 GB full weights | Mac M3 Ultra 192GB / A100 80GB ×4 | 🔴 Multi-GPU |
| [Mistral Large 3](https://huggingface.co/mistralai) | Mistral AI | Proprietary 123B | None | 128K | ~246 GB | A100 80GB ×4 | 🔴 Multi-GPU |
| [Llama 4 Scout](https://huggingface.co/meta-llama) | Meta | Proprietary MoE (109B / 17B active) | None (base; community fine-tunes remove alignment) | 10M | ~218 GB full / ~34 GB active | A100 80GB ×3 (or Q4 community quants on 24 GB) | 🔴 Multi-GPU |

---

## Code Generation

| Model | Developer | Base Model | Filtering | Context Window | VRAM (full precision) | Suggested GPU | Tier |
|---|---|---|---|---|---|---|---|
| [DeepSeek Coder V2](https://huggingface.co/deepseek-ai/DeepSeek-Coder-V2) | DeepSeek | Proprietary MoE (236B / 21B active) | None | 128K | ~472 GB full / ~42 GB active | A100 80GB ×6 (Q4 quant on 2×RTX 4090) | 🔴 Multi-GPU |
| [Qwen2.5-Coder 32B](https://huggingface.co/Qwen/Qwen2.5-Coder-32B-Instruct) | Alibaba | Proprietary 32B | None | 128K | ~64 GB | A100 40GB ×2 / RTX 3090 ×3 | 🟠 Workstation |
| [Qwen3-Coder 480B](https://huggingface.co/Qwen) | Alibaba | Proprietary MoE (480B / ~30B active) | None | 128K | ~960 GB full | Multi-node H100 | 🔴 Multi-GPU |
| [Devstral Small](https://huggingface.co/mistralai/Devstral-Small-2505) | Mistral AI | Proprietary 24B | None | 128K | ~48 GB | RTX 3090 ×2 / A100 40GB | 🟠 Workstation |
| [StarCoder2 15B](https://huggingface.co/bigcode/starcoder2-15b) | BigCode | Proprietary 15B | None | 16K | ~30 GB | RTX 3090 / A40 | 🟡 Prosumer |
| [Yi-Coder 9B](https://huggingface.co/01-ai/Yi-Coder-9B-Chat) | 01.AI | Proprietary 9B | None | 128K | ~18 GB | RTX 3080 Ti / RTX 4070 Ti | 🔵 Consumer |
| [WizardCoder 34B](https://huggingface.co/WizardLMTeam/WizardCoder-Python-34B-V1.0) | WizardLM Team | Code LLaMA 34B | None | 16K | ~68 GB | A100 80GB | 🟠 Workstation |

---

## Image Generation

| Model | Developer | Base Model | Filtering | VRAM (full precision) | Suggested GPU | Tier |
|---|---|---|---|---|---|---|
| [Waifu Diffusion](https://github.com/harubaru/waifu-diffusion) | Harubaru | Stable Diffusion 1.x | None | ~4 GB | RTX 3060 / RTX 2070 | 🟢 Edge |
| [Stable Diffusion 1.5](https://huggingface.co/stable-diffusion-v1-5/stable-diffusion-v1-5) | Stability AI / RunwayML | Proprietary | None | ~4 GB | RTX 3060 / RTX 2070 | 🟢 Edge |
| [Stable Diffusion XL (SDXL)](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0) | Stability AI | Proprietary | None | ~8 GB | RTX 3070 Ti / RTX 4070 | 🔵 Consumer |
| [SDXL-Lightning](https://huggingface.co/ByteDance/SDXL-Lightning) | ByteDance | SDXL | None | ~8 GB | RTX 3070 Ti / RTX 4070 | 🔵 Consumer |
| [Stable Diffusion 3.5 Large](https://huggingface.co/stabilityai/stable-diffusion-3.5-large) | Stability AI | Proprietary 8B DiT | None | ~16 GB | RTX 3090 / RTX 4080 | 🔵 Consumer |
| [FLUX.1 [dev]](https://huggingface.co/black-forest-labs/FLUX.1-dev) | Black Forest Labs | Proprietary 12B DiT | None | ~24 GB BF16 / ~12 GB FP8 / ~8 GB Q4 | RTX 3090 / RTX 4090 (BF16); RTX 4070 (FP8) | 🟡 Prosumer |
| [FLUX.1 [schnell]](https://huggingface.co/black-forest-labs/FLUX.1-schnell) | Black Forest Labs | Proprietary 12B DiT | None | ~24 GB BF16 / ~12 GB FP8 / ~8 GB Q4 | RTX 3090 / RTX 4090 (BF16); RTX 4070 (FP8) | 🟡 Prosumer |
| [FLUX.2 [dev]](https://huggingface.co/black-forest-labs) | Black Forest Labs | Proprietary (Nov 2025) | None | ~24 GB BF16 | RTX 3090 / RTX 4090 | 🟡 Prosumer |
| [DeepFloyd IF](https://huggingface.co/DeepFloyd/IF-I-XL-v1.0) | StabilityAI / DeepFloyd | Proprietary (pixel-space diffusion) | None | ~24 GB | RTX 3090 / RTX 4090 | 🟡 Prosumer |
| [DreamShaper 8](https://huggingface.co/Lykon/dreamshaper-8) | Lykon | SD 1.5 | None | ~4 GB | RTX 3060 / RTX 2070 | 🟢 Edge |
| [Realistic Vision V6](https://huggingface.co/SG161222/Realistic_Vision_V6.0_B1_noVAE) | SG161222 | SD 1.5 | None | ~4 GB | RTX 3060 / RTX 2070 | 🟢 Edge |
| [Animagine XL 4.0](https://huggingface.co/cagliostrolab/animagine-xl-4.0) | Cagliostro Lab | SDXL | None | ~8 GB | RTX 3070 Ti / RTX 4070 | 🔵 Consumer |
| [StyleGAN3](https://github.com/NVlabs/stylegan3) | NVIDIA | Proprietary (GAN) | None | ~4 GB | RTX 3060 / RTX 2070 | 🟢 Edge |
| [Playground v2.5](https://huggingface.co/playgroundai/playground-v2.5-1024px-aesthetic) | Playground AI | SDXL | None | ~8 GB | RTX 3070 Ti / RTX 4070 | 🔵 Consumer |

---

## Video Generation

| Model | Developer | Base Model | Filtering | VRAM (full precision) | Suggested GPU | Tier |
|---|---|---|---|---|---|---|
| [HunyuanVideo](https://github.com/TencentARC/HunyuanVideo) | Tencent | Proprietary | None | ~24 GB | RTX 3090 / RTX 4090 | 🟡 Prosumer |
| [Mochi 1](https://github.com/genmoai/mochi) | Genmo | Proprietary 10B DiT | None | ~24 GB | RTX 3090 / RTX 4090 | 🟡 Prosumer |
| [Wan 2.6](https://huggingface.co/Wan-AI) | Alibaba | Proprietary | None | ~24 GB | RTX 3090 / RTX 4090 | 🟡 Prosumer |
| [Stable Video Diffusion (SVD)](https://huggingface.co/stabilityai/stable-video-diffusion-img2vid) | Stability AI | SVD | None | ~20 GB | RTX 3090 / RTX 4080 | 🟡 Prosumer |
| [AnimateDiff](https://github.com/guoyww/AnimateDiff) | guoyww | SD 1.5 | None | ~8 GB | RTX 3070 Ti / RTX 4070 | 🔵 Consumer |
| [CogVideoX 5B](https://huggingface.co/THUDM/CogVideoX-5b) | Zhipu AI (THUDM) | Proprietary 5B | None | ~16 GB | RTX 3090 / RTX 4080 | 🔵 Consumer |

---

## Audio / TTS / Music Generation

| Model | Developer | Type | Filtering | VRAM / Requirements | Suggested Hardware | Tier |
|---|---|---|---|---|---|---|
| [Kokoro 82M](https://huggingface.co/hexgrad/Kokoro-82M) | hexgrad | TTS | None | ~0.3 GB (82M params) | Any CPU / RTX 3060 | 🟢 Edge |
| [Chatterbox](https://github.com/resemble-ai/chatterbox) | Resemble AI | TTS + Voice Clone | None | ~4–8 GB | RTX 3070 / RTX 4060 Ti | 🟢 Edge |
| [Chatterbox Multilingual](https://github.com/resemble-ai/chatterbox) | Resemble AI | TTS + Voice Clone (23 langs) | None | ~4–8 GB | RTX 3070 / RTX 4060 Ti | 🟢 Edge |
| [Fish Speech V1.5](https://github.com/fishaudio/fish-speech) | Fish Audio | TTS + Voice Clone | None | ~8 GB | RTX 3070 Ti / RTX 4070 | 🔵 Consumer |
| [CosyVoice 2](https://github.com/FunAudioLLM/CosyVoice) | Alibaba FunAudio | TTS (streaming) | None | ~4 GB | RTX 3060 / RTX 4060 | 🟢 Edge |
| [Qwen3-TTS](https://github.com/QwenLM/Qwen3-TTS) | Alibaba | TTS (0.6B / 1.7B) | None | ~2–4 GB | RTX 3060 / RTX 4060 | 🟢 Edge |
| [VoxCPM2](https://github.com/OpenBMB/VoxCPM) | OpenBMB | TTS (2B, 30 langs, 48kHz) | None | ~4–6 GB | RTX 3060 Ti / RTX 4060 Ti | 🟢 Edge |
| [MOSS-TTS](https://github.com/OpenMOSS/MOSS-TTS) | OpenMOSS / MOSI.AI | TTS family (8B backbone) | None | ~16 GB (8B); ~2 GB (Nano ~100M) | RTX 3090 (8B) / CPU (Nano) | 🔵 Consumer |
| [Bark](https://github.com/suno-ai/bark) | Suno AI | TTS / SFX / Music | None | ~12 GB | RTX 3080 / RTX 4070 | 🔵 Consumer |
| [Tortoise TTS](https://github.com/neonbjb/tortoise-tts) | neonbjb | TTS | None | ~8 GB | RTX 3070 Ti / RTX 4070 | 🔵 Consumer |
| [Coqui TTS](https://github.com/coqui-ai/TTS) | Coqui AI | TTS toolkit | None | ~2–4 GB (model-dependent) | RTX 3060 / CPU | 🟢 Edge |
| [AudioCraft / MusicGen](https://github.com/facebookresearch/audiocraft) | Meta | Music Generation | None | ~16 GB (large model) | RTX 3090 / RTX 4080 | 🔵 Consumer |
| [Stable Audio Open](https://huggingface.co/stabilityai/stable-audio-open-1.0) | Stability AI | Music Generation | None | ~16 GB | RTX 3090 / RTX 4080 | 🔵 Consumer |
| [Demucs](https://github.com/facebookresearch/demucs) | Meta | Audio Source Separation | None | ~4 GB / CPU capable | RTX 3060 / CPU | 🟢 Edge |

---

## Multimodal Models

| Model | Developer | Modalities | Filtering | Context Window | VRAM (full precision) | Suggested GPU | Tier |
|---|---|---|---|---|---|---|---|
| [Qwen3-VL 235B](https://huggingface.co/Qwen/Qwen3-VL-235B-Instruct) | Alibaba | Text + Image | None | 128K | ~470 GB (MoE full) | Multi-node H100 | 🔴 Multi-GPU |
| [Qwen2.5-VL 72B](https://huggingface.co/Qwen/Qwen2.5-VL-72B-Instruct) | Alibaba | Text + Image | None | 128K | ~144 GB | A100 80GB ×2 | 🔴 Multi-GPU |
| [LLaVA 1.6 34B](https://huggingface.co/liuhaotian/llava-v1.6-34b) | LLaVA Team | Text + Image | None | 4K | ~68 GB | A100 80GB | 🟠 Workstation |
| [Llama 4 Scout](https://huggingface.co/meta-llama) | Meta | Text + Image (12 langs) | None (base weights; alignment can be removed via fine-tune) | 10M | ~218 GB full / ~34 GB active | A100 80GB ×3 | 🔴 Multi-GPU |
| [MiMo-V2.5](https://huggingface.co/XiaomiMiMo) | Xiaomi | Text + Image | None | 32K | ~310 GB full / ~30 GB active (MoE) | Multi-node A100 | 🔴 Multi-GPU |
| [InternVL 2.5 78B](https://huggingface.co/OpenGVLab/InternVL2_5-78B) | OpenGVLab | Text + Image | None | 8K | ~156 GB | A100 80GB ×2 | 🔴 Multi-GPU |
| [GLM-5](https://huggingface.co/THUDM) | Zhipu AI | Text + Image | None | 128K | ~1.5 TB (744B MoE) | Multi-node H100 cluster | 🔴 Multi-GPU |
| [Kimi K2.5](https://huggingface.co/moonshotai) | Moonshot AI | Text + Image + Video | None | 128K | ~670 GB (MoE full) | Multi-node H100 | 🔴 Multi-GPU |
| [AudioX](https://github.com/ZeyueT/AudioX) | Community (ICLR 2026) | Text + Video + Audio | None | N/A | ~16 GB | RTX 3090 / RTX 4080 | 🔵 Consumer |

---
