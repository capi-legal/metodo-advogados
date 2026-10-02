# Estrutura da pasta do advogado

Arquivos em branco que o assistente usa para criar a pasta de trabalho do advogado
(`rotinas/configurar.md`), cada cliente e cada assunto (`rotinas/novo-cliente.md`). A pasta
pode ficar no Google Drive, no OneDrive, no Dropbox ou no computador. O nome é escolhido
pelo advogado, por exemplo "Escritório IA".

## Como fica a pasta

```
<Pasta escolhida pelo advogado>/
  AGENTS.md, CLAUDE.md, GEMINI.md   ponteiros para o método (só quando um assistente de
                                    computador trabalha na pasta; ver raiz/)
  _escritorio/
    configuracao      onde ficam as coisas, formato, acesso de cada assistente
    perfil            quem é o advogado, como escreve e entrega
    posicoes          posições em cada cláusula, por lado
    clientes          índice de clientes e contrapartes (checagem de conflito)
    datas-chave       datas dos contratos
    referencias       referências legais conferidas
    modelos/          modelos e cláusulas do próprio advogado
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

## Formato dos registros: `.md` ou Google Docs

Os registros são `configuracao`, `perfil`, `posicoes`, `clientes`, `datas-chave`,
`referencias`, `cliente`, `ficha` e `historico`. Eles têm **um formato por pasta**,
definido na configuração:

| Situação do advogado | Formato | Por quê |
|---|---|---|
| Usa um assistente **no computador** sobre a pasta (Claude Cowork, ChatGPT para computador, Codex) | **`.md`** | Google Docs nativo aparece no computador só como atalho; o assistente não consegue ler nem editar |
| Usa **só** assistentes na web ou no celular, com a pasta no **Google Drive** | **Google Docs** | Os conectores de Drive leem bem e, em alguns assistentes, editam Google Docs. Para o advogado, parece um documento comum |
| Usa os dois sobre a mesma pasta | **`.md`** | O assistente do computador precisa ler tudo; na web, os `.md` são lidos pelo conector |
| Pasta no OneDrive, Dropbox ou só no computador | **`.md`** | |

Os modelos desta pasta estão em `.md`. No formato Google Docs, o assistente cria um
documento com o mesmo nome (sem extensão) e o mesmo conteúdo.

**Contratos e entregas** seguem o que o advogado usa no dia a dia, normalmente `.docx` ou
`.pdf`. Quem trabalha com assistente no computador não deve usar Google Docs nativo para
contratos: o assistente não consegue lê-los.

## Arquivos desta pasta

| Arquivo | Vira |
|---|---|
| `raiz/AGENTS.md`, `raiz/CLAUDE.md`, `raiz/GEMINI.md` | Ponteiros na raiz da pasta do advogado (só no modo computador) |
| `_escritorio/*` | `_escritorio/` do advogado |
| `cliente/cliente.md` | `clientes/<cliente>/cliente` |
| `assunto/ficha.md`, `assunto/historico.md` | `clientes/<cliente>/<assunto>/ficha` e `historico` |

Linhas em itálico que começam com `_exemplo_` são ilustração. Não as copie para a pasta do
advogado, ou apague-as no primeiro registro real.
