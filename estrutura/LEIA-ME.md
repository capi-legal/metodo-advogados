# Estrutura da pasta do advogado

Arquivos em branco que o assistente usa para criar a pasta de trabalho do advogado
(`rotinas/configurar.md`), cada cliente e cada assunto (`rotinas/novo-cliente.md`). A pasta
fica **no computador** e pode estar sincronizada com o Google Drive, o OneDrive ou o
Dropbox. O nome é escolhido pelo advogado, por exemplo "Escritório IA".

## Como fica a pasta

```
<Pasta escolhida pelo advogado>/
  AGENTS.md, CLAUDE.md, GEMINI.md   ponteiros para o método (ver raiz/)
  _escritorio/
    configuracao      onde ficam as coisas, formato, acesso de cada assistente
    perfil            quem é o advogado, como escreve e entrega
    formatacao        como os documentos devem ficar: fonte, numeração, assinaturas
    posicoes          posições em cada cláusula, por lado
    clientes          índice de clientes e contrapartes (checagem de conflito)
    datas-chave       datas dos contratos
    referencias       referências legais conferidas
    modelos/          modelos e cláusulas do próprio advogado, com o índice de quando usar
  clientes/
    <cliente>/
      cliente         dados do cliente, quem assina, canal preferido
      <AAAA-MM_assunto-curto>/
        ficha         estado atual do assunto, versões, próximo passo
        historico     registro do que foi feito, por quê, a pedido de quem
        01_documentos/  originais recebidos: contrato social, e-mails, conversas
        02_versoes/     v01, v02… do contrato (nunca sobrescritos)
        03_entregas/    revisões, comparações, resumos
  _legado/            opcional: material anterior ao método, só leitura
```

As subpastas do assunto são numeradas para aparecerem na ordem do trabalho, em qualquer
aplicativo: o que chegou, as versões, o que sai.

**Assuntos criados antes da versão 0.5** podem ter nomes no padrão antigo
(`AAAA-MM-tipo-contraparte`) e subpastas sem número (`documentos/`, `versoes/`,
`entregas/`). O assistente usa as pastas que existirem e não renomeia nada sem perguntar.

## Nomes de pastas e arquivos

**Pasta do assunto:** `AAAA-MM_assunto-curto`, por exemplo `2026-10_saas-gestao-estoque`.
- O assunto descreve o objeto do contrato de forma **neutra**: `prestacao-servicos-ti`,
  nunca `divorcio-joao` ou o nome da contraparte.
- Contraparte, valores e motivos ficam na `ficha` e no índice `_escritorio/clientes`.

**Versões do contrato (`02_versoes/`):** `vNN-AAAA-MM-DD-origem.ext`, por exemplo
`v02-2026-10-14-contraparte.docx`. Origem: `nossa`, `contraparte`, `cliente` ou
`assinada`. Detalhes na `ficha`.

**Documentos recebidos (`01_documentos/`):** `AAAA-MM-DD_tipo_descritor.ext`, por exemplo
`2026-10-12_email_proposta-prazo-entrega.eml`.
- **Data:** a do documento (assinatura, envio, emissão), não a do download. Data
  desconhecida: `sem-data_tipo_descritor.ext`. Nunca invente uma data.
- **Tipo**, de uma lista curta: `contrato`, `minuta`, `aditivo`, `ata`, `parecer`,
  `notificacao`, `procuracao`, `email`, `conversa`, `comprovante`, `certidao`, `planilha`,
  `apresentacao`, `outro`.
- **Descritor:** curto, com hífens entre as palavras.

**Entregas (`03_entregas/`):** `AAAA-MM-DD-tipo`, por exemplo `2026-10-15-revisao-v02.md`.
Cada rotina indica o nome.

**Regras para todos os nomes:**
- Letras minúsculas, sem acento, cedilha ou espaço.
- **Nada sensível no nome:** CPF, CNPJ, valores de acordo, motivos, fatos íntimos. Nomes
  aparecem em links compartilhados, e-mails, registros de sincronização e conversas com a
  IA.
- Nunca `final`, `novo` ou `revisado` no nome: a pasta e o número da versão dizem isso.
- Um documento, um arquivo. Prefira PDF com texto pesquisável a fotos soltas.
- Caminho completo com menos de 255 caracteres.
- Esses padrões valem para os arquivos que o assistente cria. Arquivos que o advogado já
  salvou com outro nome só são renomeados se ele aprovar.

## Quem já tem pastas de clientes

Duas opções. O advogado escolhe na configuração ou no primeiro cliente:

1. **Adaptar no lugar** (padrão). O assistente cria os registros ao lado dos arquivos
   existentes, aponta para eles na `ficha` e não move nada sem perguntar.
2. **Data de corte.** A partir de uma data, tudo o que é novo segue o método. O material
   antigo vai, pelo próprio advogado ou com o OK dele, para `_legado/`, e ali fica intacto.
   - Quando um assunto antigo for reaberto, o assistente **copia** (não move) os arquivos
     dele para a estrutura nova, cria a `ficha` e registra no `historico` os nomes
     originais dos arquivos renomeados.
   - Antes de qualquer renomeação em lote: cópia de segurança. Duplicados não são
     apagados sem conferir.

## Formato dos arquivos

**Registros** (`configuracao`, `perfil`, `formatacao`, `posicoes`, `clientes`, `datas-chave`,
`referencias`, `cliente`, `ficha` e `historico`): sempre **`.md`**.
- Texto simples: qualquer assistente lê e edita direto na pasta, e é barato ler inteiro.
- O Google Drive, o OneDrive e o Dropbox guardam e sincronizam `.md` como qualquer
  arquivo, e os conectores de nuvem leem `.md`.

**Contratos e entregas:** o que o advogado usa no dia a dia, normalmente `.docx` ou `.pdf`.
O assistente do computador grava o `.docx` exato na pasta, com controle de alterações, e a
sincronização leva para a nuvem.

**Não use Google Docs nativo** (nem para registros, nem para contratos). No computador, o
app do Google Drive mostra esses arquivos só como atalhos (`.gdoc`), e o assistente não
consegue ler nem editar.

**Pastas configuradas antes da versão 0.7 com registros em Google Docs.** O assistente
continua usando o que existe e oferece converter: lê cada registro pelo conector do Google
Drive (no computador, o atalho `.gdoc` não tem o conteúdo), grava o `.md` ao lado e deixa o
Google Doc intacto. Só depois do OK do advogado o Google Doc
vai para `_legado/`, e nada é apagado.

## Arquivos desta pasta

| Arquivo | Vira |
|---|---|
| `raiz/AGENTS.md`, `raiz/CLAUDE.md`, `raiz/GEMINI.md` | Ponteiros na raiz da pasta do advogado |
| `_escritorio/*` | `_escritorio/` do advogado |
| `cliente/cliente.md` | `clientes/<cliente>/cliente` |
| `assunto/ficha.md`, `assunto/historico.md` | `clientes/<cliente>/<assunto>/ficha` e `historico` |

Linhas em itálico que começam com `_exemplo_` são ilustração. Não as copie para a pasta do
advogado, ou apague-as no primeiro registro real.
