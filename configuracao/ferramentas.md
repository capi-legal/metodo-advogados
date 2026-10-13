# Como configurar cada assistente

> Informações conferidas em 2026-10-12. Os aplicativos mudam com frequência: o que
> estiver marcado `[testar]` ainda não foi verificado na prática.

## 1. Comece (em qualquer assistente)

Copie o texto de `prompt-de-configuracao.md`, que está na página do método, e cole numa
conversa nova **num assistente no computador**, com acesso a pastas (seção 3A). Pela web
ou pelo celular a configuração não começa: o assistente diz qual app abrir.

O prompt funciona mesmo em assistentes que não abrem links (por exemplo, o Gemini), porque
traz o essencial no próprio texto. O assistente:
- confere se a conversa alcança a sua pasta no computador; se não alcançar, diz onde
  clicar e pede para reabrir a conversa;
- explica o que vai fazer;
- faz 5 perguntas;
- monta ou adota a sua pasta de trabalho;
- guarda na memória dele onde ela fica;
- entrega o **bloco de configuração**.

## 2. Cole o bloco nas configurações

Onde colar em cada assistente, limites e cuidados: `configuracao/bloco-de-configuracao.md`.
Faça isso em cada assistente que você usa. O bloco é o mesmo para todos, e todos passam a
trabalhar na mesma pasta.

## 3. Como o assistente chega à sua pasta

**A pasta fica no computador. É obrigatório.** Uma pasta comum basta. A nuvem é
opcional: se você já usa, o app de sincronização mantém a mesma pasta no computador e na
nuvem, e o conector dá acesso extra pela web e pelo celular.

Por que assim: só o assistente do computador grava qualquer arquivo exato na pasta,
inclusive o `.docx` recebido e o redline com controle de alterações. Pelos conectores, os
assistentes leem bem, mas em geral não conseguem salvar um `.docx` nem editar um arquivo
que já existe.

### A. No computador (obrigatório)

O assistente lê, cria e edita direto na pasta.

| Assistente | Como abrir a pasta | Encontra o método sozinho? |
|---|---|---|
| **Claude** (app para computador: Cowork, ou conversa com a pasta adicionada pelo "+") | Escolha a pasta de trabalho, não a raiz do Drive | Pelo `CLAUDE.md` da pasta `[testar]` |
| **ChatGPT** (app para computador, Work) | Projeto local com a pasta como principal | `[testar]`. O bloco nas instruções garante o essencial |
| **Codex** (OpenAI) | Abra na pasta | Sim, pelo `AGENTS.md` da pasta (testado) |
| **Claude Code / Gemini CLI** | No terminal, na pasta: `claude` ou `gemini` | Sim (`CLAUDE.md` / `GEMINI.md`) |

A configuração cria esses ponteiros (`AGENTS.md`, `CLAUDE.md`, `GEMINI.md`) na raiz da
sua pasta.

### Se a pasta estiver sincronizada com a nuvem (opcional)

No app da sua nuvem, deixe a pasta **baixada no computador**. Se o
arquivo estiver só na nuvem, alguns apps não conseguem abri-lo.

| Nuvem | App | Deixar baixado | Onde aparece no Mac |
|---|---|---|---|
| **Google Drive** | Google Drive para computador | Modo "espelhar arquivos", ou "disponível off-line" na pasta | Finder → Locais → Google Drive (`~/Library/CloudStorage`) |
| **OneDrive** | OneDrive | Botão direito na pasta → "Sempre manter neste dispositivo" | Finder → Locais → OneDrive (`~/Library/CloudStorage`) |
| **Dropbox** | Dropbox | Botão direito na pasta → "Disponibilizar off-line" | Finder → Locais → Dropbox (`~/Library/CloudStorage`) |

No Windows, cada uma aparece como pasta no Explorador de Arquivos, com as mesmas opções.

As três nuvens guardam e sincronizam `.md`, `.docx` e `.pdf` sem problema. Cuidados que
valem para todas:
- **Não use Google Docs nativo**, nem para registros nem para contratos: no computador ele
  aparece só como atalho (`.gdoc`), e o assistente não lê.
- **Sincronizar não é backup.** Apagar de um lado apaga do outro. Quem protege os arquivos
  é a lixeira e o histórico de versões da nuvem, e a regra do método de nunca apagar nem
  sobrescrever.
- **Mesmo arquivo editado em dois lugares ao mesmo tempo** (computador e celular) pode
  gerar uma "cópia em conflito". O assistente não apaga nenhuma das duas: mostra a
  diferença e pergunta.
- Se o Mac pedir permissão para o app do assistente acessar a pasta da nuvem, aceite.

### B. Na web ou no celular (acesso extra, por conector)

Com a pasta sincronizada, você também chega a ela pelo conector da mesma nuvem. É um
acesso **limitado**: o assistente lê tudo, mas normalmente só **cria** arquivos de texto
novos. Ele segue `AGENTS.md` §10: registros em arquivos novos com data, que o assistente
do computador consolida depois, e contratos `.docx` salvos por você.

| | Google Drive | Dropbox | OneDrive pessoal | OneDrive / SharePoint da empresa |
|---|---|---|---|---|
| **ChatGPT** | Lê, cria e edita onde autorizado (planos pagos, web) | Lê; cria, copia e move arquivos; `.docx` `[testar]` | Só para anexar arquivos | Lê e grava, se o administrador liberar |
| **Claude** | Lê tudo; cria `.md` e Google Docs; não edita `.md` nem salva `.docx` (testado) | Lê; salva texto gerado; editar e `.docx` `[testar]` | Não suportado (só contas de trabalho) | Lê; cria e atualiza arquivos só se o administrador ligar as ferramentas de escrita |
| **Gemini** | Lê; edita Documentos e Planilhas pelo Spark (planos Pro/Ultra) | Pelo Spark | Não suportado | Não suportado |
| **Grok** | Lê e cria em qualquer pasta | `[testar]` | Não suportado | Envia arquivos |

**OneDrive pessoal não tem conector útil em nenhum assistente.** Funciona normalmente no
computador (A), mas sem acesso extra pela web ou pelo celular.

## 4. Sigilo e plano

- Os arquivos que o assistente lê são **enviados ao fornecedor da IA** para
  processamento. Estar na sua pasta não significa ficar só no computador.
- Use **plano pago com o uso dos dados para treinamento desativado**, ou plano
  empresarial. Evite planos gratuitos para trabalho de clientes.
- **Memória do assistente:** ela vale para todas as conversas, e o bloco já proíbe guardar
  nela fatos de clientes. Para mais segurança, desligue "consultar conversas anteriores"
  (ChatGPT) ou "pesquisar e consultar conversas" (Claude).
- Envie só o necessário e, quando não fizer diferença, troque nomes por iniciais.
