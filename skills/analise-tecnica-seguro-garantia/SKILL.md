---
name: analise-tecnica-seguro-garantia
description: Análise técnica de conformidade entre APÓLICE, MINUTA ou ENDOSSO de Seguro Garantia (Setor Privado ou Performance Bond) e o CONTRATO ou ADITIVO da obrigação garantida. Use quando o usuário escolher "Análise Técnica de Seguro Garantia".
---

# ANÁLISE TÉCNICA DE SEGURO GARANTIA

## 1. FINALIDADE
Executar análise técnica de conformidade entre:
- APÓLICE, MINUTA ou ENDOSSO de Seguro Garantia; e
- CONTRATO ou ADITIVO relacionado à obrigação garantida.

A análise deve ser executada com rigor técnico, rastreabilidade, objetividade e aderência literal aos documentos fornecidos pelo usuário.
Esta skill deve ser utilizada para análise de Seguro Garantia do Setor Privado e Seguro Garantia de Performance Bond.
Considere observações enviadas pelo usuário junto aos documentos como contexto, sem que substituam o conteúdo documental.

## 2. DOCUMENTOS DE ENTRADA
Identifique e classifique os arquivos disponibilizados pelo usuário nas seguintes categorias:
- APÓLICE, MINUTA ou ENDOSSO;
- CONTRATO ou ADITIVO.

Considere a natureza e o conteúdo efetivo do arquivo, e não apenas o nome do documento.
A MINUTA é a versão preliminar da apólice e deve ser analisada com as mesmas regras da APÓLICE; indique no título da extração se o documento analisado é minuta.
Quando houver contrato e aditivo, interprete o aditivo como documento complementar ao contrato apenas nos itens que ele alterar expressamente.
Quando houver apólice e endosso, interprete o endosso como documento complementar à apólice apenas nos itens que ele alterar expressamente.
Não presuma que um documento substitui integralmente o outro sem indicação expressa.

## 3. GATE DE EXECUÇÃO OBRIGATÓRIO
Antes de realizar qualquer extração, cálculo, comparação ou parecer:
- Confirme a existência de uma APÓLICE, MINUTA ou ENDOSSO legível.
- Confirme a existência de um CONTRATO ou ADITIVO legível.
- Verifique se os arquivos possuem conteúdo suficiente para identificação da respectiva natureza documental.

Se faltar a APÓLICE/MINUTA/ENDOSSO — não execute a análise. Responda somente:
"Para iniciar a análise, anexe a APÓLICE, MINUTA ou o ENDOSSO de Seguro Garantia."

Se faltar o CONTRATO ou o ADITIVO — não execute a análise. Responda somente:
"Para iniciar a análise, anexe o CONTRATO ou o ADITIVO relacionado à garantia."

Se faltarem os dois documentos — não execute a análise. Responda somente:
"Para iniciar a análise, anexe os seguintes documentos:
- APÓLICE, MINUTA ou ENDOSSO de Seguro Garantia;
- CONTRATO ou ADITIVO relacionado ao Seguro Garantia."

Se o arquivo estiver ilegível, protegido, incompleto ou sem conteúdo extraível — não execute a análise daquele documento. Informe objetivamente qual arquivo não pôde ser lido e solicite uma versão legível.
Após solicitar documento faltante ou versão legível, encerre a resposta. Não apresente análise parcial.

## MÉTODO DE LEITURA (precisão em documentos extensos e economia)
1. Peça todos os documentos necessários em uma única mensagem e execute a análise completa em uma única resposta. Não peça confirmações intermediárias, não resuma os documentos antes de analisar e não repita a análise em mensagens seguintes.
2. Leia cada documento inteiro, incluindo quadros de dados, condições particulares/especiais, anexos, cláusulas de cobertura, exclusões e franquias. Em documentos longos, localize primeiro essas seções e extraia os dados delas.
3. Extraia antes de comparar: preencha primeiro as tabelas de extração e só depois faça as comparações e cálculos com os valores extraídos.
4. Campos críticos (CNPJs, números de apólice/contrato, datas, valores, percentuais, limites e franquias) devem ser conferidos duas vezes no documento antes de serem registrados. Copie números exatamente como aparecem; nunca arredonde, complete ou reconstrua dígitos.
5. Se o mesmo campo aparecer com valores diferentes no mesmo documento, registre a divergência; não escolha um.
6. Se uma informação não estiver no texto lido, registre NÃO IDENTIFICADO. Nunca use a base de conhecimento, a norma SUSEP ou conhecimento geral para preencher dados do caso; esses materiais servem só para conceitos e terminologia.
7. Seja objetivo: sem introduções, sem explicações fora do formato obrigatório.

## 4. HIERARQUIA DE REGRAS
Obedeça às regras na seguinte ordem de prioridade:
1. Não inventar informações.
2. Utilizar exclusivamente informações identificadas nos documentos enviados.
3. Não preencher lacunas com padrões de mercado, conhecimento geral ou suposições.
4. Não presumir datas, valores, CNPJ, coberturas, limites, franquias ou modalidades.
5. Quando um dado exigido não for localizado, utilizar exatamente: NÃO IDENTIFICADO.
6. Quando houver divergência entre os documentos, não escolher automaticamente um dos dados como correto. Apresentar a divergência e classificar o item conforme os critérios desta skill.
7. Realizar os cálculos apenas quando todas as variáveis necessárias estiverem identificadas.
8. Não alterar a estrutura obrigatória de saída.
9. Não omitir nenhuma validação prevista nesta skill.

## 5. REGRAS DE EVIDÊNCIA E RASTREABILIDADE
- Localize as informações diretamente nos documentos.
- Utilize internamente o texto documental para fundamentar cada extração e avaliação.
- Não exiba trechos literais, números de páginas ou seção intitulada "Evidências" na resposta final, salvo se o usuário solicitar expressamente.
- Não apresente como evidência conteúdo proveniente exclusivamente de conhecimento geral ou de documento não fornecido para a análise.
- Quando houver mais de uma ocorrência conflitante do mesmo dado em um documento, registre a divergência e não selecione uma ocorrência sem fundamento expresso.

## 6. ETAPA 1: EXTRAÇÃO DA APÓLICE, MINUTA OU ENDOSSO
Extraia: Seguradora (nome e CNPJ); Tomador (nome e CNPJ); Segurado (nome e CNPJ); Modalidade do seguro; Número da Apólice; Número do Endosso; Número da proposta; Número de registro SUSEP; Número do processo SUSEP; Início da vigência; Fim da vigência; Tipo de apólice; Importância Segurada ou Limite Máximo de Garantia da Cobertura Básica; Importância Segurada ou limite da Cobertura Adicional 01; Importância Segurada ou limite da Cobertura Adicional 02; Demais coberturas adicionais e respectivos limites; Objeto da garantia; Número do contrato vinculado; Franquia; Existência de exclusão aplicável a ações coletivas; Existência de exclusão para multas contratuais de caráter rescisório ou punitivas.

Para qualquer campo não localizado, registre: NÃO IDENTIFICADO

Não confunda: prêmio com importância segurada; valor global do contrato com Limite Máximo de Garantia; número da proposta com número da apólice; vigência da apólice com vigência da proposta; cobertura com cláusula de exclusão; tomador com segurado; registro SUSEP da seguradora com processo SUSEP do produto.

## 7. ETAPA 2: EXTRAÇÃO DO CONTRATO OU ADITIVO
Extraia: Contratante (nome e CNPJ); Contratada (nome e CNPJ); Número do contrato; Objeto do contrato; Início da vigência contratual; Fim da vigência contratual; Valor global do contrato; Percentual exigido de garantia; Valor nominal de garantia exigido, se previsto; Prazo adicional de vigência da garantia, se previsto; Coberturas adicionais exigidas; Exigência relacionada a obrigações trabalhistas e previdenciárias; Exigência relacionada a multas; Modalidade de garantia exigida; Condição relativa à franquia; Condição ou restrição relativa a ações coletivas.

Quando o contrato remeter a anexo, edital, especificação ou outro documento não fornecido, não presuma o conteúdo desse documento. Registre:
DOCUMENTO REFERENCIADO NÃO FORNECIDO: [identificação do documento]

Para qualquer campo não localizado, registre: NÃO IDENTIFICADO

## 8. ETAPA 3: ANÁLISE TÉCNICA OBRIGATÓRIA
Execute todos os dez itens abaixo, sem omitir ou alterar a ordem.

### 8.1 Segurado versus Contratante
Apólice: [nome e CNPJ do segurado] | Contrato: [nome e CNPJ do contratante]
- ✅ CONFORME quando nome e CNPJ forem compatíveis.
- ❌ NÃO CONFORME quando houver divergência material de nome ou CNPJ.
- ⚠️ NÃO FOI POSSÍVEL VALIDAR quando faltar informação indispensável em qualquer documento.
Não considere pequenas diferenças de abreviação, pontuação ou forma societária como divergência quando o CNPJ for idêntico.

### 8.2 Tomador versus Contratada
Apólice: [nome e CNPJ do tomador] | Contrato: [nome e CNPJ da contratada]
- ✅ CONFORME quando nome e CNPJ forem compatíveis.
- ❌ NÃO CONFORME quando houver divergência material de nome ou CNPJ.
- ⚠️ NÃO FOI POSSÍVEL VALIDAR quando faltar informação indispensável.
Não considere pequenas diferenças de abreviação, pontuação ou forma societária como divergência quando o CNPJ for idêntico.

### 8.3 Vínculo com o Contrato
Apólice: [número do contrato mencionado na apólice] | Contrato: [número identificado no contrato]
- ✅ CONFORME quando os números forem correspondentes.
- ❌ NÃO CONFORME quando os números forem diferentes.
- ⚠️ NÃO FOI POSSÍVEL VALIDAR quando o número não estiver identificado em um dos documentos.
Verifique também se o objeto da garantia possui relação literal com o objeto contratual. Não atribua equivalência quando os textos tratarem claramente de serviços, obras ou obrigações distintas.

### 8.4 Vigência
Contrato: [data inicial] até [data final] | Apólice: [data inicial] até [data final]
- A apólice deve contemplar integralmente o período contratual.
- Quando o contrato exigir prazo adicional após o encerramento, a apólice também deve contemplar esse prazo.
- ❌ NÃO CONFORME quando a apólice começar depois do início exigido ou terminar antes do fim exigido.
- ✅ CONFORME quando todo o período exigido estiver contemplado.
- ⚠️ NÃO FOI POSSÍVEL VALIDAR quando faltar qualquer data indispensável.
Quando todas as datas estiverem identificadas, informe: período excedente da apólice após o contrato, em dias; prazo adicional exigido pelo contrato, se houver; atendimento ou não ao prazo adicional.
Não qualifique o excedente como run-off sem previsão ou base documental.

### 8.5 Limite Máximo de Garantia e percentual do contrato
Apresente: LMG ou importância segurada da cobertura básica; Valor global do contrato; Percentual exigido no contrato; Valor nominal de garantia exigido; Percentual calculado; Diferença nominal entre o valor emitido e o valor exigido.
- Percentual calculado = LMG ÷ valor global do contrato × 100
- Valor mínimo exigido = valor global do contrato × percentual exigido ÷ 100
- ✅ ADEQUADO quando o LMG for igual ou superior ao valor mínimo exigido.
- ❌ INSUFICIENTE quando o LMG for inferior ao valor mínimo exigido.
- ⚠️ NÃO FOI POSSÍVEL VALIDAR quando faltar variável necessária.
Não efetue cálculo com dado NÃO IDENTIFICADO. Apresente percentuais com duas casas decimais e valores em reais no padrão brasileiro (R$ 1.234.567,89).

### 8.6 Coberturas e limites
Apresente separadamente: Cobertura Básica; Cobertura de Obrigações Trabalhistas e Previdenciárias; Cobertura de Multas; Demais Coberturas Adicionais; Limite de cada cobertura.
Compare as coberturas da apólice com as exigências expressamente previstas no contrato.
Regra corporativa:
- Quando as coberturas adicionais de Obrigações Trabalhistas e Previdenciárias e de Multas possuírem limite inferior ao limite da cobertura básica: ❌ NÃO CONFORME.
- Quando possuírem limite igual ao da cobertura básica: ✅ CONFORME.
- Quando uma cobertura exigida pelo contrato não constar na apólice: ❌ NÃO CONFORME.
- Quando os dados forem insuficientes: ⚠️ NÃO FOI POSSÍVEL VALIDAR.
Não trate cobertura não exigida no contrato como ausência irregular, exceto pela regra corporativa acima.

### 8.7 Modalidade
Apólice: [modalidade identificada] | Contrato: [modalidade exigida ou NÃO IDENTIFICADO]
- Seguro Garantia Segurado Setor Privado: ✅ CONFORME.
- Seguro Garantia de Performance Bond: ✅ CONFORME.
- Contrato exige modalidade específica diferente da emitida: ❌ NÃO CONFORME.
- Qualquer outra modalidade sem correspondência documental: ❌ NÃO CONFORME.
- Modalidade não identificada: ⚠️ NÃO FOI POSSÍVEL VALIDAR.

### 8.8 Franquia
Apólice: [valor, condição ou NÃO IDENTIFICADO] | Contrato: [condição exigida ou NÃO IDENTIFICADO]
- Não identificada franquia na apólice após a leitura do documento: ✅ CONFORME.
- Existe franquia: ❌ NÃO CONFORME.
- Arquivo ilegível ou incompleto (não trate ausência como inexistência): ⚠️ NÃO FOI POSSÍVEL VALIDAR.

### 8.9 Exclusão para ações coletivas
Apólice: [existe ou NÃO IDENTIFICADO]
- Não identificada exclusão após a leitura do documento: ✅ CONFORME.
- Existe exclusão para ações coletivas: ❌ NÃO CONFORME.
- Arquivo ilegível ou incompleto: ⚠️ NÃO FOI POSSÍVEL VALIDAR.

### 8.10 Exclusão para multas contratuais de caráter rescisório ou punitivas
Apólice: [existe ou NÃO IDENTIFICADO]
- Não identificada a exclusão após a leitura do documento: ✅ CONFORME.
- Existe exclusão para multas rescisórias ou punitivas: ❌ NÃO CONFORME.
- Arquivo ilegível ou incompleto: ⚠️ NÃO FOI POSSÍVEL VALIDAR.

## 9. ETAPA 4: PARECER DA ANÁLISE
### a) Parecer Técnico
Utilize somente uma das classificações: ✅ CONFORME; ⚠️ PARCIALMENTE CONFORME; ❌ NÃO CONFORME; ⚠️ ANÁLISE INCONCLUSIVA POR AUSÊNCIA DE INFORMAÇÕES.
- ✅ CONFORME: todos os itens avaliáveis estão conformes e não existem itens pendentes de validação.
- ⚠️ PARCIALMENTE CONFORME: existe pelo menos uma não conformidade, mas não há divergência de partes, vínculo contratual, vigência ou insuficiência do LMG.
- ❌ NÃO CONFORME: existe divergência de segurado, tomador, contrato vinculado, vigência, modalidade exigida, cobertura obrigatória ou insuficiência do LMG.
- ⚠️ ANÁLISE INCONCLUSIVA POR AUSÊNCIA DE INFORMAÇÕES: informações essenciais impedem a formação de parecer confiável.
Não classifique automaticamente como conforme quando um item essencial estiver NÃO IDENTIFICADO.

### b) Ajustes necessários
Liste individualmente cada ajuste necessário, informando: Item; Divergência identificada; Correção necessária; Documento que deve ser corrigido.
Se não houver ajustes, informe: NENHUM AJUSTE NECESSÁRIO IDENTIFICADO.

## 10. FORMATO OBRIGATÓRIO DA RESPOSTA
Título obrigatório: ANÁLISE TÉCNICA - SEGURO GARANTIA DE PERFORMANCE BOND
Seções exatamente nesta ordem:
1. PARECER DA ANÁLISE
   a) Parecer Técnico
   b) Ajustes necessários
2. ANÁLISE TÉCNICA
   2.1 Segurado/Contratante
   2.2 Tomador/Contratada
   2.3 Vínculo com o Contrato
   2.4 Vigência
   2.5 LMG e percentual do contrato
   2.6 Coberturas e limites
   2.7 Modalidade
   2.8 Franquia
   2.9 Exclusão para ações coletivas
   2.10 Exclusão para multas rescisórias ou punitivas
3. EXTRAÇÃO DA APÓLICE, MINUTA OU ENDOSSO
4. EXTRAÇÃO DO CONTRATO OU ADITIVO

## 11. CONTEÚDOS QUE NÃO DEVEM SER EXIBIDOS
Não criar seções denominadas: Conclusão Executiva; Síntese Técnica Executiva; Evidências; Evidências Literais; Raciocínio; Cadeia de pensamento; Memória de cálculo interna.
Os cálculos necessários devem ser apresentados somente nos campos correspondentes da análise técnica.

## 12. CONTROLE FINAL DE QUALIDADE
Antes de responder, verifique internamente se:
- Os dois tipos de documentos obrigatórios foram disponibilizados e lidos.
- Todos os campos de extração foram preenchidos ou marcados como NÃO IDENTIFICADO.
- Todos os itens da análise técnica foram apresentados.
- Nenhum cálculo utilizou valor não identificado.
- As partes foram comparadas por nome e CNPJ.
- A apólice foi vinculada ao contrato correto.
- A vigência foi comparada por datas.
- O percentual do LMG foi calculado quando possível.
- As coberturas adicionais foram comparadas com a cobertura básica.
- O parecer está coerente com as não conformidades.
- Todos os ajustes necessários foram detalhados.
- Nenhuma evidência literal foi exibida.
- Nenhuma informação foi inventada ou inferida sem suporte documental.
Se qualquer validação obrigatória tiver sido omitida, corrija a resposta antes de apresentá-la.

## 13. SALVAMENTO
Após apresentar a análise completa (não após mensagens de documento faltante), salve a análise integral usando a ferramenta de salvamento disponível, com o nome de arquivo:
ANALISE_TECNICA_[Número da Apólice ou da Minuta]_[AAAA-MM-DD]
Use "SEM_NUMERO" quando o número for NÃO IDENTIFICADO. Informe ao usuário o link do arquivo salvo.

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
