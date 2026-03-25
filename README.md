# awesome-free-llm-apis 🧠

> A curated list of **permanently free LLM APIs** — with rate limits, OpenAI SDK compatibility, available SDKs, speed tiers, and free model lists. No trial credits. No time-limited promos. No credit card required.

[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)
![Last Verified](https://img.shields.io/badge/last%20verified-March%202026-brightgreen)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-blue)
![License: CC0](https://img.shields.io/badge/license-CC0-lightgrey)
![Providers](https://img.shields.io/badge/providers-12-orange)

**Keywords:** `free LLM API` · `free AI API` · `OpenAI compatible API` · `free GPT API` · `free Llama API` · `free inference API` · `LLM API key` · `no credit card AI API` · `free tier AI` · `open source LLM hosting`

---

## Why This List — The Most Detailed Free LLM API Directory

Most "free LLM API" lists give you a name and a link. This one gives you everything you need to decide *before* you sign up — so you're not hunting across 12 different docs pages to compare rate limits, SDK support, and OpenAI compatibility:

| Column | What it means |
|---|---|
| **Free Models** | Models available on the permanent free tier |
| **Rate Limits** | RPM (requests/min) and RPD (requests/day) |
| **OpenAI Compat** | Can you use the OpenAI Python/JS SDK by just swapping `base_url`? |
| **SDKs** | Official client libraries available |
| **Speed Tier** | 🟢 Fast / 🟡 Medium / 🔴 Slow (see legend below) |

---

## Contents

- [Provider APIs](#provider-apis) — companies that train or fine-tune their own models
- [Inference Providers](#inference-providers) — third-party platforms hosting open-weight models
  - includes Groq, Cerebras, OpenRouter, GitHub Models, NVIDIA NIM, Hugging Face, Cloudflare, Kluster AI, LLM7.io, Pollinations AI
  - [Speed Tier Legend](#speed-tier-legend)
  - [Quick Comparison Table](#quick-comparison-table)
  - [Code Snippets](#code-snippets)
  - [Contributing](#contributing)

  ---

  ## Provider APIs — First-Party Free LLM APIs

  APIs run by the companies that train or fine-tune the models themselves. These are **official free AI APIs** directly from the model creators.

  ---

  ### [Google Gemini](https://aistudio.google.com/app/apikey) 🇺🇸

  > Google's flagship model family. The free tier via AI Studio is among the most generous of any first-party provider.

  | Detail | Info |
  |---|---|
  | **Free Models** | Gemini 2.5 Pro, Gemini 2.0 Flash, Gemini 1.5 Flash, Gemini 1.5 Flash-8B, Gemini 1.0 Pro |
  | **Rate Limits** | 15 RPM / 1,500 RPD (Flash) · 2 RPM / 50 RPD (2.5 Pro) |
  | **OpenAI Compat** | ✅ Yes — `https://generativelanguage.googleapis.com/v1beta/openai/` |
  | **SDKs** | Python (`google-generativeai`), JS/TS, REST, Go, Swift, Dart |
  | **Speed Tier** | 🟢 Fast (Flash) · 🟡 Medium (Pro) |

  > ⚠️ Free tier not available in the EU, UK, or Switzerland. [Check available regions →](https://ai.google.dev/gemini-api/docs/available-regions)

  ---

  ### [Mistral AI](https://console.mistral.ai/api-keys) 🇪🇺

  > European flagship. Apache 2.0 licensed models — free to use and self-host. One of the best free tiers for token volume.

  | Detail | Info |
  |---|---|
  | **Free Models** | Mistral Small 3.1, Mistral Large 3, Ministral 8B, Codestral Mamba, Mistral Embed |
  | **Rate Limits** | 1 req/sec · 1B tokens/month |
  | **OpenAI Compat** | ✅ Yes — `https://api.mistral.ai/v1` |
  | **SDKs** | Python (`mistralai`), JS/TS (`@mistralai/mistralai`), REST |
  | **Speed Tier** | 🟡 Medium |

  ---

  ### [Cohere](https://dashboard.cohere.com/api-keys) 🇺🇸

  > Specializes in enterprise NLP. Strong free tier for RAG and embedding use cases.

  | Detail | Info |
  |---|---|
  | **Free Models** | Command A, Command R+, Command R, Aya Expanse 32B, Aya Expanse 8B + 5 more |
  | **Rate Limits** | 20 RPM · 1,000 req/month |
  | **OpenAI Compat** | ⚠️ Partial — native SDK preferred (`cohere-python`) |
  | **SDKs** | Python (`cohere`), JS/TS (`cohere-ai`), Go, Java, REST |
  | **Speed Tier** | 🟡 Medium |

  ---

  ### [Zhipu AI](https://open.bigmodel.cn/usercenter/apikeys) 🇨🇳

  > Chinese AI lab. Flash models are genuinely free with no published cap — good for experimentation.

  | Detail | Info |
  |---|---|
  | **Free Models** | GLM-4.7-Flash, GLM-4.5-Flash, GLM-4.6V-Flash (vision) |
  | **Rate Limits** | Undocumented |
  | **OpenAI Compat** | ✅ Yes — `https://open.bigmodel.cn/api/paas/v4/` |
  | **SDKs** | Python (`zhipuai`), REST |
  | **Speed Tier** | 🟡 Medium |

  ---

  ## Inference Providers — Free Third-Party LLM Hosting

  Third-party platforms hosting open-weight models from various sources (Meta, Mistral, DeepSeek, etc.). These are **free AI inference APIs** — no need to self-host.

  ---

  ### [Groq](https://console.groq.com/keys) 🇺🇸

  > Fastest free inference available. Runs on custom LPU (Language Processing Unit) hardware. Drop-in OpenAI replacement.

  | Detail | Info |
  |---|---|
  | **Free Models** | Llama 3.3 70B, Llama 4 Scout, Llama 4 Maverick, Gemma 2 9B, Kimi K2, Qwen QwQ 32B + 17 more |
  | **Rate Limits** | 30 RPM · 14,400 RPD · 6,000 TPM (varies by model) |
  | **OpenAI Compat** | ✅ Yes — `https://api.groq.com/openai/v1` |
  | **SDKs** | Python (`groq`), JS/TS (`groq`), REST |
  | **Speed Tier** | 🟢 Fast — LPU hardware, consistently 300–500 tok/sec |

  ---

  ### [Cerebras](https://cloud.cerebras.ai/) 🇺🇸

  > Wafer-scale chip inference. Competing with Groq on raw speed, strong free tier.

  | Detail | Info |
  |---|---|
  | **Free Models** | Llama 3.3 70B, Qwen3 235B, Llama 4 Scout, GPT-OSS-120B + 3 more |
  | **Rate Limits** | 30 RPM · 60,000 TPM · 14,400 RPD |
  | **OpenAI Compat** | ✅ Yes — `https://api.cerebras.ai/v1` |
  | **SDKs** | Python (`cerebras-cloud-sdk`), REST |
  | **Speed Tier** | 🟢 Fast — wafer-scale chip, comparable to Groq |

  ---

  ### [OpenRouter](https://openrouter.ai/keys) 🇺🇸

  > One API key for 30+ free models across multiple providers. Great as a fallback layer or for model switching.

  | Detail | Info |
  |---|---|
  | **Free Models** | DeepSeek R1, Llama 3.3 70B, GPT-OSS-120B, Qwen3 Coder 480B + 27 more (models ending in `:free`) |
  | **Rate Limits** | 20 RPM · 200 RPD |
  | **OpenAI Compat** | ✅ Yes — `https://openrouter.ai/api/v1` |
  | **SDKs** | Python (via `openai`), JS/TS (via `openai`), REST |
  | **Speed Tier** | 🟡 Medium — routes to various backends, latency varies |

  ---

  ### [GitHub Models](https://github.com/marketplace/models) 🇺🇸

  > Free inference via GitHub account. Good access to frontier models like GPT-4o alongside open-weight models.

  | Detail | Info |
  |---|---|
  | **Free Models** | GPT-4o, Llama 3.3 70B, DeepSeek-R1, Phi-4, Mistral Large + more |
  | **Rate Limits** | 10–15 RPM · 50–150 RPD (varies by model tier) |
  | **OpenAI Compat** | ✅ Yes — `https://models.inference.ai.azure.com` |
  | **SDKs** | Python (`azure-ai-inference` or `openai`), JS/TS, REST |
  | **Speed Tier** | 🟡 Medium |

  ---

  ### [NVIDIA NIM](https://build.nvidia.com/explore/discover) 🇺🇸

  > NVIDIA's hosted inference. Access to large parameter models including Qwen3 235B on GPU clusters.

  | Detail | Info |
  |---|---|
  | **Free Models** | Llama 3.3 70B, Mistral Large, Qwen3 235B, DeepSeek-R1 + more |
  | **Rate Limits** | 40 RPM (credit-based, replenishes) |
  | **OpenAI Compat** | ✅ Yes — `https://integrate.api.nvidia.com/v1` |
  | **SDKs** | Python (via `openai`), REST |
  | **Speed Tier** | 🟡 Medium |

  ---

  ### [Hugging Face Serverless](https://huggingface.co/settings/tokens) 🇺🇸

  > $0.10/month in free credits, auto-replenished. Access to thousands of community and flagship models. Limited to models under 10GB unless featured.

  | Detail | Info |
  |---|---|
  | **Free Models** | Llama 3.3 70B, Qwen2.5 72B, Mistral 7B, Zephyr, Phi + many more |
  | **Rate Limits** | $0.10 free credits/month (auto-refresh) |
  | **OpenAI Compat** | ✅ Yes — `https://api-inference.huggingface.co/v1` |
  | **SDKs** | Python (`huggingface_hub`, `openai`), JS/TS, REST |
  | **Speed Tier** | 🔴 Slow — shared queues, cold starts common |

  ---

  ### [Cloudflare Workers AI](https://dash.cloudflare.com/profile/api-tokens) 🇺🇸

  > Edge inference baked into Cloudflare Workers. Globally low-latency via the Cloudflare network. 10K "neurons"/day free.

  | Detail | Info |
  |---|---|
  | **Free Models** | Llama 3.3 70B, Qwen QwQ 32B, Phi-2, Gemma 7B + 47 more |
  | **Rate Limits** | 10,000 neurons/day (1 neuron ≈ 1 output token) |
  | **OpenAI Compat** | ⚠️ Partial — own REST API format, not drop-in |
  | **SDKs** | JS/TS (Workers SDK), Python (via REST), REST |
  | **Speed Tier** | 🟡 Medium — edge inference, latency varies by region |

  ---

  ### [Kluster AI](https://platform.kluster.ai/apikeys) 🇺🇸

  > Newer inference provider with access to flagship open-weight models. Rate limits not publicly documented.

  | Detail | Info |
  |---|---|
  | **Free Models** | DeepSeek-R1, Llama 4 Maverick, Qwen3-235B + 2 more |
  | **Rate Limits** | Undocumented |
  | **OpenAI Compat** | ✅ Yes |
  | **SDKs** | Python (via `openai`), REST |
  | **Speed Tier** | 🟡 Medium |

  ---

  ### [LLM7.io](https://token.llm7.io) 🇬🇧

  > UK-based inference provider. Token-based rate limiting — free token increases RPM from 15 to 30.

  | Detail | Info |
  |---|---|
  | **Free Models** | DeepSeek R1, Gemini Flash-Lite, Qwen2.5 Coder + 27 more |
  | **Rate Limits** | 15 RPM (30 RPM with free token) |
  | **OpenAI Compat** | ✅ Yes |
  | **SDKs** | Python (via `openai`), REST |
  | **Speed Tier** | 🟡 Medium |

  ---

  ### [Pollinations AI](https://enter.pollinations.ai) 🇩🇪

  > Berlin-based open-source platform. Unique in covering **text, image, video, and audio** generation all under one free API. No sign-up required for basic use — just hit the endpoint. API key unlocks higher limits and model access.

  | Detail | Info |
  |---|---|
  | **Free Models** | openai, openai-large, openai-reasoning, gemini, gemini-large, mistral, llama (text) · flux, gpt-image, seedream, kontext (image) · wan-fast (video) · tts-1, 30+ ElevenLabs voices (audio) |
  | **Rate Limits** | Per-IP, resets hourly. Undocumented exact cap — authenticated requests get priority limits |
  | **OpenAI Compat** | ✅ Yes — `https://gen.pollinations.ai/v1` (text & audio endpoints) |
  | **SDKs** | Python (via `openai`), JS/TS (via `openai`), REST, MCP server |
  | **Speed Tier** | 🟡 Medium |

  > 💡 **Standout feature:** The only free API on this list with image, video, and audio generation alongside text — all from one key. Also has an [MCP server](https://github.com/pollinations/pollinations) for use directly inside Claude and other AI assistants.

  ---

  ## Speed Tier Legend

  | Tier | Typical Output Speed | Hardware |
  |---|---|---|
  | 🟢 **Fast** | 300–600 tok/sec | Custom silicon (LPU/Wafer-scale) |
  | 🟡 **Medium** | 50–150 tok/sec | Standard cloud GPUs (A100/H100) |
  | 🔴 **Slow** | < 50 tok/sec or variable | Shared queues, CPU offload, cold starts |

  > Speed tiers are approximate. Real-world performance varies based on model size, prompt length, and time of day.

  ---

  ## Quick Comparison — Free LLM APIs at a Glance

  All 12 **free LLM API providers** side by side. Sorted by category (provider-first, then inference). Use this to pick the right free AI API for your use case before diving into the full entry above.

  | Provider | Best Free Model | RPM | RPD | OpenAI Compat | Speed |
  |---|---|---|---|---|---|
  | Google Gemini | Gemini 2.5 Pro | 2–15 | 50–1,500 | ✅ | 🟢🟡 |
  | Mistral AI | Mistral Large 3 | 60 | Unlimited* | ✅ | 🟡 |
  | Cohere | Command A | 20 | ~33/day | ⚠️ | 🟡 |
  | Zhipu AI | GLM-4.7-Flash | — | — | ✅ | 🟡 |
  | Groq | Llama 3.3 70B | 30 | 14,400 | ✅ | 🟢 |
  | Cerebras | Qwen3 235B | 30 | 14,400 | ✅ | 🟢 |
  | OpenRouter | Qwen3 Coder 480B | 20 | 200 | ✅ | 🟡 |
  | GitHub Models | GPT-4o | 10–15 | 50–150 | ✅ | 🟡 |
  | NVIDIA NIM | Qwen3 235B | 40 | — | ✅ | 🟡 |
  | Hugging Face | Llama 3.3 70B | — | credit-based | ✅ | 🔴 |
  | Cloudflare Workers AI | Llama 3.3 70B | — | 10K neurons | ⚠️ | 🟡 |
  | Pollinations AI | openai-large + image/video/audio | — | hourly reset | ✅ | 🟡 |

  > \* Mistral free tier is token-volume capped (1B tokens/month), not RPD capped.

  ---

  ## Code Snippets — How to Use Free LLM APIs with the OpenAI SDK

  All **OpenAI-compatible free LLM APIs** work with the same pattern. Just swap `base_url` and `api_key` — no new SDK to learn:

  ```python
  from openai import OpenAI

  # Swap these two lines to switch provider
  BASE_URL = "https://api.groq.com/openai/v1"   # Groq
  API_KEY  = "your-groq-key"

  client = OpenAI(api_key=API_KEY, base_url=BASE_URL)

  response = client.chat.completions.create(
      model="llama-3.3-70b-versatile",           # change model per provider
          messages=[{"role": "user", "content": "Hello!"}],
          )

          print(response.choices[0].message.content)
          ```

          **Provider base URLs:**

          ```python
          PROVIDERS = {
              "groq":       ("https://api.groq.com/openai/v1",                    "llama-3.3-70b-versatile"),
                  "cerebras":   ("https://api.cerebras.ai/v1",                        "llama-3.3-70b"),
                      "openrouter": ("https://openrouter.ai/api/v1",                      "meta-llama/llama-3.3-70b-instruct:free"),
                          "mistral":    ("https://api.mistral.ai/v1",                         "mistral-small-latest"),
                              "gemini":     ("https://generativelanguage.googleapis.com/v1beta/openai/", "gemini-2.0-flash"),
                                  "github":     ("https://models.inference.ai.azure.com",             "gpt-4o"),
                                      "nvidia":     ("https://integrate.api.nvidia.com/v1",               "meta/llama-3.3-70b-instruct"),
                                          "huggingface":("https://api-inference.huggingface.co/v1",           "meta-llama/Llama-3.3-70B-Instruct"),
                                              "zhipu":      ("https://open.bigmodel.cn/api/paas/v4/",             "glm-4-flash"),
                                                  "pollinations":("https://gen.pollinations.ai/v1",                   "openai-large"),  # no key needed for basic use
                                                  }
                                                  ```

                                                  ---

                                                  ## Notes & Definitions

                                                  - **RPM** = requests per minute · **RPD** = requests per day · **TPM** = tokens per minute
                                                  - "Limits undocumented" means the provider does not publicly publish rate limits — expect throttling.
                                                  - All providers marked ✅ OpenAI Compat work with the `openai` Python/JS SDK by changing `base_url`.
                                                  - Providers marked ⚠️ Partial have their own SDK or require minor request format changes.
                                                  - **Trial credits and time-limited promos are excluded** — only permanent free tiers are listed.
                                                  - Entries verified as of **March 2026**. Rate limits change frequently — always check provider docs.

                                                  ---

                                                  ## Related Resources

                                                  Looking for something specific? These searches might help:

                                                  - **Free OpenAI-compatible APIs** → filter the table above by ✅ OpenAI Compat
                                                  - **Fastest free LLM API** → see [Groq](#groq-) and [Cerebras](#cerebras-)
                                                  - **Free API with no sign-up** → see [Pollinations AI](#pollinations-ai-)
                                                  - **Free LLM API for images** → see [Pollinations AI](#pollinations-ai-)
                                                  - **Free LLM API for Europe** → see [Mistral AI](#mistral-ai-) (EU-based, no region block)
                                                  - **Free Llama API** → Groq, Cerebras, OpenRouter, GitHub Models all offer free Llama 3.3 70B
                                                  - **Free DeepSeek API** → OpenRouter, Kluster AI, LLM7.io, GitHub Models

                                                  ---

                                                  ## Contributing to awesome-free-llm-apis

                                                  See [contributing.md](contributing.md) for the full guide. The short version:

                                                  1. Fork this repo
                                                  2. Add your entry following the existing format (table + all fields)
                                                  3. Include a link to the provider's official rate limit documentation
                                                  4. Open a pull request — add the current month/year you verified it

                                                  **Rules:** No trial credits. No invite-only access. No entries missing rate limits without noting "undocumented". One entry per provider.

                                                  ---

                                                  ## License

                                                  [CC0 1.0](license) — public domain. Use freely, no attribution required.
