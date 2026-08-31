# MeanVC Android Assets

ONNX exports of [MeanVC](https://github.com/ASLP-lab/MeanVC) (Apache 2.0) for on-device Android voice conversion, plus a precomputed reference speaker embedding.

- ASR content encoder (`fastu2plusplus_state_*.onnx`): 3 fixed-shape chunked-streaming states
- DiT voice-conversion model (`dit_state_*.onnx`): 7 fixed-shape KV-cache states
- Vocos vocoder (`vocos.onnx`): fixed 173-frame input, complex-number-free ISTFT reimplementation
- `tsukuyomi_spk_emb.bin` / `tsukuyomi_prompt_mel.bin`: precomputed speaker embedding + prompt mel for the Tsukuyomi-chan reference voice (avoids needing the 1.3GB WavLM model on-device)

All numerically verified against the original PyTorch/TorchScript models.
