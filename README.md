# How to Save Millions by Self-Hosting LLMs

**Read the book online: <https://arafatkatze.github.io/inference-math/>** (PDF and ePub downloads are in the site's sidebar)

A [Quarto book](https://quarto.org/docs/books/) covering the math of LLM inference and the actual dollars: loading the model, serving it (prefill/decode/KV cache), batching, load testing, sizing the GPU fleet, the monthly bill, and working with inference providers.

The book renders to three formats from a single source:

- **HTML** — the website (published on GitHub Pages)
- **PDF** — the printable book
- **ePub** — the e-reader version

## Local development

Install [Quarto](https://quarto.org/docs/get-started/), then:

```bash
# live-reloading preview in the browser
quarto preview

# render all formats (HTML + PDF + ePub) into _book/
quarto render
```

PDF output additionally requires a LaTeX distribution and the DejaVu fonts:

```bash
quarto install tinytex
sudo apt-get install fonts-dejavu   # Linux; macOS ships DejaVu-compatible fonts
```

To render only one format: `quarto render --to html` (or `pdf`, `epub`).

## Publishing

The book is served at <https://arafatkatze.github.io/inference-math/>. Every push to `main` triggers `.github/workflows/publish.yml`, which renders the book (HTML + PDF + ePub) and deploys it to GitHub Pages. The workflow enables Pages automatically on its first run, so no repository settings are required.

If the first run ever fails on the "Enable and configure GitHub Pages" step, enable it manually once: **Settings → Pages → Source → GitHub Actions**.

## Structure

```
├── _quarto.yml                    # one config for all formats
├── index.qmd                      # preface
├── 01-architecture.qmd            # model architecture
├── 02-picking-the-gpu.qmd         # picking the GPU + node cost
├── 03-loading-the-model.qmd       # GPUs needed to load the model
├── 04-serving.qmd                 # prefill / decode / KV cache
├── 05-batching.qmd                # batching regions + load test math
├── 06-sizing-the-fleet.qmd        # sizing the GPU fleet
├── 07-the-bill.qmd                # the monthly bill
├── 08-load-testing.qmd            # how to actually run a load test
├── 09-working-with-providers.qmd  # working with inference providers
├── 10-closing.qmd                 # closing note + credits
├── references.qmd
└── images/
```
