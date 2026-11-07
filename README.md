# imalc model files

Ahead-of-time compiled model files for the [imalc](https://github.com/bitmvk/imalc) on-device photo-classification benchmark. The app downloads them from this repository's releases.

All files are derivatives of [LiquidAI/d1-2B](https://huggingface.co/LiquidAI/d1-2B), made via [litert-community/d1-2B-LiteRT](https://huggingface.co/litert-community/d1-2B-LiteRT) and the conversions described in the app repository. They are licensed under the LFM Open License v1.0 (see `LICENSE` and `NOTICE`) and are not official Liquid AI releases.

| Files | Runtime | Hardware |
|---|---|---|
| `d1-2b_decide_L{192,256}_a16w8.pte` | ExecuTorch, MediaTek Neuron backend | MediaTek Dimensity 9400 (MT6991) NPU |
| `d1-2b_decide_L{192,256}_8da4w.pte`, `d1-2b_tower_G{16,24}x*_fp32.pte` and their `.json` files | ExecuTorch XNNPACK | CPU |
| `*_MediaTek_MT6991_apply_plugin.tflite` | LiteRT, MediaTek dispatch | MT6991 NPU |
| `d1-2b_tower_G16x16_fp16fc.tflite` | LiteRT GPU | GPU |

The NPU files are compiled only for MT6991.
