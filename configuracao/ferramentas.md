# Como configurar cada assistente

> Informações conferidas em 2026-10-01. Os aplicativos mudam com frequência: o que
> estiver marcado `[testar]` ainda não foi verificado na prática.

## 1. Comece (em qualquer assistente)

Abra uma conversa nova e escreva:

> Leia https://raw.githubusercontent.com/capi-legal/metodo-advogados/main/AGENTS.md e vamos configurar.

Um endereço escrito na conversa é aberto por todos os assistentes. O assistente faz 6
perguntas, monta ou adota a sua pasta de trabalho e entrega o **bloco de configuração**.

## 2. Cole o bloco nas configurações

Onde colar em cada assistente, limites e cuidados: `configuracao/bloco-de-configuracao.md`.
Faça isso em cada assistente que você usa. O bloco é o mesmo para todos, e todos passam a
trabalhar na mesma pasta.

## 3. Como o assistente chega à sua pasta

### A. No computador (experiência completa, recomendada)

O assistente lê e grava direto na pasta. Para pastas na nuvem, use o app de
sincronização (Google Drive para computador, OneDrive, Dropbox) e deixe a pasta
**baixada no computador**:
- Drive: modo "espelhar", ou "disponível off-line";
- OneDrive: "Sempre manter neste dispositivo".

| Assistente | Como abrir a pasta | Encontra o método sozinho? |
|---|---|---|
| **Claude** (app para computador, Cowork) | Escolha a pasta de trabalho, não a raiz do Drive | Pelo `CLAUDE.md` da pasta `[testar]` |
| **ChatGPT** (app para computador, Work) | Projeto local com a pasta como principal | `[testar]`. O bloco nas instruções garante o essencial |
| **Codex** (OpenAI) | Abra na pasta | Sim, pelo `AGENTS.md` da pasta (testado) |
| **Claude Code / Gemini CLI** | No terminal, na pasta: `claude` ou `gemini` | Sim (`CLAUDE.md` / `GEMINI.md`) |

A configuração cria esses ponteiros (`AGENTS.md`, `CLAUDE.md`, `GEMINI.md`) na raiz da
sua pasta.

**Contratos em `.docx` ou `.pdf`.** Google Docs nativo aparece no computador só como um
atalho, e o assistente não consegue ler o conteúdo.

### B. Na web ou no celular (por conector)

O assistente acessa a pasta pelo conector de armazenamento. O que cada um consegue fazer
varia:

| | Google Drive | Dropbox | OneDrive pessoal | OneDrive / SharePoint da empresa |
|---|---|---|---|---|
| **ChatGPT** | Lê, cria e edita onde autorizado (planos pagos, web) | Lê e grava | Só para anexar arquivos | Lê e grava, se o administrador liberar |
| **Claude** | Lê e cria arquivos; editar não está documentado | Cria arquivos de texto | Não suportado | Lê e grava, com autorização do administrador |
| **Gemini** | Lê; edita Documentos e Planilhas pelo Spark (planos Pro/Ultra) | Pelo Spark | Não suportado | Não suportado |
| **Grok** | Lê e cria em qualquer pasta | `[testar]` | Não suportado | Envia arquivos |

**OneDrive pessoal não pode receber gravações por conector em nenhum assistente.** Use o
modo computador (A).

Quando o assistente não puder editar um arquivo, ele cria um arquivo novo, ou entrega o
texto para você colar (`AGENTS.md` §10).

Para quem trabalha **só** na web ou no celular com Google Drive, os registros podem ser
Google Docs. A regra está em `estrutura/LEIA-ME.md`.

## 4. Sigilo e plano

- Os arquivos que o assistente lê são **enviados ao fornecedor da IA** para
  processamento. Estar na sua pasta não significa ficar só no computador.
- Use **plano pago com o uso dos dados para treinamento desativado**, ou plano
  empresarial. Evite planos gratuitos para trabalho de clientes.
- **Memória do assistente:** ela vale para todas as conversas, e o bloco já proíbe guardar
  nela fatos de clientes. Para mais segurança, desligue "consultar conversas anteriores"
  (ChatGPT) ou "pesquisar e consultar conversas" (Claude).
- Envie só o necessário e, quando não fizer diferença, troque nomes por iniciais.
