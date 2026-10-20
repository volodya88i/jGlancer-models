# jGlancer models

Model files that the jGlancer app for Windows downloads when the user asks for them. They are not part of the app's
installer, and the app downloads nothing else.

## Stem splitting (release `models-1`)

| File | Stems | Size | SHA-256 |
|---|---|---|---|
| `htdemucs.onnx` | vocals, drums, bass, other | 90,555,550 bytes | `4782234fdd0ce38d94ae198746c680c898e1cb6c35d062c2042a3318871c113a` |
| `htdemucs_6s.onnx` | also guitar, piano | 59,959,882 bytes | `982cbe0b6a8e8715d2a142b9c5aae36d7d0c087b9c1382fab57d8e6d3aebfcd1` |
| `htdemucs-full.onnx` | vocals, drums, bass, other | 174,264,723 bytes | `6941830d664bbf4a8238dbe9dec242b8c2799ce651a7dfbe7997b1e36b70c56f` |
| `htdemucs_6s-full.onnx` | also guitar, piano | 114,560,305 bytes | `2f8d1e48cd6a4328f85f43afee3f73f53662450b3ecda0cb546e1508055d8a00` |

These are Demucs v4 (Hybrid Transformer) by Meta: `htdemucs` and `htdemucs_6s`. Only the network is exported to ONNX;
the STFT and iSTFT run in the app. In the compact files the weights are stored as float16, and the network computes in
float32; the "-full" files keep the original float32 weights. Both separate the same (the difference is 65–92 dB down).

Demucs is released under the MIT license by Meta Platforms, Inc. and affiliates: https://github.com/facebookresearch/demucs

```
MIT License

Copyright (c) Meta Platforms, Inc. and affiliates.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
