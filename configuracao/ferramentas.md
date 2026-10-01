# Como usar esta pasta em cada assistente

A pasta funciona com qualquer assistente de IA que trabalhe com arquivos. Há dois jeitos:

- **A. O assistente trabalha na pasta do computador.** É a experiência completa: lê,
  cria e atualiza os arquivos sozinho.
- **B. O assistente está na web.** Projeto com instruções e arquivos anexados, ou conector
  de Drive. Funciona, mas com mais passos manuais.

**Primeira mensagem em qualquer assistente:** "Leia o AGENTS.md e vamos configurar."

Se o assistente não mencionar o seu perfil na primeira resposta, ele não leu as
instruções. Repita a frase.

---

## A. Na pasta do computador

| Assistente | Como abrir | Lê as instruções sozinho? |
|---|---|---|
| **Claude, app para computador (Cowork)** | Escolha esta pasta como pasta de trabalho | Normalmente sim (`CLAUDE.md` → `AGENTS.md`) `[testar]` |
| **Claude Code** (terminal) | `cd` até a pasta e rode `claude` | Sim (`CLAUDE.md` → `AGENTS.md`) |
| **ChatGPT, app para computador (Work)** | Crie um projeto local com esta pasta como principal | `[testar]`. Se não ler, cole `instrucoes-curtas.md` nas instruções do projeto |
| **Codex** (OpenAI) | Abra na pasta | Sim (`AGENTS.md`) |
| **Gemini CLI** (Google) | `cd` até a pasta e rode `gemini` | Sim (`GEMINI.md` → `AGENTS.md`) |
| **Outros** (Cursor e similares) | Abra a pasta | Quase todos leem `AGENTS.md`. Se não, peça na primeira mensagem |

## B. Na web (ChatGPT, Claude, Gemini, Grok…)

1. Crie um **projeto** ou espaço com instruções personalizadas. O nome muda conforme o
   assistente: Projeto, Gem, Workspace.
   - Para sigilo, use **um projeto por cliente**, ou pelo menos um projeto só para
     trabalho de clientes.
2. Cole o conteúdo de `configuracao/instrucoes-curtas.md` no campo de instruções.
3. Anexe ao projeto:
   - `_escritorio/perfil.md`;
   - `_escritorio/posicoes.md`;
   - `guias/pontos-gerais.md`;
   - as rotinas que mais usa (por exemplo `rotinas/revisar-contrato.md`).
4. Para cada assunto, anexe a `ficha.md`, o `historico.md` e o contrato.
5. **O assistente na web não grava na sua pasta.** Ele entrega o texto; você salva o
   arquivo. Com conector de Drive, ele pode criar arquivos novos, mas talvez não edite os
   existentes (`AGENTS.md` §10).
6. Atualize os anexos do projeto quando o perfil ou as posições mudarem.

## Pasta no Google Drive ou no OneDrive

Funciona bem se você usar o app de sincronização e:

- deixar os arquivos **baixados no computador**:
  - Drive: modo "espelhar", ou "disponível off-line";
  - OneDrive: "Sempre manter neste dispositivo";
- usar **.docx/.pdf**, não Google Docs nativo;
- abrir no assistente **a pasta do escritório**, não a raiz do Drive.

Detalhes em `conectores/LEIA-ME.md`.

## Sigilo e plano

- Os arquivos que o assistente lê são **enviados ao fornecedor da IA** para processamento.
  Ficar na pasta não significa ficar só no computador.
- Use um **plano pago com o uso dos dados para treinamento desativado** (ou plano
  empresarial). Evite planos gratuitos para trabalho de clientes.
- Envie só o necessário. Quando não fizer diferença, troque nomes por iniciais.
- Se você usa o termo de uso de IA com clientes, respeite as recusas. O assistente avisa
  se o cliente recusou.
