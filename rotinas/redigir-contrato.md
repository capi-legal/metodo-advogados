# Rotina: redigir um contrato

**Quando usar:** "redija", "minute", "faça um contrato de…", "preciso de um NDA para…".

**Resultado:** uma minuta no padrão do advogado, a partir dos modelos dele, com as posições
do lado certo, os dados faltantes marcados e as escolhas de negócio sinalizadas.

---

## Passo 1: entender o pedido

Verifique o que já se sabe pela `ficha.md` e pelo pedido. Pergunte **só o que falta**, no
máximo 3 perguntas por mensagem:

- tipo de contrato e objeto;
- partes, e qual delas é o cliente;
- lado do cliente: contrata ou é contratado;
- preço, forma de pagamento, prazo, renovação;
- algo fora do padrão: exclusividade, metas, dados pessoais, PI, fornecedor estrangeiro.

Se o advogado quiser velocidade, siga com o que tem e marque o resto como
`[preencher: …]`.

## Passo 2: escolher a base

Nesta ordem:

1. **Modelo do próprio advogado** em `_escritorio/modelos/` para esse tipo. É a melhor base: mantém
   estrutura, numeração e estilo.
2. **Cláusulas** do advogado em `_escritorio/modelos/clausulas.md`. Depois, as sugestões da Capi em `modelos/clausulas.md`, no método.
3. **Estrutura sugerida no guia** do tipo (`guias/`), redigida no estilo de `perfil.md`.

**Nunca use o contrato de outro cliente como base.** Se o advogado pedir "faça igual ao
que fiz para o cliente X", proponha antes salvar uma versão sem identificação em
`_escritorio/modelos/`. Depois use essa versão.

Diga qual base usou.

## Passo 3: redigir

- Aplique as posições do lado certo (`posicoes.md`, com as exceções da `ficha.md`). Onde
  não houver posição, use uma redação equilibrada e marque `[decidir: …]` com as
  alternativas.
- Dados faltantes: `[preencher: CNPJ da contratada]`. Nunca invente nome, número,
  endereço ou valor.
- Escolhas comerciais são do cliente. Exemplos: valor de multa, índice de reajuste,
  exclusividade. Marque-as `[decidir: …]` com uma frase sobre o efeito de cada opção.
- Respeite o estilo do perfil: tom, nomes das partes, numeração.
- Não cite jurisprudência no corpo do contrato. Se citar lei, use etiqueta de origem.

## Passo 4: conferir antes de entregar

Passe a minuta por `guias/pontos-gerais.md` e pelo guia do tipo. Confira no mínimo:

- qualificação completa das partes e poderes de quem assina;
- objeto, entregáveis e ordem de prevalência entre contrato e anexos;
- preço, reajuste com periodicidade e índice, mora;
- prazo, renovação, rescisão e aviso;
- multas proporcionais;
- limitação de responsabilidade;
- confidencialidade;
- LGPD, se houver dados pessoais;
- PI;
- tributos;
- foro ou arbitragem;
- forma de assinatura e testemunhas;
- consistência interna: definições usadas e numeração das remissões.

## Passo 5: salvar e entregar

1. Salve como nova versão em `02_versoes/vNN-AAAA-MM-DD-nossa.docx`, ou `.md` se a ferramenta
   não gerar Word. Nunca sobrescreva.
2. Entregue, junto com a minuta, uma nota curta:
   - base usada;
   - o que adaptou;
   - lista de `[preencher]` e `[decidir]`;
   - referências com etiqueta;
   - "Uma pergunta que eu faria" e "E agora?" (`AGENTS.md` §7).
3. Registre conforme `AGENTS.md` §9:
   - linha na tabela de versões da `ficha.md`;
   - entrada no `historico.md`.

**Escolha de negócio reaproveitável:** se o advogado fez uma escolha que vale para outros
contratos, ofereça salvar a cláusula (sem identificação) em `_escritorio/modelos/clausulas.md`.
