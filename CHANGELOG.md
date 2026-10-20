# Mudanças no método

O assistente informa a versão em uso (topo do `AGENTS.md`). Mudanças que alteram o
comportamento ficam registradas aqui, a mais recente primeiro.

## 0.9 · 2026-10-20

Modelos do próprio advogado, a partir do trabalho dele, sem expor o cliente de origem.

- **"Salve isto como modelo."** Nova rotina `rotinas/salvar-modelo.md`. O assistente
  combina o tipo de documento, o lado e quando usar (e não usar) o modelo; tira nomes,
  documentos, valores, detalhes do negócio e os dados escondidos no arquivo (autor,
  comentários, alterações controladas); pergunta o que fazer com as concessões daquela
  negociação; e mostra o modelo limpo, como prévia na pasta do assunto, com o relatório do
  que saiu. Só grava em `_escritorio/modelos/` depois do "sim". O relatório cita dados do
  cliente e por isso fica só na conversa.
- **Índice dos modelos.** Novo `_escritorio/modelos/indice.md`: arquivo, tipo, lado, quando
  usar, quando não usar e origem anonimizada. Pastas já configuradas ganham o índice no
  primeiro modelo salvo.
- **Aviso de uso.** Ao redigir e nos documentos de início, o assistente procura no índice o
  modelo do tipo e do lado e **sempre diz qual vai usar**, antes de redigir e na entrega
  (`AGENTS.md` §7). Sem modelo para o tipo, ele oferece uma vez salvar a minuta aprovada
  como modelo.
- **Modelos nunca por cima.** Modelo atualizado é arquivo novo com a data; o índice diz qual
  é o atual. Substitui a regra antiga de "salvar por cima se a versão antiga não importar".
- **Campos dos modelos:** `[preencher: …]`, como nas minutas, no lugar de `[•]`.
- **Sigilo:** os modelos ficam só na pasta do advogado; o conector da Capi não tem acesso
  a ela (`conectores/capi.md`). O README apresenta o recurso, e o bloco de configuração
  ganhou uma linha sobre modelos (cerca de 4.200 caracteres).

## 0.8 · 2026-10-13

Ajustes do teste da configuração ao vivo (2026-10-13).

- **Sem a pergunta de canal e tom.** A antiga pergunta 4 saiu inteira. O campo "Tom" saiu
  do `perfil`; o canal com o cliente fica `[padrão]` e é aprendido com o uso. No bloco de
  configuração, a linha "Tom" do resumo do método, que falava da postura do assistente,
  passou a se chamar "Postura".
- **Formatação dos documentos.** Nova pergunta 4: como os contratos devem ficar. O melhor
  caminho é um documento de que o advogado gosta: o assistente lê só a forma, escreve as
  regras em texto simples (fonte, tamanho, numeração, estrutura, como um quadro de termos
  no início), mostra uma página de amostra e grava as regras depois do "sim". O conteúdo
  não vai para `_escritorio`. Uma cópia do arquivo é opcional e só completa o que o texto
  não descreve (logo, quadros). Sem documento, há 3 opções prontas
  (Clássico, Moderno e Compacto). A resposta vai para o novo `_escritorio/formatacao.md`,
  e todo documento criado segue esse arquivo (`AGENTS.md` §7). O que se registra e como
  aplicar está em `modelos/formatacao.md`. Mesmo sem nada registrado: papel A4 e números das
  cláusulas escritos no texto, que não somem em nenhum visualizador.
- **Pergunta 5: "O que a Capi deve sempre saber sobre você para te atender melhor?"**
  Substitui "o que você repete a cada conversa", com exemplos de formatação, idioma,
  tarefas que se repetem e regras para outros conectores. Dá para pular: depois, "adicione
  à minha memória da Capi: …" grava em `_escritorio/perfil`, "Sempre que trabalhar para
  mim", e nunca na memória do assistente (`AGENTS.md` §9).
- **Redação com pedido curto.** Antes de redigir, o assistente confere o básico: partes,
  lei aplicável e foro, idioma e prazo. Se faltar, ele pergunta se o advogado prefere
  responder agora ou ver primeiro um esqueleto. Respondendo agora, as perguntas vêm em
  rodadas de no máximo 3 por mensagem (o limite de antes continua), até a minuta poder
  sair sem lacunas. No esqueleto, tudo o que falta abre a entrega, em "Em aberto", como
  perguntas. Se o pedido já traz o básico, nada é perguntado de novo.
- **Texto para as configurações do app, explicado.** O passo 5 da configuração passa a
  ser opcional e é explicado em linguagem simples antes do bloco: o que ele faz, que vale
  também em conversas não jurídicas e como tirar, o que acontece sem ele (a Capi funciona
  com a pasta aberta na conversa), onde colar, em passos numerados, e que dá para decidir
  depois. O mesmo texto está no início de `configuracao/bloco-de-configuracao.md`. Caminho
  no Claude: Configurações → "Instruções para o Claude".
- Configuração: continuam 5 perguntas no total (a pasta e mais 4), cerca de 3 minutos.

## 0.7.1 · 2026-10-13

- **Pergunta 2: "Em quais destas áreas você se sente mais forte?"** Uma lista só, por
  ramo do direito, porque é o ramo que define o risco do contrato: 10 áreas, mais
  "outra". Tipos de documento (NDA, contratação de PJ) entram como exemplos da área a que
  pertencem. Não se pergunta mais o que fica de fora nem onde a pessoa é mais fraca: as
  opções não marcadas vão para "Onde posso precisar de apoio" no `perfil`, e é nelas que
  o assistente pode sugerir a Capi (`AGENTS.md` §8). As marcadas vão para "Onde me sinto
  mais forte", que substitui "Contratos que mais passam pela minha mesa", "Outras áreas
  que atendo" e "Áreas que não atendo".
- **Opções numeradas** em todas as perguntas da configuração, uma por linha e sem
  marcadores, para a pessoa responder só com os números ("1, 3, 10"). Na pergunta 4,
  canal (1 a 3) e tom (4 a 6) têm números diferentes.

## 0.7 · 2026-10-12

A pasta de trabalho fica no computador, sempre. Mudança feita depois de um teste com o
conector do Google Drive: os registros funcionaram, mas o contrato recebido (v01) e o
redline em `.docx` não puderam ser salvos na pasta.

- **Pasta no computador obrigatória.** A configuração só acontece num assistente no
  computador, com a pasta aberta (Claude, ChatGPT para computador, Codex, Claude Code,
  Gemini CLI). Pela web ou pelo celular, o assistente diz qual app abrir e para.
- **Nuvem opcional.** A pergunta 1 passa a ser "em qual pasta do computador vamos
  trabalhar?". Uma pasta comum basta. A sincronização com Google Drive, OneDrive ou
  Dropbox é mencionada uma vez, sem insistir, porque dá acesso pela web e pelo celular.
  Pasta já sincronizada: o assistente explica como deixar os arquivos baixados
  (`configuracao/ferramentas.md`).
- **Conector vira acesso extra.** Na web ou no celular, sobre a mesma pasta, o assistente
  lê tudo e registra em arquivos novos com data (`AGENTS.md` §10). Um assistente da web
  pode ser ligado a uma pasta já configurada.
- **Arquivos `.docx` pelo conector:** o assistente avisa no início da tarefa que não
  consegue salvá-los, pede ao advogado que salve o contrato recebido em `02_versoes/`
  antes de ler e entrega o que produzir com o caminho exato (`AGENTS.md` §10).
- **Registros sempre em `.md`.** Google Docs deixa de ser formato de registro e não deve
  ser usado para contratos. Pastas antigas em Google Docs continuam funcionando, e o
  assistente oferece converter sem apagar nada (`estrutura/LEIA-ME.md`).
- **`_escritorio/configuracao`:** caminho no computador, nuvem que sincroniza, se os
  arquivos estão baixados e link da pasta na nuvem.
- Mantido da 0.6.1 (não publicada): a pergunta 1 mostra de uma vez o "para quê", as
  opções e como dar acesso no app em uso; se a pessoa diz que já adicionou a pasta, o
  assistente confere.

Ajustes do teste da configuração pelo conector da Capi (Claude Desktop, 2026-10-09):

- **Sem arquivo de teste.** O teste de criar e editar usa o próprio
  `_escritorio/configuracao`; antes ficava um `teste-acesso` na pasta.
- **A estrutura completa.** A configuração cria também `datas-chave`, `referencias` e
  `modelos/`, que o `AGENTS.md` já usa.
- **Outras áreas.** A pergunta 2 continua igual (contratos e áreas fora do trabalho).
  "Outras áreas que atendo", no `perfil`, fica `[preencher]` e é aprendida com o uso, para
  manter a configuração curta.
- **Onde colar o bloco:** o caminho no Claude e no ChatGPT.
- **Fechamento:** lista o que foi criado, inclusive os ponteiros na raiz, e sugere como
  teste uma pergunta sobre contrato. "Onde ficam meus arquivos?" é respondida pelo perfil e
  não mostra se o método está sendo seguido.
- **Conector da Capi:** com ele ligado, a configuração vem do conector
  (`rotinas/configurar.md`). No trabalho do dia a dia o assistente segue o método da pasta;
  a Capi entra no fim, para sugerir a revisão por um advogado (§8). Endereço do conector em
  `conectores/capi.md`.

## 0.6 · 2026-10-09

Configuração refeita depois do teste com uma pasta no computador.

- **O lugar certo vem primeiro.** O assistente diz em qual app e modo está, explica que
  precisa de uma pasta (modo de trabalho no computador ou conector de nuvem) e pergunta
  onde ficam os arquivos antes de tudo. Testa ler, criar e editar ali mesmo.
- **Sem acesso, a configuração para.** O assistente mostra os cliques do próprio app
  (Claude, ChatGPT, Codex e outros) e recomenda reabrir a conversa no lugar certo. Não
  prepara arquivos nem pacotes para copiar depois.
- **Perguntas novas:** quem é o usuário (advogado interno, de escritório, autônomo,
  fundador ou sócio, outra função) e o que ele repete a cada conversa, que vira a seção
  "Sempre que trabalhar para mim" do `perfil` e a seção "Minhas regras" do bloco.
- **Perguntas retiradas:** o lado do cliente (fica `[padrão: varia]`, confirmado em cada
  assunto) e "a coisa que sempre olho primeiro" (aprendida com o uso).
- **Todas as opções e o "para quê"** são obrigatórios em cada pergunta, sem resumir.
- **Usuário que não é advogado:** linguagem simples, e a Capi é sugerida antes de assinar
  ou enviar algo de risco alto (`AGENTS.md` §1 e §8). O bloco começa com "[quem sou]".

## 0.5 · 2026-10-02

Organização e nomes de arquivos revistos. A estrutura por versões, que serve melhor a
contratos, foi mantida.

- **Subpastas do assunto numeradas**, na ordem do trabalho: `01_documentos/`,
  `02_versoes/`, `03_entregas/`. A `ficha` e o `historico` mantêm os nomes.
- **Pasta do assunto com nome neutro:** `AAAA-MM_assunto-curto`, sem o nome da
  contraparte, de pessoas, motivos ou valores. Eles ficam na `ficha`.
- **Assuntos criados antes da 0.5** continuam valendo com os nomes antigos. O assistente
  usa as pastas que existirem e não renomeia sem perguntar.
- **Nomes de documentos recebidos:** `AAAA-MM-DD_tipo_descritor.ext`, com lista curta de
  tipos e `sem-data_` quando a data é desconhecida. Os nomes das versões não mudam.
- **Regras para todos os nomes:** minúsculas, sem acento nem espaço, nada sensível
  (CPF, CNPJ, valores, motivos), sem "final" ou "revisado".
- **Permissão de IA por assunto:** campo "IA pode ler esta pasta?" no topo da `ficha`. Se
  for "não", o assistente para. Também no bloco de configuração.
- **Guarda de arquivos:** campos "Encerrado em" e "Guardar até" na `ficha`, com piso de
  5 anos. No encerramento, o fim da guarda vai para `datas-chave`. O assistente só avisa;
  nada é apagado sem o OK do advogado.
- **Antes de um arquivo sair do escritório:** lembrar de remover autor, comentários e
  histórico de alterações, salvo num redline intencional.
- **Pastas antigas:** opção de data de corte com `_legado/` (só leitura), além de adaptar
  no lugar. Ao reabrir um assunto antigo, copiar em vez de mover.
- **Ponteiro na raiz da pasta** (`estrutura/raiz/AGENTS.md`) traz as regras da pasta:
  ficha primeiro, estrutura, nomes, propor em vez de executar, não inventar dados.

## 0.4 · 2026-10-01

Ajustes após o primeiro teste com um advogado.

- **Prompt de configuração** (`prompt-de-configuracao.md`). É um texto único que o
  advogado copia e cola numa conversa nova. Funciona sem abrir links, inclusive no Gemini.
  O assistente:
  - explica antes o que vai fazer, o que acessa e o que fica privado, e só começa depois
    do "sim";
  - verifica se já existe configuração;
  - faz 5 perguntas, com opções fixas e o "para quê" de cada uma;
  - pergunta sobre o armazenamento em dois passos (onde você guarda hoje; pasta nova ou
    existente);
  - testa o acesso;
  - guarda uma nota curta na memória;
  - oferece o bloco para as instruções.
- **`AGENTS.md` lista o endereço completo de cada arquivo do método** (§12). O Claude só
  abre endereços escritos por extenso. No teste, ele não conseguiu abrir as rotinas.
- `rotinas/configurar.md` passa a apontar para o prompt, que é a única fonte dos passos.

## 0.3 · 2026-10-01

- O bloco de configuração passa a trazer um **resumo do método**. Assim as regras e o
  jeito de trabalhar valem mesmo quando o assistente não abre o endereço do método.
- Dois blocos:
  - completo, com cerca de 3.200 caracteres, para ChatGPT pago, Claude, Gemini e Grok;
  - curto, com cerca de 900 caracteres, para ChatGPT Free e Go.
- O bloco e a configuração **não pedem mais nome nem número da OAB**. Esses dados são
  opcionais no perfil e só são pedidos quando um documento precisar deles.
- `configuracao/instrucoes-curtas.md` foi removido; o conteúdo está no bloco completo.
- `configuracao/ferramentas.md` foi reescrito:
  - como começar;
  - onde colar o bloco;
  - o que cada assistente consegue fazer na pasta, no computador ou por conector.

## 0.2 · 2026-10-01

- O método passa a viver num repositório público, separado da pasta do advogado.
- A pasta de trabalho do advogado pode ficar no Google Drive, OneDrive, Dropbox ou no
  computador. É definida na configuração e registrada em `_escritorio/configuracao`.
- Bloco de configuração para colar nas instruções de cada assistente
  (`configuracao/bloco-de-configuracao.md`). Inclui as regras que nem o método muda.
- Registros em `.md` ou Google Docs, conforme o modo de uso (`estrutura/LEIA-ME.md`).
- Configuração com 6 perguntas, incluindo onde ficam os arquivos, o teste de acesso e a
  entrega do bloco.
- Regra da memória: a memória do assistente guarda só a configuração, nunca fatos de
  clientes.

## 0.1 · 2026-10-01

- Primeira versão: rotinas de configuração, novo cliente, revisão (com triagem de NDA),
  redação, comparação de versões, resumo para o cliente e datas do contrato.
- Guias de direito brasileiro: pontos gerais, prestação de serviços, SaaS e software,
  confidencialidade.
