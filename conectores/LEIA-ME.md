# Conectores

Integrações opcionais. **Nada aqui é obrigatório.** Sem conector, a pasta funciona com os
arquivos que você coloca nela.

Os conectores são descritos pelo que fazem, não pelo nome técnico, porque o nome muda
conforme a ferramenta. O assistente descobre na hora quais estão disponíveis.

| Capacidade | Exemplos | Para que serve aqui | Cuidados |
|---|---|---|---|
| **Armazenamento** | Google Drive, OneDrive, SharePoint, Dropbox | Abrir os contratos onde já estão | Ver abaixo: sincronizar é melhor que conectar |
| **E-mail** | Gmail, Outlook | Achar a última versão enviada pela contraparte; trazer o contexto de um cliente | Buscar **só** pelo cliente ou assunto ativo. Nunca varrer a caixa inteira. Não enviar nada sem confirmação |
| **Assinatura eletrônica** | Clicksign, D4Sign, ZapSign, DocuSign, gov.br | Status da assinatura; preparar envelope | **Nunca** enviar para assinatura sem um "sim" para aquele envio. Antes, conferir partes, poderes e anexos |
| **Agenda** | Google Agenda, Outlook | Lembretes das datas de `datas-chave.md` | Criar evento só com confirmação |
| **Capi** | Conector Capi | Pedir revisão de outro advogado | Ver `capi.md` |

## Drive e OneDrive: sincronizar é melhor que conectar

**Melhor opção: o app de sincronização** (Google Drive para computador, ou OneDrive). A
pasta aparece no computador e qualquer assistente lê e grava normalmente. Para funcionar
bem:

- Os arquivos precisam estar **baixados no computador**:
  - Google Drive: modo "espelhar", ou "disponível off-line" na pasta;
  - OneDrive: "Sempre manter neste dispositivo".
- Contratos em **.docx ou .pdf**. Google Docs nativo aparece no computador só como um
  atalho, e o assistente não consegue ler o conteúdo.
- Abra no assistente **a pasta do escritório**, não a raiz do Drive.

**Conector de nuvem (sem sincronizar)**, usado pelas versões web dos assistentes:

- costuma **ler** e **criar** arquivos;
- muitas vezes **não edita** arquivos existentes.

Nesse caso, o assistente segue o modo sem edição (`AGENTS.md` §10). O conector do
Microsoft 365 costuma exigir conta corporativa e autorização do administrador.

## Sem conector

Coloque o arquivo na pasta do assunto (em `02_versoes/` ou `01_documentos/`), ou cole o texto
na conversa.

Conversas de WhatsApp: no celular, use "Exportar conversa" (sem mídia) e salve o .txt em
`01_documentos/`. O assistente lê a conversa e atualiza a `ficha.md`.
