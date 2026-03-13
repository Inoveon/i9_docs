---
name: preview
description: Abre um arquivo HTML no navegador padrão para visualização. Use quando o usuário quiser visualizar, abrir ou fazer preview de um arquivo .html. Exemplos: "abre no navegador", "preview do HTML", "abrir o arquivo", "/preview".
---

Abra o arquivo HTML indicado no navegador padrão.

## Regras

1. Se um caminho foi passado como argumento, use-o diretamente.
2. Se não foi passado argumento, verifique se há um arquivo HTML aberto no IDE (disponível no contexto como `ide_opened_file`). Use esse caminho.
3. Se nenhum arquivo for identificado, liste os arquivos `.html` do projeto e use `AskUserQuestion` para o usuário escolher.
4. Use `open "{caminho_absoluto}"` para abrir no macOS.
5. Confirme ao usuário qual arquivo foi aberto.

## Exemplo de uso

```
/preview
/preview presentations/internal/diagnostico-organizacional-2026.html
```
