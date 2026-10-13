# Conectores

Integrações opcionais. **Nada aqui é obrigatório.** Sem conector, a pasta funciona com os
arquivos que você coloca nela.

Os conectores são descritos pelo que fazem, não pelo nome técnico, porque o nome muda
conforme a ferramenta. O assistente descobre na hora quais estão disponíveis.

| Capacidade | Exemplos | Para que serve aqui | Cuidados |
|---|---|---|---|
| **Armazenamento** | Google Drive, OneDrive, SharePoint, Dropbox | Acesso extra à pasta pela web e pelo celular | Ver abaixo: a pasta fica no computador; o conector é complemento |
| **E-mail** | Gmail, Outlook | Achar a última versão enviada pela contraparte; trazer o contexto de um cliente | Buscar **só** pelo cliente ou assunto ativo. Nunca varrer a caixa inteira. Não enviar nada sem confirmação |
| **Assinatura eletrônica** | Clicksign, D4Sign, ZapSign, DocuSign, gov.br | Status da assinatura; preparar envelope | **Nunca** enviar para assinatura sem um "sim" para aquele envio. Antes, conferir partes, poderes e anexos |
| **Agenda** | Google Agenda, Outlook | Lembretes das datas de `datas-chave.md` | Criar evento só com confirmação |
| **Capi** | Conector Capi | Pedir revisão de outro advogado | Ver `capi.md` |

## Armazenamento: a pasta fica no computador

A pasta de trabalho fica **no computador**, aberta no assistente. Para tê-la também na
nuvem, use o app de sincronização (Google Drive para computador, OneDrive ou Dropbox) e
deixe os arquivos baixados. Detalhes e cuidados em `configuracao/ferramentas.md`, seção 3.

O **conector de nuvem** é um acesso extra à mesma pasta, pela web ou pelo celular:
- **lê** bem, inclusive `.docx` e `.pdf`;
- costuma só **criar** arquivos de texto novos, sem editar os que existem;
- em geral **não salva `.docx`**: o arquivo precisaria ser enviado como texto dentro da
  chamada, e um caractere errado corrompe o documento.

Por isso, pelo conector o assistente segue `AGENTS.md` §10. O conector do Microsoft 365
exige conta de trabalho, e a gravação depende do administrador. OneDrive pessoal não tem
conector útil.

## Sem conector

Coloque o arquivo na pasta do assunto (em `02_versoes/` ou `01_documentos/`), ou cole o texto
na conversa.

Conversas de WhatsApp: no celular, use "Exportar conversa" (sem mídia) e salve o .txt em
`01_documentos/`. O assistente lê a conversa e atualiza a `ficha.md`.
