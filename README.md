# YVYRA – Core Oto Utilities

Biblioteca leve para manipulação de arquivos `oto.ini` usados em engines de síntese vocal como **UTAU** e **OpenUtau**. Projetada para automação, integração e ferramentas de edição eficientes.

## Funcionalidades

- Leitura e escrita de arquivos `oto.ini` com suporte a múltiplos encodings
- Representação estruturada de entradas de voicebank (`OtoEntry`)
- Operações seguras e serializáveis para edição em lote
- Totalmente independente; ou seja: sem dependências externas

## Arquivos principais

- `oto_entry.py` – Define a classe `OtoEntry` (representação de uma linha do oto.ini)
- `oto_file.py`   – Lida com carregamento, parsing e salvamento de arquivos oto completos
- `__init__.py`   – Expõe a interface pública do módulo

## Uso básico

```python
from yvyra import OtoFile

oto = OtoFile.load("caminho/oto.ini")
for entry in oto.entries:
    print(entry.alias, entry.filename)
oto.save("output.ini")
