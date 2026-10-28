# aud_audio_web

English | [Deutsch](README.de.md)

Web build of the Audanika Audio Engine: Emscripten toolchain, AudioWorklet
host, Wasm Worker control runtime.

Part of the Audanika Audio Engine; planned in
[aud_audio_pm](https://github.com/audaudio/aud_audio_pm).

## Motivation

The engine has one API on native platforms and the web (web-001). This
package is meant to become its web side: the graph of `aud_audio_graph`
compiled with Emscripten, rendered in an AudioWorklet and controlled from
a Wasm Worker, so that the Dart side needs no `dart:ffi`. Today it is a
stub that only follows the versions of the family; the web engine follows
with step S5.

## Installation

The package is not published to pub.dev; add it as a git dependency:

```yaml
dependencies:
  aud_audio_web:
    git:
      url: git@github.com:audaudio/aud_audio_web.git
      tag_pattern: "{{version}}"
    version: ^0.0.10
```

## Usage

The public API is the version of the package:

```dart
import 'package:aud_audio_web/aud_audio_web.dart';

void main() {
  print(audAudioWebVersion);
}
```

It prints:

```text
0.0.10
```

## Limitations

- No web engine yet: no Emscripten build, no AudioWorklet host, no Wasm
  Worker runtime; the package exports its version only

## Documentation

- The guides in [doc/guides](doc/guides) and the blog posts in
  [doc/blog](doc/blog)
- The changes per version in [CHANGELOG.md](CHANGELOG.md)

## Status

Before 1.0 - the API may change between minor versions. The package is a
stub of the family until step S5.

## Contributing

Tickets run through the `gg` workflow: see the
[Develop Guide](doc/guides/develop-guide.md) and the
[Review Guide](doc/guides/for-ai/ai-review-guide.md).

## License

MIT - see [LICENSE](LICENSE).
