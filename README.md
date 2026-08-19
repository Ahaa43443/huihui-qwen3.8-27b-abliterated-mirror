# Huihui-Qwen3.8-27B-abliterated — personal mirror manifest

> **Unofficial mirror/manifest.** This repository is not owned by `huihui-ai` and does not contain the model weights in GitHub.

## Model name

`huihui-ai/Huihui-Qwen3.8-27B-abliterated`

- Original model page: https://huggingface.co/huihui-ai/Huihui-Qwen3.8-27B-abliterated
- Base model: `Qwen/Qwen3.8-27B`
- Format on Hugging Face: BF16 SafeTensors
- Repository size on Hugging Face: approximately 55.6 GB
- License shown on the original model card: Apache-2.0
- Tags: abliterated, uncensored, huihui, qwen3

## Author's description

The author describes this model as an uncensored version of `Qwen/Qwen3.8-27B` created with abliteration. The model card says that this is a crude proof-of-concept implementation for reducing refusals from an LLM without using TransformerLens.

The model card also notes that the first 15 layers were retained without ablation, while MTP and the visual component were not modified.

### Usage and safety notes from the original model card

The author warns that the model's safety filtering has been significantly reduced and that it may produce sensitive, controversial, or inappropriate outputs. The model is recommended for research, testing, or controlled environments rather than direct public-facing production use. Users are responsible for legal, ethical, and safety review of outputs. The author states that the model has no default safety guarantees.

## ZincDrive mirror files

The current storage workaround uses the `.bin` extension because ZincDrive's `.safetensors` confirmation path returned an internal database error. The file bytes remain the original SafeTensors bytes; the extension was changed only for storage. After downloading, rename each file back to `.safetensors` before loading the model.

| Original model file | Current ZincDrive file | Download |
|---|---|---|
| `model-00001-of-00018.safetensors` | `model-00001-of-00018.bin` | https://zdrive.to/9AqGQV4JmMn6 |
| `model-00002-of-00018.safetensors` | `model-00002-of-00018.bin` | https://zdrive.to/qLQ36DK7G19j |

More shards and tokenizer/configuration files will be added as they are uploaded.

## Restoring the original filename

After downloading a shard:

```bash
mv model-00001-of-00018.bin model-00001-of-00018.safetensors
mv model-00002-of-00018.bin model-00002-of-00018.safetensors
```

All 18 weight shards and the original configuration/tokenizer files are required for a complete model. The two files listed above are not sufficient to run the model by themselves.

## Why the weights are not stored on GitHub

GitHub is being used here for documentation and a download manifest only. GitHub has strict per-file and repository limits, so a 55+ GB model should not be committed to a normal Git repository. The original files remain attributed to the upstream Hugging Face author and repository.
