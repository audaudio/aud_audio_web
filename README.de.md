# aud_audio_web

[English](README.md) | Deutsch

Web-Build der Audanika Audio Engine: Emscripten-Toolchain,
AudioWorklet-Host, Wasm-Worker-Steuerlaufzeit.

Teil der Audanika Audio Engine; geplant in
[aud_audio_pm](https://github.com/audaudio/aud_audio_pm).

## Motivation

Die Engine hat eine API auf nativen Plattformen und im Web (web-001).
Dieses Paket soll ihre Web-Seite werden: der Graph von `aud_audio_graph`,
mit Emscripten kompiliert, in einem AudioWorklet gerendert und aus einem
Wasm-Worker gesteuert, sodass die Dart-Seite kein `dart:ffi` braucht.
Heute ist es ein Stub, der nur den Versionen der Familie folgt; die
Web-Engine folgt mit Schritt S5.

## Installation

Das Paket ist nicht auf pub.dev veröffentlicht; es kommt als
Git-Abhängigkeit dazu:

```yaml
dependencies:
  aud_audio_web:
    git:
      url: git@github.com:audaudio/aud_audio_web.git
      tag_pattern: "{{version}}"
    version: ^0.0.10
```

## Verwendung

Die öffentliche API ist die Version des Pakets:

```dart
import 'package:aud_audio_web/aud_audio_web.dart';

void main() {
  print(audAudioWebVersion);
}
```

Es gibt aus:

```text
0.0.10
```

## Grenzen

- Noch keine Web-Engine: kein Emscripten-Build, kein AudioWorklet-Host,
  keine Wasm-Worker-Laufzeit; das Paket exportiert nur seine Version

## Dokumentation

- Die Guides in [doc/guides](doc/guides) und die Blogbeiträge in
  [doc/de/blog](doc/de/blog)
- Die Änderungen je Version in [CHANGELOG.md](CHANGELOG.md)

## Status

Vor 1.0 - die API kann sich zwischen Minor-Versionen ändern. Das Paket
ist ein Stub der Familie bis Schritt S5.

## Mitwirken

Tickets laufen über den `gg`-Workflow: siehe den
[Develop Guide](doc/guides/develop-guide.md) und den
[Review Guide](doc/guides/for-ai/ai-review-guide.md).

## Lizenz

MIT - siehe [LICENSE](LICENSE).
