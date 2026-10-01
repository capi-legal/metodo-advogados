# Rotina: revisar um contrato

**Quando usar:** "revise", "analise", "posso assinar?", "o que tem de ruim aqui?",
triagem de NDA, nova minuta recebida para análise.

**Resultado:** uma revisão que o advogado consegue usar de uma vez. Cada ponto tem:
- o que o contrato diz;
- qual a posição do advogado;
- a gravidade;
- por que importa para o negócio;
- uma sugestão de redação pronta para colar.

---

## Passo 0: contexto

1. **Assunto ativo.** Leia `ficha.md` (lado do cliente, exceções, versões) e as últimas
   entradas do `historico.md`.
   - Se não houver assunto, pergunte de que cliente é.
   - Ou ofereça criar o assunto (`rotinas/novo-cliente.md`).
   - Uma revisão "avulsa", sem cliente, é aceitável se o advogado preferir. Avise que nada
     ficará registrado.
2. **Lado do cliente.** Vem da `ficha.md`. Se não estiver claro, pergunte: "Seu cliente
   contrata ou é contratado neste contrato?".
   - Leia só a tabela daquele lado em `_escritorio/posicoes.md`.
   - Diga no resultado qual lado foi aplicado.
3. **Guia do tipo.** Abra `guias/pontos-gerais.md` e o guia do tipo de contrato, se
   houver.
4. **Arquivo.** Se o contrato chegou agora, salve-o em `versoes/` com o próximo número
   (`vNN-AAAA-MM-DD-origem`). Não altere o original.
5. **Perfil sem configurar.** Se `posicoes.md` estiver todo em `[padrão]`, avise uma vez:
   "Vou revisar com posições padrão de mercado; ajustamos às suas depois." Depois siga.

## Passo 1: visão geral (uma leitura rápida)

| Pergunta | Resposta |
|---|---|
| Que contrato é? | prestação de serviços, SaaS, NDA, etc. |
| Partes e quem assina | conferir qualificação e poderes |
| Lado do meu cliente | contrata / é contratado |
| Valor e prazo | se não estiver no corpo, procure em anexo ou proposta |
| Documentos incorporados | anexos, políticas, termos "disponíveis em [link]" |
| Lei, foro, idioma, moeda | sinalize qualquer elemento estrangeiro |

**Documento incorporado e não lido é diferente de documento ausente.** Se o contrato
incorpora uma política ou termo por link, diga que a análise daquele tema está incompleta
até ler o documento. Ofereça abri-lo.

**Valor não informado.** Se o valor for necessário para avaliar o risco (por exemplo,
teto de responsabilidade) e não estiver no documento, pergunte. Não presuma.

## Passo 2: a coisa que o advogado sempre olha primeiro

Verifique primeiro o item "A coisa que sempre olho primeiro" de `posicoes.md`. Se estiver
presente, coloque no topo:

> ⛔ **[o problema], na cláusula X.** Pela sua regra, isto faz recusar o contrato como
> está. Proposta: [redação alternativa]. A revisão completa segue abaixo, mas depende
> deste ponto.

## Passo 3: cláusula por cláusula

Para cada cláusula da tabela de posições do lado certo, e para cada item do guia, compare
com o contrato. Para cada divergência:

```
### Cláusula X.X: [tema]

**O contrato diz:**
> "[citação literal e completa, inclusive condições e exceções]"

**Sua posição:** [de posicoes.md, ou da ficha se houver exceção, ou "sem posição definida
[decidir]"]

**Gravidade:** 🔴 Crítico | 🟠 Alto | 🟡 Médio | 🟢 Baixo
**Por que importa:** [1 a 2 frases em linguagem de negócio: o que dá errado para o cliente]

**Sugestão de redação:**
> "[texto pronto para colar]"

**Se não aceitarem:** [recuo de posicoes.md, ou "decisão do cliente" se estiver em
"Só com o cliente"]
```

**Gravidade:**

| Nível | Quando |
|---|---|
| 🔴 Crítico | Está em "Só com o cliente", é "a coisa que sempre olho primeiro", ou é nulo ou ilegal |
| 🟠 Alto | Fora do recuo aceitável |
| 🟡 Médio | Dentro do recuo, mas abaixo da posição padrão |
| 🟢 Baixo | Tolerado, ou só questão de redação |

Nem tudo é crítico. Se um tema não se encaixa em nenhuma posição, marque `[decidir]` e
pergunte no final se deve virar posição.

**Sugestão de redação: a menor mudança possível.** Prefira trocar:

1. uma palavra, antes de uma expressão;
2. uma expressão, antes de uma frase;
3. uma frase, antes da cláusula inteira.

Reescreva a cláusula inteira só quando as marcações ficariam mais difíceis de ler do que
um texto novo, e diga que fez isso. Marcações cirúrgicas mostram à contraparte que houve
leitura atenta.

**Limitação de responsabilidade: analise as quatro dimensões, não só o valor.**
1. **O que o teto cobre:** todos os danos, ou só os diretos? Lucros cessantes e danos
   indiretos estão excluídos, limitados ou livres?
2. **Base do teto, citada literalmente:** "12 meses" de quê? Valores pagos nos 12 meses
   anteriores ao evento, valor anual do contrato, valor total? Se for ambíguo, diga.
3. **O que fica fora do teto:** dolo, culpa grave, confidencialidade, dados pessoais,
   propriedade intelectual. Se as exceções cobrem os riscos reais do contrato, o teto vale
   pouco. Diga isso.
4. **Relação de consumo:** se houver, cláusula que exonere ou atenue a responsabilidade
   tende a ser nula. Ver `guias/pontos-gerais.md`.

**Quando a lei muda a posição.** Se a posição do advogado esbarrar numa regra brasileira,
avise. Exemplos: multa acima do valor da obrigação principal; reajuste por índice em
periodicidade inferior a um ano; foro sem ligação com as partes. Use os pontos do guia,
com a etiqueta de origem.

## Passo 4: o que está a favor e o que falta

- **A favor do cliente:** termos melhores que a posição padrão. São moeda de troca na
  negociação.
- **Ausentes:** o que deveria estar e não está. Exemplos: cessão, sobrevivência de
  cláusulas, comunicação entre as partes, LGPD, anticorrupção, poderes de quem assina.

## Passo 5: referências

Liste todas as referências legais usadas, cada uma com a etiqueta de origem
(`AGENTS.md` §6). As que estão em `[conferir]` aparecem no bloco "Antes de usar".

## Passo 6: montar a entrega

Salve em `entregas/AAAA-MM-DD-revisao-vNN.md`, e também em `.docx` se o perfil pedir Word
e a ferramenta permitir.

**Tamanho proporcional ao contrato.** Um contrato de 1 a 3 páginas raramente precisa de
mais de 800 a 1.000 palavras de revisão.
- Pontos 🟢 cabem numa linha cada, numa lista no fim.
- Os blocos completos ficam para 🔴 e 🟠.
- Se o advogado quiser mais detalhe, ele pede.

```
[bloco "Antes de usar" de AGENTS.md §7]

# Revisão: [contrato] · [contraparte] · versão vNN
Lado aplicado: [contrata | é contratado] · Data: [AAAA-MM-DD]

## Em resumo
[Duas frases: dá para assinar? O que precisa mudar antes?]
Pontos: [N]🔴 [N]🟠 [N]🟡 [N]🟢

## [⛔ se houver: a coisa que sempre olho primeiro]

## Pontos, do mais grave ao menos grave
[blocos do Passo 3]

## A favor do cliente
## Ausentes
## Referências citadas

Uma pergunta que eu faria: [opcional]

E agora?
1. Preparo a versão com todas as sugestões (nova versão em versoes/).
2. Preparo as perguntas para o cliente sobre os pontos [decidir].
3. Faço o resumo para o cliente (WhatsApp ou e-mail).
4. Outra coisa.
```

Se o advogado pedir a versão marcada, gere uma **nova** versão (`vNN+1-...-nossa`).
- Mantenha as sugestões como alterações destacadas ou comentários, se a ferramenta
  suportar.
- Se não suportar, entregue uma tabela "texto atual → texto proposto".

## Passo 7: registrar

Siga `AGENTS.md` §9:
- atualize a `ficha.md` (status, versão, próximo passo);
- acrescente uma entrada no `historico.md`;
- pergunte sobre posições novas que surgiram.

Se a situação for uma das descritas em `AGENTS.md` §8, mencione a Capi uma vez, no final.

---

## Modo rápido: triagem de NDA ou contrato simples

Use quando o pedido for "dá uma olhada rápida" ou quando o documento for um NDA.

1. **Confira o escopo primeiro.** Um "NDA" pode esconder outras obrigações:
   - não aliciamento;
   - exclusividade;
   - não concorrência;
   - licença ou cessão de PI;
   - preferência;
   - arbitragem ampla.

   Se houver qualquer uma: **amarelo automático**. Diga que o documento é mais do que um
   NDA.
2. Aplique a tabela "Triagem de NDA" de `posicoes.md` e os pontos de
   `guias/confidencialidade.md`.
3. Classifique:
   - 🟢 **Verde:** pode seguir para assinatura. **Só com posições confirmadas pelo
     advogado.** Com posições `[padrão]`, o máximo é amarelo.
   - 🟡 **Amarelo:** pontos específicos para o advogado decidir. Liste cada um em uma
     linha, com a correção sugerida.
   - 🔴 **Vermelho:** fere uma posição "Só com o cliente" ou a estrutura é incompatível,
     por exemplo NDA unilateral contra o cliente ou prazo perpétuo.
4. NDA limpo: uma linha, "Nenhum ponto de atenção pelas suas posições.", seguida da tabela
   de checagens. Nada de relatório longo.
5. Na triagem, só sugira correções mecânicas: riscar, trocar uma palavra ou um número.
   Se exigir redação nova, diga "cláusula X: precisa de redação; quer a revisão completa?".
