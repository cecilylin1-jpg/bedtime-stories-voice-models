# Bedtime Stories — local voice models

Public model distribution proposal for the Android app「睡前故事：AI聲音克隆 爸爸媽媽說故事」 / Bedtime Stories: Voice Clone. No app source, user data or voice recordings belong in this repository or its release assets.

## Origins and licenses

- OpenVoice V2: https://github.com/myshell-ai/OpenVoice ; official MIT weights https://huggingface.co/myshell-ai/OpenVoiceV2 . OpenVoice upstream source commit74a1d147b17a8c3092dd5430504bd83ef6c7eb23. Full original MIT copyright/license: LICENSE-OpenVoice-MIT.txt.
- MeloTTS: https://github.com/myshell-ai/MeloTTS ; MIT weights https://huggingface.co/myshell-ai/MeloTTS-Chinese and https://huggingface.co/myshell-ai/MeloTTS-English . Official sherpa exports: https://github.com/k2-fsa/sherpa-onnx/blob/master/scripts/melo-tts/README.md . Original MIT copyright/license: LICENSE-MeloTTS-MIT.txt. All notices also remain inside the model pack.

## Compact v2 pack

199,105,645bytes split into24parts (8MiB except last). Download ALL files listed in compact-manifest.json, concatenate in numeric order, and verify every SHA256. The app pins its own manifest; a downloaded manifest cannot replace trusted hashes. Reversible16-bit-byte-shuffle transport is undone before decoded model SHA verification. Installed251,154,660bytes;14-bit zh/converter and15-bit English weights stored in INT16, FP32 arithmetic, original FP32 speaker extractor. Storage compression does not imply reduced RAM/compute or perceptual equality. Synthetic test full-pipeline SNR35.49dB zh/27.00dB en. Original FP32 fallback is larger and separately versioned.

Use only a consenting adult's own voice; never a child, celebrity or third party. No audio uploads are required for local inference. This is an experimental test model pack, not a production safety/quality certification.
