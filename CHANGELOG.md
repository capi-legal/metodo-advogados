# Mudanças no método

O assistente informa a versão em uso (topo do `AGENTS.md`). Mudanças que alteram o
comportamento ficam registradas aqui, a mais recente primeiro.

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
