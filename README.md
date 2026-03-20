# SEA-u-lator

SEA-u-lator is a privacy-preserving social engineering attack simulator for Gmail. It injects synthetic phishing emails into a Gmail inbox for research, education, and phishing-awareness training.

## What is released

- `dist.zip`: the Chrome extension release artifact.
- `datasets/phish_emails_cleaned.jsonl`: synthetic phishing-training emails.
- `datasets/phish_wrong_feedback.jsonl`: synthetic feedback messages used after incorrect user responses.

## Requirements

- Google Chrome
- Gmail
- Ollama is recommended, not required

## Ollama vs dataset fallback

SEA-u-lator works in two modes:

- Recommended: local generation with Ollama for the most context-aware and convincing phishing simulations.
- Fallback: a bundled synthetic dataset that works without Ollama. This mode is lighter and typically less adaptive, so it may be less convincing than live local generation.

## Installation

1. Download `dist.zip` from the latest release.
2. Unzip it somewhere convenient.
3. Open `chrome://extensions/` in Chrome.
4. Enable Developer mode.
5. Click `Load unpacked`.
6. Select the unzipped `dist` folder.

## Datasets

The release includes two synthetic dataset files in [`datasets/`](datasets/):

- [`phish_emails_cleaned.jsonl`](datasets/phish_emails_cleaned.jsonl)
- [`phish_wrong_feedback.jsonl`](datasets/phish_wrong_feedback.jsonl)

The dataset is documented separately in [`datasets/README.md`](datasets/README.md).

## Licensing

- Software in this repository: GPL-3.0. See [`LICENSE`](LICENSE).
- Dataset files in [`datasets/`](datasets/): CC BY 4.0. See [`datasets/LICENSE-CC-BY-4.0.txt`](datasets/LICENSE-CC-BY-4.0.txt).

## Dataset risk FAQ

### Can the authors control misuse of the dataset?

No. Once the dataset is public, the authors cannot technically or practically control every downstream use.

### Are the authors aware of misuse risk?

Yes. The release is intentional and reflects a tradeoff between misuse risk and the research goals of transparency, reproducibility, and independent evaluation.

### Why release the dataset anyway?

Because SEA-u-lator includes a bundled fallback mode, and sharing the dataset improves reproducibility and makes the artifact easier to inspect, evaluate, and reuse in research settings.

### What reduces the misuse potential?

The released dataset is synthetic and fixed. It does not expose real participant inboxes, and it is less adaptive than SEA-u-lator's local Ollama mode.

### Where is the full dataset documentation?

See [`datasets/README.md`](datasets/README.md) for intended use, out-of-scope use, limitations, license scope, and provenance.

## Model provenance

The synthetic dataset was generated offline with Ollama using `llama3.1:latest`, then programmatically filtered, validated, and cleaned. Users are responsible for complying with any applicable upstream model or provider terms.
