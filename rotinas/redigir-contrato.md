# Rotina: redigir um contrato

**Quando usar:** "redija", "minute", "faça um contrato de…", "preciso de um NDA para…".

**Resultado:** uma minuta no padrão do advogado, a partir dos modelos dele, com as posições
do lado certo, a formatação dele, as escolhas de negócio sinalizadas e, se algo ficou em
aberto, a lista do que falta.

---

## Passo 1: entender o pedido

Verifique o que já se sabe pela `ficha.md`, pelos documentos do assunto e pelo pedido.
**Não redija antes de ter o básico**, nem entregue uma minuta cheia de lacunas sem o
advogado ter escolhido isso.

**O básico**, que toda minuta precisa ter respondido ou conscientemente deixado para
depois:
1. **Partes:** quem são, e qual delas é o cliente (contrata ou é contratado).
2. **Lei aplicável e foro:** lei brasileira e foro de qual cidade, ou arbitragem.
3. **Idioma:** português, outro idioma ou bilíngue.
4. **Prazo:** vigência, renovação e aviso para encerrar.

Por cima do básico, o que o tipo de contrato exige: objeto e entregáveis, preço e forma
de pagamento, e o que o guia do tipo (`guias/`) apontar como essencial (exclusividade,
dados pessoais, PI, fornecedor estrangeiro).

**Se o pedido já traz o básico:** não pergunte de novo. Pergunte só o que faltar do tipo,
se for essencial, e siga.

**Se o pedido é curto e falta o básico:** antes de redigir, ofereça a escolha, em uma
mensagem:

> Para a minuta sair pronta, faltam alguns dados. Prefere:
> 1. responder agora (umas N perguntas rápidas, em 2 ou 3 mensagens); ou
> 2. ver primeiro um esqueleto e completar depois?

- **Opção 1:** pergunte em rodadas, **no máximo 3 perguntas por mensagem**, numeradas e
  curtas: primeiro o básico que faltar, depois o essencial do tipo de contrato. Siga
  perguntando até ter o necessário para uma minuta sem lacunas; em geral bastam 2 ou 3
  rodadas. Não pergunte o que a resposta anterior já trouxe. Se o advogado disser "pode
  seguir" no meio do caminho, o que ficou sem resposta segue a opção 2.
- **Opção 2:** redija o esqueleto e abra a entrega com **"Em aberto"**: a lista do que
  falta, escrita como perguntas ("Qual o prazo de vigência?"), com a cláusula onde cada
  resposta entra. No texto, cada lacuna é `[preencher: …]` e aparece nessa lista. Nenhuma
  lacuna fica só no corpo do contrato.
- Se o advogado já disse que quer velocidade ou um esqueleto, não ofereça a escolha: siga
  a opção 2.

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
- Respeite o estilo do perfil (nomes das partes, particularidades de redação) e a
  formatação de `_escritorio/formatacao.md` (como aplicar: `modelos/formatacao.md`).
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
   não gerar Word. Nunca sobrescreva. No `.docx`, aplique `_escritorio/formatacao.md`, de
   preferência a partir do arquivo de referência indicado lá, e confira o arquivo gerado.
2. Entregue, junto com a minuta, uma nota curta:
   - base usada;
   - o que adaptou;
   - lista de `[preencher]` (a mesma de "Em aberto", se houver) e `[decidir]`;
   - referências com etiqueta;
   - "Uma pergunta que eu faria" e "E agora?" (`AGENTS.md` §7).
3. Registre conforme `AGENTS.md` §9:
   - linha na tabela de versões da `ficha.md`;
   - entrada no `historico.md`.

**Escolha de negócio reaproveitável:** se o advogado fez uma escolha que vale para outros
contratos, ofereça salvar a cláusula (sem identificação) em `_escritorio/modelos/clausulas.md`.
