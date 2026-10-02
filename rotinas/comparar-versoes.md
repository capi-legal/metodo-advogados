# Rotina: comparar versões e rodadas de negociação

**Quando usar:** "chegou a nova versão", "a contraparte devolveu", "o que mudou?",
"compare com a nossa", "quais aditivos mudaram a cláusula X?".

**Resultado:** uma tabela de **todas** as mudanças entre duas versões. Mudanças que
ninguém anunciou aparecem em destaque. Para cada mudança há uma recomendação: aceitar,
contrapropor ou perguntar ao cliente.

Este é o ponto onde mais se perde coisa numa negociação: alteração feita sem marcação, sem
comentário ou fora da lista enviada pela outra parte.

---

## Passo 1: identificar e guardar

1. Pela tabela de versões da `ficha.md`, identifique a **última versão nossa** e a **versão
   recebida**. Se a ordem não estiver clara pelos nomes e datas, pergunte.
2. Salve a versão recebida, sem alterar, como `02_versoes/vNN-AAAA-MM-DD-contraparte.ext`.
   Pergunte antes de renomear um arquivo que o advogado já salvou com outro nome.
3. A contraparte mandou uma lista do que mudou (e-mail, comentários, carta)? Leia. Ela
   serve para cruzar com o que de fato mudou.

**Word com controle de alterações:** se a ferramenta não conseguir ler as marcações,
compare o texto final das duas versões. Avise que comentários e marcações não foram lidos.
Se precisar, peça uma versão "limpa" ou em PDF.

## Passo 2: comparar o texto inteiro

Compare cláusula por cláusula, não só os trechos marcados. Procure em especial:

- alterações **sem marcação**: palavras trocadas, números, prazos, "e" virando "ou";
- **definições alteradas**, que mudam o sentido do contrato inteiro;
- cláusulas **renumeradas**, com remissões internas quebradas;
- **anexos** trocados ou removidos;
- inclusões no fim do documento ou em anexos que ninguém costuma reler.

## Passo 3: montar a tabela

Salve em `03_entregas/AAAA-MM-DD-comparacao-vNN-vMM.md`:

```
[bloco "Antes de usar" de AGENTS.md §7]

# O que mudou: vNN (nossa) → vMM (contraparte)
[contrato] · [contraparte] · [data]

## Em resumo
[N] mudanças, das quais [N] não anunciadas. [N] precisam da sua decisão.

## ⚠️ Mudanças não anunciadas
[só as que não estavam marcadas nem na lista da contraparte]

## Todas as mudanças

| # | Cláusula | Antes (vNN) | Agora (vMM) | Tipo | Anunciada? | Avaliação | Recomendação |
|---|---|---|---|---|---|---|---|
| 1 | 9.2 | "12 (doze) meses" | "6 (seis) meses" | alteração | não | 🟠 fora do recuo (posicoes.md) | contrapropor 9 meses, ou perguntar ao cliente |

Uma pergunta que eu faria: [opcional]

E agora?
1. Preparo a nossa resposta: nova versão com as contrapropostas, numerada vMM+1.
2. Preparo a mensagem para o cliente decidir os pontos [decidir].
3. Preparo a mensagem para a contraparte listando o que aceitamos e o que não aceitamos.
4. Outra coisa.
```

- **Tipo:** inclusão, exclusão, alteração, renumeração ou mudança de definição.
- **Avaliação:** use as posições do lado certo e as exceções da `ficha.md`, com a mesma
  escala de gravidade de `rotinas/revisar-contrato.md`.
- Cite os textos literalmente e por completo. Não corte condições.

## Passo 4: registrar

- `ficha.md`: nova linha na tabela de versões, com "o que mudou" em uma frase; status e
  próximo passo.
- `historico.md`: entrada com quantas mudanças, quantas não anunciadas, o que foi
  recomendado e os arquivos.

---

## Modo histórico de aditivos

Use quando o pedido for "como este contrato está hoje, depois de todos os aditivos?" ou
"onde está a versão atual da cláusula X?".

1. Ordene o contrato e os aditivos pela data de assinatura. Use a data do preâmbulo e as
   referências entre documentos ("aditivo ao contrato de…").
2. Confira se as partes são as mesmas em todos os documentos. Uma parte nova ou um nome
   alterado sem cessão formal é um ponto de atenção.
3. **Visão geral:** para cada aditivo, o que mudou (antes → depois) e a cláusula. Depois,
   uma tabela "situação atual" com cada cláusula relevante, o texto vigente em resumo e
   em que documento mudou por último.
4. **Uma cláusula específica:** mostre só os documentos que a alteraram, com o texto
   literal de cada um, até chegar à redação vigente.
5. Aponte inconsistências: aditivo que altera cláusula já excluída, aditivos
   contraditórios, numeração que mudou.
