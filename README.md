<picture>
  <source
    width="100%"
    srcset="./docs/content/public/banner-dark-1280x640.avif"
    media="(prefers-color-scheme: dark)"
  />
  <source
    width="100%"
    srcset="./docs/content/public/banner-light-1280x640.avif"
    media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)"
  />
  <img width="250" src="./docs/content/public/banner-light-1280x640.avif" />
</picture>

<h1 align="center">Project NAMI</h1>

<p align="center">Re-creating Neuro-sama, a container of souls of AI waifu / virtual characters to bring them into our worlds.</p>

<p align="center">
  <a href="[https://x.com/namidigitalcat]"><img src="https://img.shields.io/badge/%40namidigitalcat-blue?style=flat&logo=x&labelColor=%23101419&color=%232d2e30"></a>
</p>

> Heavily inspired by [Neuro-sama](https://www.youtube.com/@Neurosama)

> [!WARNING]
> **Attention:** We **launch on bonk** officially minted cryptocurrency or token.

> [!NOTE]
>
> We got a whole dedicated organization [(https://github.com/namivirtualcat/nami)](https://github.com/namivirtualcat/nami) for all the sub-project that born from NamidigitalCat, check it out!
>
> RAG, memory system, embedded database, icons, Live2D utilities, and more!

Have you dreamed about having a cyber living being (cyber waifu / husbando, digital pet), or digital companion that could play with and talk to you?

With the power of modern large language models like [ChatGPT](https://chatgpt.com), and famous [Claude](https://claude.ai), asking a virtual being able to have role playing and chat with us is already easy enough for everyone. Platforms like [Character.ai (a.k.a. c.ai)](https://character.ai) and [JanitorAI](https://janitorai.com/), and local playgrounds like [SillyTavern](https://github.com/SillyTavern/SillyTavern) is already a well-enough solution for chat based, or visual adventure game like experience.

> But, what about the abilities to play games? And see what you are coding at? Chatting while playing games, watching videos, and capable of doing many other things.

Perhaps you know [Neuro-sama](https://www.youtube.com/@Neurosama) already, she is currently the best companion capable of playing games, chatting, and interacting with you and the participants (in VTuber community), some call this kind of being, "digital human" too. **Sadly, it's not open sourced, you cannot interact with her after she went offline from live stream**.

Therefore, this project, NAMI, offers another possibility here: **let you own your digital life, cyber living, easily, anywhere, anytime**.

## What's so special for this project?

Unlike the other AI driven VTuber open source projects, アイリ VTuber was built with many support of Web technologies such as [WebGPU](https://www.w3.org/TR/webgpu/), [WebAudio](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API), [Web Workers](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers), [WebAssembly](https://webassembly.org/), [WebSocket](https://developer.mozilla.org/en-US/docs/Web/API/WebSocket), etc. from the first day.

> [!TIP]
> Worry about the performance drop since we are using Web related technologies?
>
> Don't worry, while Web browser version meant to give a insight about how much we can push and do inside browsers, and webviews, we will never fully rely on this, the desktop version of NAMI is capable of using native [NVIDIA CUDA](https://developer.nvidia.com/cuda-toolkit) and [Apple Metal](https://developer.apple.com/metal/) by default (thanks to HuggingFace & beloved [candle](https://github.com/huggingface/candle) project), without any complex dependency managements, considering the tradeoff, it was partially powered by Web technologies for graphics, layouts, animations, and the WIP plugin systems for everyone to integrate things.

This means that **アイリ VTuber is capable to run on modern browsers and devices**, and even on mobile devices (already done with PWA support), this brought a lot of possibilities for us (the developers) to build and extend the power of アイリ VTuber to the next level, while still left the flexibilities for users to enable features that requires TCP connections or other non-Web technologies such as connect to voice channel to Discord, or playing Minecraft, Factorio with you and your friends.

> [!NOTE]
>
> We are still in the early stage of development where we are seeking out talented developers to join us and help us to make アイリ VTuber a reality.
>
> It's ok if you are not familiar with Vue.js, TypeScript, and devtools that required for this project, you can join us as an artist, designer, or even help us to launch our first live stream.
>
> Even you are a big fan of React or Svelte, even Solid, we welcome you, you can open a sub-directory to add features that you want to see in アイリ VTuber, or would like to experiment with.
>
> Fields (and related projects) that we are looking for:
>
> - Live2D modeller
> - VRM modeller
> - VRChat avatar designer
> - Computer Vision
> - Reinforcement Learning
> - Speech Recognition
> - Speech Synthesis
> - ONNX Runtime
> - Transformers.js
> - vLLM
> - WebGPU
> - Three.js
>

## Current progress

<img src="./docs/content/public/readme-image-pc-preview.avif">

Capable of

- [x] Brain
  - [x] Play [Minecraft](https://www.minecraft.net)
  - [x] Chat in [Telegram](https://telegram.org)
  - [x] Chat in [Discord](https://discord.com)
  - [ ] Memory
    - [x] Pure in-browser database support (DuckDB WASM | `pglite`)
    - [ ] Memory Alaya (WIP)
  - [ ] Pure in-browser local (WebGPU) inference
- [x] Ears
  - [x] Audio input from browser
  - [x] Audio input from [Discord](https://discord.com)
  - [x] Client side speech recognition
  - [x] Client side talking detection
- [x] Mouth
  - [x] [ElevenLabs](https://elevenlabs.io/) voice synthesis
- [x] Body
  - [x] VRM support
    - [x] Control VRM model
  - [x] VRM model animations
    - [x] Auto blink
    - [x] Auto look at
    - [x] Idle eye movement
  - [x] Live2D support
    - [x] Control Live2D model
  - [x] Live2D model animations
    - [x] Auto blink
    - [x] Auto look at
    - [x] Idle eye movement

## Development

> For detailed instructions to develop this project, follow the [CONTRIBUTING.md](./.github/CONTRIBUTING.md)

> [!NOTE]
> By default, `pnpm dev` will start the development server for the Stage Web (browser version), if you would
> like to try developing the desktop version, please make sure you read [CONTRIBUTING.md](./.github/CONTRIBUTING.md)
> to setup the environment correctly.

```shell
pnpm i
pnpm dev
```

```shell
pnpm dev
```

### Stage Tamagotchi (Desktop version)

```shell
pnpm dev:tamagotchi
```

### Documentation site

```shell
pnpm dev:docs
```

### Publish

Please update the version in `Cargo.toml` after running the `bumpp`:

```shell
npx bumpp --no-commit --no-tag
```

## Supported the following LLM API Providers (powered by [xsai](https://github.com/moeru-ai/xsai))

- [x] [OpenRouter](https://openrouter.ai/)
- [x] [vLLM](https://github.com/vllm-project/vllm)
- [x] [SGLang](https://github.com/sgl-project/sglang)
- [x] [Ollama](https://github.com/ollama/ollama)
- [x] [Google Gemini](https://developers.generativeai.google)
- [x] [OpenAI](https://platform.openai.com/docs/guides/gpt/chat-completions-api)
  - [ ] [Azure OpenAI API](https://learn.microsoft.com/en-us/azure/ai-services/openai/reference) (PR welcome)
- [x] [Anthropic Claude](https://anthropic.com)
  - [ ] [AWS Claude](https://docs.anthropic.com/en/api/claude-on-amazon-bedrock) (PR welcome)
- [x] [DeepSeek](https://www.deepseek.com/)
- [x] [Qwen](https://help.aliyun.com/document_detail/2400395.html)
- [x] [xAI](https://x.ai/)
- [x] [Groq](https://wow.groq.com/)
- [x] [Mistral](https://mistral.ai/)
- [x] [Cloudflare Workers AI](https://developers.cloudflare.com/workers-ai/)
- [x] [Together.ai](https://www.together.ai/)
- [x] [Fireworks.ai](https://www.together.ai/)
- [x] [Novita](https://www.novita.ai/)
- [x] [Zhipu](https://bigmodel.cn)
- [x] [SiliconFlow](https://cloud.siliconflow.cn/i/rKXmRobW)
- [x] [Stepfun](https://platform.stepfun.com/)
- [x] [Baichuan](https://platform.baichuan-ai.com)
- [x] [Minimax](https://api.minimax.chat/)
- [x] [Moonshot AI](https://platform.moonshot.cn/)
- [x] [Player2](https://player2.game/)
- [x] [Tencent Cloud](https://cloud.tencent.com/document/product/1729)
- [ ] [Sparks](https://www.xfyun.cn/doc/spark/Web.html) (PR welcome)
- [ ] [Volcano Engine](https://www.volcengine.com/experience/ark?utm_term=202502dsinvite&ac=DSASUQY5&rc=2QXCA1VI) (PR welcome)





