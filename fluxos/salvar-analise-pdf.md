# Fluxo "Salvar Analise em PDF"

Fluxo de trabalho do Copilot Studio (agent flow) usado como ferramenta pelos dois especialistas. Ele recebe a análise em HTML, converte em PDF e salva numa biblioteca do SharePoint.

```mermaid
flowchart LR
    A[Agente chama o fluxo] --> B[OneDrive: Criar arquivo .html]
    B --> C[OneDrive: Converter arquivo para PDF]
    C --> D[SharePoint: Criar arquivo .pdf]
    D --> E[Responder ao agente com o caminho]
```

## Gatilho: "Quando um agente chama o fluxo de trabalho"

| Entrada | Tipo | Descrição |
|---|---|---|
| `NomeArquivo` | Texto | Nome do arquivo sem extensão, ex.: `ANALISE_TECNICA_123456_2026-10-18` |
| `ConteudoHTML` | Texto | Análise completa em HTML (`<html>`, `<body>`, títulos e tabelas) |

## Ações

| # | Conector / ação | Parâmetros |
|---|---|---|
| 1 | OneDrive for Business – **Criar arquivo** | Pasta: `/` · Nome: `@{triggerOutputs()?['body/text']}.html` · Conteúdo: `ConteudoHTML` |
| 2 | OneDrive for Business – **Converter arquivo** | Arquivo: `Id` da ação 1 · Tipo de destino: `PDF` |
| 3 | SharePoint – **Criar arquivo** | Site: `<SEU_SITE>` · Pasta: `<SUA_BIBLIOTECA>/<SUA_PASTA>` · Nome: `@{triggerOutputs()?['body/text']}.pdf` · Conteúdo: `Conteúdo do arquivo` da ação 2 |
| 4 | **Responder ao agente** | Saída `CaminhoArquivo` (Texto) = `Path` da ação 3 |

## Observações

- A conversão usa o OneDrive porque o conector "Converter arquivo" só trabalha com arquivos do OneDrive.
- Melhoria opcional: incluir uma ação OneDrive **Excluir arquivo** depois da ação 3, para apagar o `.html` temporário.
- Os fluxos consomem créditos do Copilot Studio. Se o ambiente estiver sem créditos, o fluxo não executa.
