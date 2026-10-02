# Rotina: novo cliente, novo assunto, ou organizar um cliente existente

**Quando usar:**
- "novo cliente";
- "abre um assunto para…";
- "chegou um contrato do cliente X" e o assunto ainda não existe;
- "organiza a pasta do cliente Y".

---

## Passo 1: checar conflito

Antes de criar qualquer coisa, leia `_escritorio/clientes.md` e procure:

- o novo cliente entre as **contrapartes** de outros clientes;
- a **contraparte** do novo assunto entre os **clientes** atuais e antigos.

Se encontrar algo, informe objetivamente: "A Fornecedora Alfa aparece como contraparte em
um assunto da Padaria Silva (2026)". A análise de conflito e a decisão são do advogado; o
assistente só aponta o que encontrou no índice.

Não abra as pastas desses clientes para investigar.

## Passo 2: criar ou localizar o cliente

**Cliente novo:**

1. Crie `clientes/<nome-curto>/`, por exemplo `clientes/padaria-silva/`, com letras
   minúsculas, sem acento e com hífens. Se `_escritorio/configuracao` indicar outra pasta
   de clientes, use-a.
2. Crie dentro dela o registro `cliente` a partir de `estrutura/cliente/cliente.md`, no
   método. Use o formato de `_escritorio/configuracao` (`.md` ou Google Docs). Preencha o
   essencial. Pergunte só o que falta:
   - nome ou razão social;
   - CPF ou CNPJ;
   - quem assina e com que poderes;
   - contato;
   - canal preferido.

   O resto pode ficar `[preencher]`.
3. Acrescente uma linha em `_escritorio/clientes.md`. Se ainda houver linha de exemplo,
   apague-a.

**Cliente existente:** abra o registro `cliente` dele e siga.

## Passo 3: criar o assunto

1. Crie a pasta `clientes/<cliente>/AAAA-MM_assunto-curto/`, por exemplo
   `2026-10_saas-gestao-estoque/`, com as subpastas `01_documentos/`, `02_versoes/` e
   `03_entregas/`. O assunto é **neutro**: descreve o objeto do contrato, nunca o nome da
   contraparte, de pessoas, motivos ou valores. Regras de nomes em `estrutura/LEIA-ME.md`.
2. Crie `ficha` e `historico` a partir de `estrutura/assunto/`, no formato da
   configuração, e preencha a `ficha`:
   - contraparte;
   - tipo;
   - lado do cliente;
   - de quem é a minuta;
   - valor e prazo, se já souber;
   - o que o cliente quer, em 2 a 5 frases;
   - próximo passo;
   - **IA pode ler esta pasta?**: "sim", salvo se o termo de uso de IA do cliente foi
     recusado (`cliente.md`) ou o advogado disser outra coisa. Na dúvida, pergunte.
3. Se veio um contrato, salve uma cópia fiel como `02_versoes/v01-AAAA-MM-DD-origem.ext` e
   registre na tabela de versões. **Não duplique o contrato em `01_documentos/`**: a v01 já
   é o original. Outros arquivos (contrato social, e-mails, conversas) vão para
   `01_documentos/`, com nome `AAAA-MM-DD_tipo_descritor.ext`.
4. `historico`: primeira entrada, "Assunto aberto".
5. Atualize a tabela "Assuntos" do registro `cliente` e a coluna "Assuntos ativos" do índice.

## Passo 4: documentos de início (opcional, pergunte)

Pergunte: "Quer que eu prepare os documentos de início? Proposta de honorários, contrato
de honorários, procuração."

- **Use os modelos do advogado** em `_escritorio/modelos/`, preenchendo com o registro
  `cliente`.
- **Nome e OAB do advogado:** leia de `_escritorio/perfil`. Se estiverem vazios, pergunte
  uma vez e grave no perfil. Não grave na memória do assistente.
- Se ele não tiver modelo, ofereça um rascunho. Os valores de honorários ficam
  `[decidir: valor e forma de cobrança]`. **Os honorários são decisão do advogado.** Não
  sugira valores. Se ele perguntar, lembre que existe a tabela de honorários da seccional
  da OAB.
- **Termo de uso de IA:** veja `perfil.md`.
  - Se for "sim", gere a partir de `modelos/termo-de-uso-de-ia.md` (termo separado ou
    cláusula, conforme o perfil).
  - Se ainda não decidido, pergunte **uma vez**: "Quer usar um termo de ciência sobre uso
    de IA com seus clientes? A Recomendação CFOAB 001/2024 orienta formalizar o uso de IA
    com o cliente." Grave a resposta no perfil e não pergunte de novo.
  - Registre o status no `cliente.md`.
- Salve tudo em `01_documentos/` do assunto, ou na pasta do cliente, como **novos** arquivos.

## Passo 5: fechar

Mostre em até 6 linhas o que foi criado e onde. Ofereça o próximo passo natural, por
exemplo: "Quer que eu revise a v01 agora?".

---

## Organizar um cliente que já existe (pastas antigas)

Use quando o advogado já tem uma pasta do cliente no Drive ou OneDrive, com arquivos
soltos. Veja as duas opções (adaptar no lugar ou data de corte com `_legado/`) em
`estrutura/LEIA-ME.md`. Se o advogado ainda não escolheu, pergunte uma vez.

1. **Não mova nem renomeie nada sem perguntar.**
2. Liste o que existe: tipos de documento, contratos aparentes, versões, datas.
3. Crie `cliente.md` na pasta do cliente. Para cada contrato em andamento, crie a pasta do
   assunto com `ficha.md` e `historico.md`.
   - Na tabela de versões, **aponte para os arquivos onde estão hoje** (caminho
     relativo).
4. Proponha uma reorganização: o que iria para `01_documentos/`, `02_versoes/` e
   `03_entregas/`, com os nomes no padrão. Só execute se o advogado aprovar. **Copie, não
   mova**, e registre no `historico.md` os nomes originais dos arquivos renomeados.
5. Contratos já assinados: ofereça extrair as datas (`rotinas/datas-do-contrato.md`).
