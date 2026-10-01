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
      <AAAA-MM-tipo-contraparte>/
        ficha         estado atual do assunto, versões, próximo passo
        historico     registro do que foi feito, por quê, a pedido de quem
        versoes/      v01, v02… (nunca sobrescritos)
        documentos/   originais recebidos: contrato social, e-mails, conversas
        entregas/     revisões, comparações, resumos
```

Se o advogado já tem pastas de clientes, a estrutura se adapta a elas: o assistente cria
os registros ao lado dos arquivos existentes, sem mover nada sem perguntar.

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
