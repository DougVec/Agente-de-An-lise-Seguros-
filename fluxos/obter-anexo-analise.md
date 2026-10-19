# Fluxo "Obter Anexo para Analise"

Ferramenta dos **dois especialistas**. Recebe o `IdArquivo` enviado pelo orquestrador, busca o documento no SharePoint e o devolve como **arquivo** ao agente. Devolver como arquivo, e não como texto, evita que o modelo receba o PDF em base64, que ele não consegue ler.

```mermaid
flowchart LR
    A[Especialista chama o fluxo com o IdArquivo] --> B[SharePoint: Obter conteúdo de arquivo]
    B --> C[Responder ao agente com o arquivo]
```

## Gatilho: "Quando um agente chama o fluxo de trabalho"

| Entrada | Tipo | Descrição |
|---|---|---|
| `IdArquivo` | Texto | IdArquivo do documento no SharePoint, recebido do orquestrador |
| `NomeArquivo` | Texto | Nome do arquivo (ex.: `apolice.pdf`), recebido do orquestrador |

## Ações

| # | Conector / ação | Parâmetros |
|---|---|---|
| 1 | SharePoint – **Obter conteúdo de arquivo** | Site: `<SEU_SITE>` · Identificador de Arquivo: `IdArquivo` · Inferir tipo de conteúdo: `true` |
| 2 | **Responder ao agente** | Saída `Documento` (File) = `Conteúdo do Arquivo` da ação 1 |

## Observações

- Descrição da ferramenta nos especialistas: `Busca no SharePoint o documento enviado pelo orquestrador (IdArquivo) e o entrega como arquivo para leitura. Use uma vez para cada IdArquivo recebido, antes de iniciar a análise.`
- Ainda não validado em produção (ambiente sem créditos). Se o especialista não conseguir ler o arquivo retornado, a alternativa é extrair o texto do PDF no próprio fluxo (ação **Extrair**) e devolver como Texto.
