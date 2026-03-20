# SEA-u-lator Synthetic Phishing Dataset

## Overview

This directory contains two synthetic dataset files released alongside SEA-u-lator:

- `phish_emails_cleaned.jsonl`
- `phish_wrong_feedback.jsonl`

They were created for phishing-awareness research, interface evaluation, education, and reproducibility of the SEA-u-lator artifact.

## Files

### `phish_emails_cleaned.jsonl`

JSONL records of synthetic phishing-training emails with these fields:

- `id`
- `subject`
- `from_name`
- `from_email`
- `body_html`
- `body_text`

### `phish_wrong_feedback.jsonl`

JSONL records mapping message ids to synthetic feedback text:

- `id`
- `ollama_feedback`

## How the dataset was produced

The data was generated offline using Ollama with `llama3.1:latest`, then programmatically filtered, validated, and cleaned before release.

The release is intentionally limited to synthetic text artifacts. The bundled dataset fallback is also less adaptive than SEA-u-lator's live Ollama mode, because it comes from a fixed pool rather than generation from the current inbox context.

## Intended use

This dataset is intended for:

- phishing-awareness training,
- human-subjects research,
- security and HCI experiments,
- teaching and demonstration,
- and reproducibility of the SEA-u-lator artifact.

## Out-of-scope use

This dataset is not released for:

- operational phishing campaigns,
- credential harvesting,
- deceptive messaging against real users,
- malware delivery,
- or other harmful deployment.

These statements describe intended and out-of-scope use, but they do not add legal restrictions beyond the dataset license.

## FAQ

### Is this dataset real or synthetic?

It is synthetic. The released files contain synthetic phishing-themed emails and synthetic feedback text, not harvested real-user mailboxes.

### Does it contain personal data, live phishing links, credentials, or malware?

No real personal mailbox content is intentionally included. The dataset is a synthetic research artifact and is not distributed with live credential-harvesting workflows, malware, or executable payloads.

### Can the authors control misuse of the dataset?

No. Once a dataset is publicly released, the authors cannot technically or practically control every downstream use.

### Are the authors aware of misuse risk?

Yes. The authors recognize that phishing-themed artifacts may be misused. The dataset is being released anyway because reproducibility, transparency, and independent evaluation are important research goals.

### What was done to reduce misuse potential?

The release is limited to synthetic training data and synthetic feedback text. It does not rely on real victim mailboxes, and the bundled fallback dataset is less adaptive than live local generation with Ollama.

### Does release imply endorsement of downstream use?

No. Publication of this dataset does not imply endorsement of downstream uses by the authors.

### Does this README legally prohibit harmful use?

No. The dataset is licensed under CC BY 4.0. This README documents intended use, risks, and limitations, but it does not add new downstream license restrictions.

### Is the dataset a warranty-backed security product?

No. The dataset is provided as-is for research and educational use.

## Limitations

- The data is synthetic and may include stylistic artifacts.
- Sender names and domains may be less realistic than live, context-aware generation.
- The fallback dataset is not representative of all phishing ecosystems.
- Static synthetic examples may be less convincing than local generation driven by visible inbox context.

## License

The dataset files in this directory are licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0).

See [`LICENSE-CC-BY-4.0.txt`](LICENSE-CC-BY-4.0.txt) or the official license page:

- [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
- [Legal code](https://creativecommons.org/licenses/by/4.0/legalcode)

## Model provenance

This dataset was generated using Ollama with `llama3.1:latest`. Users of this dataset are responsible for complying with any applicable upstream model or provider terms.
