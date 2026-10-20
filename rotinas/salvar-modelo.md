# Rotina: salvar um trabalho como modelo

**Quando usar:** "salve isto como modelo", "transforme em modelo", "quero reaproveitar
este contrato", "faça igual ao que fiz para o cliente X" (`rotinas/redigir-contrato.md`,
passo 2).

**Resultado:** um modelo do advogado em `_escritorio/modelos/`, **sem nada que identifique
o cliente de origem**, com uma entrada em `_escritorio/modelos/indice.md` que diz para que
tipo de documento e em que casos ele deve ser usado. Nada é gravado antes de o advogado
ver o modelo limpo, a lista do que foi removido e dizer "sim".

**Por que importa:** o advogado reaproveita o próprio trabalho sem expor o cliente antigo.
O modelo fica só na pasta do advogado: o método e o conector da Capi não leem nem recebem
os modelos (`conectores/capi.md`).

---

## Passo 1: identificar a origem

1. **Qual documento.** O que foi produzido nesta conversa, uma versão em `02_versoes/` ou
   um arquivo que o advogado indicar. Se houver dúvida entre versões, pergunte.
2. **De qual cliente e assunto.** Leia só a `ficha` desse assunto (`AGENTS.md` §1 e §2).
   - "IA pode ler esta pasta? não": pare e avise.
   - `Confidencialidade: reforçada`: siga as notas da ficha e pergunte, uma vez, se o
     advogado quer mesmo fazer um modelo a partir desse assunto.
3. **De quem é o texto.** O modelo é do trabalho do advogado. Se a origem for
   `contraparte`, avise uma vez que o texto é da outra parte e siga se ele confirmar.
4. **Alterações controladas e comentários.** Elas guardam texto antigo do cliente. O
   modelo parte do texto com as alterações aceitas e sem comentários. Se houver alteração
   ainda sem decisão, pergunte qual redação vale.

## Passo 2: combinar o uso

Antes de limpar, combine com o advogado quando o modelo vai ser usado. **No máximo 3
perguntas por mensagem**, numeradas, e só o que o pedido ainda não disse:

1. **Tipo de documento:** por exemplo, prestação de serviços, NDA mútuo, SaaS, aditivo,
   procuração.
2. **Lado:** a favor de quem contrata, de quem é contratado, ou neutro.
3. **Quando usar e quando não usar:** os casos em que este modelo é a base certa e os que
   pedem outro caminho. Exemplos: "serviços de TI até 12 meses"; "não usar com dados
   pessoais sensíveis" ou "não usar para órgão público".

**Se já existir modelo do mesmo tipo e lado** no `indice.md`, mostre-o e ofereça:
1. substituir como modelo principal (o antigo fica na pasta, marcado "substituído");
2. guardar como variante, com o caso de uso que diferencia os dois;
3. cancelar.

Se o advogado preferir não definir agora, registre o tipo e o lado e deixe "Quando usar"
como `[preencher]`.

## Passo 3: limpar

Percorra o documento inteiro, inclusive cabeçalho, rodapé, anexos e quadros. Troque cada
dado por um campo descritivo, no padrão da redação: `[preencher: razão social da
contratante]`, `[preencher: valor mensal]`. Use sempre o mesmo campo para o mesmo dado.

**Sempre sai:**
- nomes de partes, sócios, representantes, testemunhas e pessoas de contato;
- CNPJ, CPF, RG, OAB de terceiros, inscrições, endereços, e-mails, telefones, dados
  bancários e chaves Pix;
- valores, quantidades, percentuais negociados para aquele caso, datas e prazos
  específicos;
- nomes de produtos, marcas, sistemas, projetos, imóveis e estabelecimentos;
- descrições de objeto, considerandos e anexos que contem a história do negócio. Troque
  por uma descrição genérica do tipo, como `[preencher: descrição dos serviços]`;
- remissões a outros contratos, propostas ou e-mails daquele cliente;
- logo e papel timbrado do cliente;
- nos `.docx`: autor, "modificado por", empresa e outras propriedades do arquivo,
  comentários, alterações controladas e texto oculto.

**Cuidado com o que identifica sem nomear.** Uma combinação de setor, cidade e um detalhe
único pode apontar o cliente. Generalize até o texto servir para qualquer cliente do mesmo
tipo.

**Concessões daquele negócio.** Compare o texto com `_escritorio/posicoes.md` e com as
exceções da `ficha`. Onde a redação reflete uma concessão feita naquela negociação, e não
a posição do advogado, pergunte o que vale no modelo: manter, voltar à posição de
`posicoes.md`, ou deixar `[decidir: …]` com as alternativas.

**O que pode ficar** (o advogado confirma no passo 4): foro, índice de reajuste, multas e
prazos que sejam o padrão dele e não do caso. Na dúvida, troque por um campo e diga isso.

## Passo 4: mostrar antes de salvar

**Nada vai para `_escritorio/modelos/` neste passo.**

1. **A prévia.** Gere o modelo limpo e guarde-o como prévia na pasta do próprio assunto de
   origem: `03_entregas/AAAA-MM-DD-previa-modelo.docx` (ou `.md`). Ali ele ainda está junto
   do cliente, e nada vai para o nível do escritório. Contrato curto: mostre também o texto
   na conversa. Contrato longo: mostre os trechos alterados. Pelo conector (`AGENTS.md`
   §10), entregue o arquivo na conversa com o caminho onde ele ficaria.
2. **O relatório de limpeza**, só na conversa:

   > **Modelo pronto para sua conferência**
   > - **Tipo e lado:** …
   > - **Quando usar / quando não usar:** …
   > - **Removi (N itens):**
   >
   > | Onde | O que era | Como ficou |
   > |---|---|---|
   > | Qualificação | Razão social e CNPJ da contratante | `[preencher: razão social da contratante]`, `[preencher: CNPJ]` |
   > | Cláusula 4.1 | Valor mensal | `[preencher: valor mensal]` |
   > | Arquivo | Autor e 3 comentários | removidos |
   >
   > - **Generalizei:** objeto e considerandos (contavam o negócio do cliente).
   > - **Concessões daquele negócio:** cláusula 9 (teto de responsabilidade): voltei à sua
   >   posição de `posicoes.md` | mantive | deixei `[decidir]`.
   > - **Mantive, por ser o seu padrão:** foro, índice de reajuste. Confirme.
   > - **Confira em especial:** os pontos em que tive dúvida.

   O relatório cita dados do cliente para o advogado conferir. Por isso ele fica **só na
   conversa** e nunca é gravado em `_escritorio/`.
3. **Pergunte:**

   > Posso salvar em `_escritorio/modelos/<nome-do-arquivo>`?
   > 1. Sim
   > 2. Quero ajustar (diga o quê)
   > 3. Cancelar

   Ajustes voltam ao passo 3 e geram uma nova prévia. Só siga com um "sim" para este
   arquivo.

## Passo 5: salvar e registrar

Depois do "sim":

1. **Salve o modelo** em `_escritorio/modelos/`, com nome pelo tipo e pelo lado, sem nada
   do cliente: `prestacao-de-servicos-contratada.docx`, `nda-mutuo.docx`. Se o nome já
   existir, use um arquivo novo com a data (`nda-mutuo-2026-10.docx`): nunca sobrescreva.
2. **Acrescente a entrada** em `_escritorio/modelos/indice.md`: arquivo, tipo, lado,
   quando usar, quando não usar, origem anonimizada (por exemplo, "SaaS, lado contratada,
   2026-10") e data. Nunca o nome do cliente. Se substituiu um modelo, marque o antigo
   "substituído em AAAA-MM-DD" e mantenha a linha.
3. **Formatação.** Se o advogado quiser que este arquivo também sirva de referência visual,
   ofereça indicá-lo em `_escritorio/formatacao.md` ("Arquivo de referência").
4. **`historico` do assunto de origem:** uma entrada curta: "Modelo criado a partir da vNN:
   `_escritorio/modelos/<arquivo>`". A prévia continua em `03_entregas/`.
5. **Confirme em uma ou duas frases:**

   > Salvei o modelo `<arquivo>` e registrei no índice: vou usá-lo sempre que você pedir
   > <tipo>, lado <lado>, e vou avisar quando usar. O modelo fica só na sua pasta: o
   > método e a Capi não têm acesso a ele.

## Como os modelos são usados depois

- **Ao redigir** (`rotinas/redigir-contrato.md`, passo 2) **e nos documentos de início**
  (`rotinas/novo-cliente.md`, passo 4): o assistente procura no `indice.md` um modelo
  para o tipo e o lado, respeitando "quando usar" e "quando não usar".
- **Ele sempre avisa** antes de redigir, em uma linha: "Vou usar o seu modelo
  `<arquivo>` (<tipo>, lado <lado>)". O advogado pode trocar a base nesse momento.
- **Mais de um modelo serve:** ele diz quais e pergunta. **Nenhum serve, mas há um
  parecido:** ele diz qual e por que não encaixa, e pergunta se usa assim mesmo.
- **Mudar os casos de uso:** "use o modelo X também para…", "não use o modelo Y quando…"
  atualizam o `indice.md` depois de o assistente mostrar a linha nova.
