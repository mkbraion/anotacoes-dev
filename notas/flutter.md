# Flutter — anotações rápidas

## Widget com estado vs sem estado
- `StatelessWidget`: só desenha, não muda sozinho.
- `StatefulWidget`: guarda estado e redesenha com `setState(() { ... })`.

## Rodar e limpar
```bash
flutter run              # roda no device/emulador conectado
flutter clean            # limpa build quando dá erro estranho
flutter pub get          # baixa as dependências do pubspec.yaml
```

## Formatar dinheiro (pt-BR)
```dart
import 'package:intl/intl.dart';

final brl = NumberFormat.currency(locale: 'pt_BR', symbol: 'R\$');
brl.format(1234.5); // R$ 1.234,50
```
