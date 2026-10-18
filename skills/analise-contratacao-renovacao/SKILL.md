---
name: analise-contratacao-renovacao
description: Análises do processo de contratação e renovação de seguros (edital x proposta, comparativo de seguradoras, proposta V1 x V2, proposta final x certificado x pedido de emissão, apólice x proposta x pedido de emissão, pedido de emissão x boletos). Use quando o usuário escolher "Análise de Processo de Contratação e Renovação".
---

# ANÁLISE DE PROCESSO DE CONTRATAÇÃO E RENOVAÇÃO

## 1. MENU DA ETAPA
Ao ser acionada, se o usuário ainda não indicou a etapa, pergunte exatamente:

"Qual análise do processo de Contratação e Renovação você deseja fazer?
1. Edital x Proposta
2. Edital x Propostas de várias seguradoras (comparativo A, B, C...)
3. Proposta V1 x Proposta V2
4. Proposta final x Certificado x Pedido de emissão
5. Apólice x Proposta x Pedido de emissão
6. Pedido de emissão x Boletos de pagamento"

Após a escolha, informe quais documentos anexar (conforme a etapa) e aguarde.

## 2. REGRAS GERAIS (valem para todas as etapas)
1. Não inventar informações. Use exclusivamente os documentos enviados.
2. Não preencher lacunas com padrões de mercado, conhecimento geral ou suposições.
3. Dado não localizado: registre exatamente NÃO IDENTIFICADO.
4. Divergência entre documentos: não escolha um dado como correto; apresente os dois valores e classifique.
5. Classifique cada item com: ✅ CONFORME | ❌ NÃO CONFORME | ⚠️ NÃO FOI POSSÍVEL VALIDAR.
6. Identifique cada documento pelo conteúdo, não pelo nome do arquivo.
7. Documento referenciado e não fornecido: registre DOCUMENTO REFERENCIADO NÃO FORNECIDO: [identificação].
8. Valores em reais no padrão brasileiro (R$ 1.234.567,89); percentuais com duas casas decimais; datas DD/MM/AAAA.
9. Cálculos somente com todas as variáveis identificadas.
10. Não exibir trechos literais, páginas, seções de "Evidências", "Raciocínio" ou "Cadeia de pensamento", salvo pedido expresso.
11. Se faltar documento obrigatório da etapa, ou se algum arquivo estiver ilegível: não execute a análise; responda somente qual documento falta ou não pôde ser lido e encerre. Não apresente análise parcial.
12. Observações enviadas pelo usuário são contexto, não substituem o conteúdo dos documentos.

## MÉTODO DE LEITURA (precisão em documentos extensos e economia)
1. Peça todos os documentos necessários em uma única mensagem e execute a análise completa em uma única resposta. Não peça confirmações intermediárias, não resuma os documentos antes de analisar e não repita a análise em mensagens seguintes.
2. Leia cada documento inteiro, incluindo quadros de dados, condições particulares/especiais, anexos, cláusulas de cobertura, exclusões e franquias. Em documentos longos, localize primeiro essas seções e extraia os dados delas.
3. Extraia antes de comparar: preencha primeiro as tabelas de extração e só depois faça as comparações e cálculos com os valores extraídos.
4. Campos críticos (CNPJs, números de apólice/contrato, datas, valores, percentuais, limites e franquias) devem ser conferidos duas vezes no documento antes de serem registrados. Copie números exatamente como aparecem; nunca arredonde, complete ou reconstrua dígitos.
5. Se o mesmo campo aparecer com valores diferentes no mesmo documento, registre a divergência; não escolha um.
6. Se uma informação não estiver no texto lido, registre NÃO IDENTIFICADO. Nunca use a base de conhecimento, a norma SUSEP ou conhecimento geral para preencher dados do caso; esses materiais servem só para conceitos e terminologia.
7. Seja objetivo: sem introduções, sem explicações fora do formato obrigatório.

## 3. CAMPOS PADRÃO DE COMPARAÇÃO
Use, conforme aplicável a cada etapa:
Seguradora (nome e CNPJ); Tomador (nome e CNPJ); Segurado (nome e CNPJ); Ramo/Modalidade; Objeto do seguro; Número do edital/processo; Número da proposta e versão; Número do certificado; Número da apólice/endosso; Início e fim de vigência; Importância Segurada / LMG por cobertura; Coberturas básicas e adicionais com limites; Franquias/POS; Exclusões relevantes; Prêmio líquido; IOF; Prêmio total; Forma de pagamento; Número e valor das parcelas; Datas de vencimento; Corretora e comissão (quando constar); Cláusulas particulares/especiais; Condições de habilitação exigidas (quando constar).

## 4. ETAPAS

### Etapa 1 — Edital x Proposta
Documentos obrigatórios: EDITAL (ou termo de referência) e PROPOSTA da seguradora.
Verifique, item a item, se a proposta atende a cada exigência do edital: partes, objeto, vigência, coberturas exigidas, limites/IS mínimos, franquias máximas, exclusões vedadas, condições de pagamento, prazos e documentação exigida.
Saída:
1. PARECER (✅ ATENDE AO EDITAL | ⚠️ ATENDE PARCIALMENTE | ❌ NÃO ATENDE | ⚠️ ANÁLISE INCONCLUSIVA)
2. AJUSTES NECESSÁRIOS (Item; Exigência do edital; O que consta na proposta; Correção necessária; Responsável: seguradora/corretora)
3. TABELA DE CONFORMIDADE (Exigência | Edital | Proposta | Status)
4. EXTRAÇÃO DO EDITAL
5. EXTRAÇÃO DA PROPOSTA

### Etapa 2 — Edital x Propostas de várias seguradoras
Documentos obrigatórios: EDITAL e no mínimo DUAS propostas de seguradoras diferentes.
Para cada proposta, aplique a verificação da Etapa 1. Depois compare as propostas entre si.
Critério de recomendação (nesta ordem): (1) propostas que atendem integralmente ao edital; (2) entre elas, menor prêmio total; (3) em empate, maiores limites/menores franquias e melhores condições de pagamento. Proposta que não atende ao edital não pode ser recomendada como melhor; se nenhuma atender, informe isso.
Saída:
1. RECOMENDAÇÃO (seguradora indicada e motivo objetivo, baseado somente nos documentos)
2. RANKING (Posição | Seguradora | Atende ao edital? | Prêmio total | Principais pendências)
3. QUADRO COMPARATIVO (Exigência | Edital | Seguradora A | Seguradora B | Seguradora C ...), com status por célula
4. AJUSTES NECESSÁRIOS POR SEGURADORA
5. EXTRAÇÃO DO EDITAL
6. EXTRAÇÃO DE CADA PROPOSTA

### Etapa 3 — Proposta V1 x Proposta V2
Documentos obrigatórios: duas versões de proposta da mesma seguradora (anterior e nova). Identifique qual é a mais recente pela data/número de versão do documento; se não for possível, pergunte ao usuário.
Liste TODAS as alterações entre as versões, campo a campo, inclusive cláusulas incluídas ou removidas.
Saída:
1. RESUMO DAS ALTERAÇÕES (quantidade de campos alterados e impacto: favorável, desfavorável ou neutro ao segurado, quando objetivamente aferível; caso contrário "NÃO AVALIADO")
2. TABELA DE ALTERAÇÕES (Campo | V1 | V2 | Variação | Impacto)
3. CAMPOS SEM ALTERAÇÃO (lista)
4. PONTOS DE ATENÇÃO (alterações que conflitem com o edital, se o edital for anexado)

### Etapa 4 — Proposta final x Certificado x Pedido de emissão
Documentos obrigatórios: PROPOSTA FINAL, CERTIFICADO e PEDIDO DE EMISSÃO.
Todos os campos padrão presentes nos três documentos devem estar idênticos. Qualquer diferença é ❌ NÃO CONFORME.
Saída:
1. PARECER (✅ EM LINHA | ❌ DIVERGENTE | ⚠️ ANÁLISE INCONCLUSIVA)
2. AJUSTES NECESSÁRIOS (Campo; Proposta; Certificado; Pedido de emissão; Documento a corrigir)
3. TABELA DE CONFERÊNCIA (Campo | Proposta final | Certificado | Pedido de emissão | Status)

### Etapa 5 — Apólice x Proposta x Pedido de emissão
Documentos obrigatórios: APÓLICE (ou endosso), PROPOSTA e PEDIDO DE EMISSÃO.
A apólice deve refletir exatamente a proposta aceita e o pedido de emissão. Qualquer diferença é ❌ NÃO CONFORME. Verifique também numeração (apólice vinculada à proposta correta) e se constam todas as cláusulas particulares da proposta.
Saída:
1. PARECER (✅ EM LINHA | ❌ DIVERGENTE | ⚠️ ANÁLISE INCONCLUSIVA)
2. AJUSTES NECESSÁRIOS (Campo; Apólice; Proposta; Pedido de emissão; Documento a corrigir)
3. TABELA DE CONFERÊNCIA (Campo | Apólice | Proposta | Pedido de emissão | Status)

### Etapa 6 — Pedido de emissão x Boletos
Documentos obrigatórios: PEDIDO DE EMISSÃO e o(s) BOLETO(S) de pagamento.
Verifique: beneficiário do boleto (seguradora) x seguradora do pedido; pagador x tomador/segurado; número de parcelas; valor de cada parcela; soma das parcelas = prêmio total do pedido; datas de vencimento x condição de pagamento; número da apólice/proposta referenciado no boleto.
Calcule: Soma dos boletos e Diferença = Soma dos boletos − Prêmio total do pedido.
Saída:
1. PARECER (✅ EM LINHA | ❌ DIVERGENTE | ⚠️ ANÁLISE INCONCLUSIVA)
2. AJUSTES NECESSÁRIOS
3. TABELA DE PARCELAS (Parcela | Vencimento no pedido | Vencimento no boleto | Valor no pedido | Valor no boleto | Status)
4. TOTALIZAÇÃO (Prêmio total do pedido | Soma dos boletos | Diferença | Status)
Nunca informe linha digitável ou código de barras completos na resposta.

## 5. TÍTULO DA RESPOSTA
Use: ANÁLISE DE CONTRATAÇÃO E RENOVAÇÃO - ETAPA [n]: [nome da etapa]

## 6. CONTROLE FINAL DE QUALIDADE
Antes de responder, confirme internamente: documentos obrigatórios da etapa lidos; todos os campos preenchidos ou NÃO IDENTIFICADO; nenhum cálculo com dado não identificado; parecer coerente com as divergências; todos os ajustes listados; nenhuma informação inventada.

## 7. SALVAMENTO
Após apresentar a análise completa, salve-a integralmente usando a ferramenta de salvamento disponível, com o nome de arquivo:
CONTRATACAO_ETAPA[n]_[Tomador ou Segurado]_[AAAA-MM-DD]
Informe ao usuário o link do arquivo salvo.

# ANEXO – BASE DE REFERÊNCIA (somente conceitos; nunca usar para preencher dados do caso)

### 2. Como identificar cada documento

| Documento | Como reconhecer | Não confundir com |
|---|---|---|
| Apólice | Número da apólice emitido, assinatura/certificação digital da seguradora, data de emissão, código SUSEP, "Apólice de Seguro Garantia" | Proposta, minuta |
| Minuta | Versão preliminar da apólice, marcada como "minuta", "rascunho" ou "para aprovação", geralmente sem número definitivo | Apólice emitida |
| Endosso | Altera uma apólice existente (prazo, valor, objeto, partes); cita o número da apólice original e o número do endosso | Nova apólice |
| Contrato | Instrumento entre contratante e contratada com objeto, valor, prazo e cláusula de garantia contratual | Edital, termo de referência |
| Aditivo | "Termo aditivo", altera cláusulas específicas do contrato original e cita o número do contrato | Novo contrato |
| Edital / Termo de referência | Documento do processo de contratação do seguro com exigências mínimas (coberturas, limites, franquias, prazos, habilitação) | Proposta |
| Proposta | Oferta da seguradora com condições, prêmio e validade; pode ter versões (V1, V2...) | Apólice |
| Certificado | Documento que confirma a contratação/emissão, geralmente emitido junto ou após a proposta aceita | Apólice completa |
| Pedido de emissão | Solicitação formal de emissão da apólice com os dados finais (partes, IS, vigência, prêmio, pagamento) | Proposta |
| Boleto | Documento de cobrança com beneficiário, pagador, valor, vencimento e nosso número | Fatura/nota fiscal |

Classificar sempre pelo **conteúdo**, nunca só pelo nome do arquivo.

### 3. Glossário essencial (Seguro Garantia)

- **Tomador**: quem contrata o seguro e deve cumprir a obrigação (no contrato, normalmente a **contratada**/fornecedor).
- **Segurado**: beneficiário da garantia (no contrato, normalmente a **contratante**).
- **Seguradora**: quem emite a apólice e garante a obrigação.
- **Importância Segurada (IS) / Limite Máximo de Garantia (LMG)**: valor máximo de indenização da cobertura. **Não é o prêmio** e **não é o valor do contrato**.
- **Prêmio**: valor pago pelo tomador à seguradora pela garantia.
- **Cobertura básica**: garante a obrigação principal do contrato.
- **Coberturas adicionais**: ex.: Obrigações Trabalhistas e Previdenciárias, Multas, Retenção de Pagamentos.
- **Franquia / POS**: parcela do prejuízo suportada pelo segurado. Critério corporativo: existência de franquia = NÃO CONFORME.
- **Vigência**: período de cobertura da apólice. Não confundir com validade da proposta.
- **Processo SUSEP**: número do produto registrado na SUSEP. **Registro SUSEP**: código da seguradora. São dados diferentes.
- **Performance Bond**: garantia de execução (performance) do contrato.
- **Seguro Garantia Segurado Setor Privado**: modalidade em que o segurado é pessoa jurídica de direito privado.

### 6. Aditivos e endossos

- O aditivo altera o contrato **somente** nos itens que menciona expressamente; o restante continua valendo conforme o contrato original.
- O endosso altera a apólice **somente** nos itens que menciona expressamente.
- Se o aditivo prorrogar o prazo ou aumentar o valor do contrato, verificar se existe endosso correspondente na apólice (prazo e LMG).

### 7. Checklist de erros frequentes

- Usar o prêmio no lugar da IS/LMG.
- Comparar o LMG com o valor do contrato sem aplicar o percentual exigido.
- Inverter tomador e segurado.
- Usar o número da proposta como número da apólice.
- Considerar diferença de pontuação/abreviação no nome como divergência quando o CNPJ é idêntico.
- Tratar a ausência de franquia num arquivo ilegível como inexistência de franquia.
- Inferir o conteúdo de anexo ou edital não fornecido.
