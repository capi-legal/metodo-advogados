# Rotina: configurar (cerca de 3 minutos)

**Quando usar:**
- primeiro uso: não há pasta de trabalho na configuração do assistente, ou o
  `_escritorio/perfil` ainda está com `[preencher]`;
- o advogado pede "vamos configurar", "me entreviste", "mudar minha pasta de trabalho" ou
  "configurar outro assistente".

**Resultado:**
1. A **pasta de trabalho** criada (ou adotada) e testada.
2. `_escritorio/configuracao`, `_escritorio/perfil` e `_escritorio/posicoes` preenchidos.
3. O **bloco de configuração** pronto para o advogado colar nas configurações de cada
   assistente.

Todo o resto o assistente aprende com o uso (`AGENTS.md` §9).

---

## Antes da primeira pergunta

Diga, em no máximo 3 linhas:

> Vou fazer 6 perguntas rápidas: duas sobre onde você guarda seus arquivos e quatro sobre
> como você trabalha. Leva uns 3 minutos. O que você não souber agora fica pendente. Se
> quiser parar, diga "pausa".

**Ritmo:**
- No máximo 2 perguntas por mensagem.
- Use opções clicáveis quando a ferramenta permitir.
- Se a resposta provavelmente já está escrita em algum lugar (site, modelo), peça o link
  ou o arquivo em vez de pedir que o advogado digite.

## As 6 perguntas

**Onde guardar**

1. **Quem é você, e que assistentes de IA você usa?**
   - Nome, OAB/UF, se trabalha sozinho(a) ou com equipe.
   - Quais assistentes (ChatGPT, Claude, Gemini, outro) e onde: no computador, na web, no
     celular.
2. **Onde ficam, ou vão ficar, seus arquivos de trabalho?**
   - Google Drive, OneDrive, Dropbox, outro, ou só no computador.
   - **Cole o link da pasta**, ou o caminho no computador. Se ainda não existe, sugira criar
     uma chamada "Escritório IA".
   - Se você já tem pastas de clientes, diga onde estão.

**Como você trabalha**

3. **Que contratos e clientes mais aparecem?**
   - Os 3 tipos mais frequentes.
   - Que tipo de cliente.
   - Que áreas você *não* atende.
4. **De que lado seu cliente costuma estar, e de quem é a minuta?**
   - Quem contrata, quem é contratado, ou varia.
   - Minuta sua ou da outra parte.
5. **O que você sempre olha primeiro?**
   - O único problema que faria você recusar um contrato.
   - Se quiser, mais 1 ou 2 posições firmes.
6. **Como você entrega?**
   - Formato da revisão.
   - Tom.
   - Canal com o cliente: WhatsApp ou e-mail.
   - Opcional: aponte 2 ou 3 contratos seus que representem bem o seu padrão.

**Verifique fatos jurídicos ditos nas respostas.** Se algo parecer errado, pergunte antes
de gravar.

## Definir o formato e testar o acesso

Com as respostas 1 e 2:

1. **Escolha o formato dos registros** pela tabela de `estrutura/LEIA-ME.md`:
   - algum assistente vai trabalhar **no computador** sobre a pasta: `.md`;
   - **só web ou celular**, com Google Drive: Google Docs;
   - diga ao advogado qual formato escolheu e por quê, em uma frase.
2. **Modo computador com Drive, OneDrive ou Dropbox.** Oriente:
   - instalar o app de sincronização;
   - deixar a pasta **baixada no computador** (Drive: "espelhar" ou "disponível
     off-line"; OneDrive: "Sempre manter neste dispositivo");
   - abrir no assistente a **pasta de trabalho**, não a raiz do Drive.
3. **Teste o acesso** de onde você está agora:
   - consegue ler a pasta?
   - consegue criar um arquivo?
   - consegue editar um arquivo existente?

   Crie `_escritorio/configuracao` (é o teste de criação) e depois acrescente a data nele
   (é o teste de edição). Registre o resultado na tabela "Assistentes e acesso".
   - **Não diga que o acesso funciona sem ter testado.**
   - Os outros assistentes do advogado serão testados quando ele os usar pela primeira
     vez.
4. **Se não houver acesso nenhum** (assistente sem conector), diga isso e ofereça:
   - conectar o armazenamento (`conectores/LEIA-ME.md`);
   - ou usar um assistente no computador;
   - ou trabalhar enviando os arquivos na conversa e salvando o que eu entregar.

## Criar ou adotar a pasta

A partir de `estrutura/`, no método, no formato escolhido:

1. **`_escritorio/`:**
   - `configuracao`, `perfil`, `posicoes`, `clientes`, `datas-chave`, `referencias`;
   - a pasta `modelos/`, com `LEIA-ME` e `clausulas`.

   Não copie as linhas `_exemplo_`.
2. **`clientes/`**, vazia. Se o advogado já tem pastas de clientes, registre o caminho em
   `configuracao` e não mova nada.
3. **Modo computador:** copie `estrutura/raiz/AGENTS.md`, `CLAUDE.md` e `GEMINI.md` para a
   raiz da pasta. Se o advogado fixou uma versão do método, troque `main` no endereço pela
   versão. Assim os assistentes de computador encontram o método sozinhos.
4. **Se a pasta já existe com outro conteúdo**, pergunte antes de criar qualquer coisa.

## Gravar as respostas

1. Antes de gravar, liste o que ficou sem resposta e pergunte uma vez: "Ficaram em aberto
   [lista]. Preencher agora ou deixo como pendente?". Nunca grave lacunas em silêncio.
2. **`configuracao`:** pasta, link ou caminho, formato, assistentes e acesso testado,
   endereço e versão do método, data.
3. **`perfil`:** respostas 1, 3, 4 e 6, com as palavras do advogado sempre que possível.
   - O que faltou fica `[padrão]` ou `[preencher]`.
   - Liste as pendências em "O que falta aprender".
4. **`posicoes`:**
   - "A coisa que sempre olho primeiro";
   - as posições firmes da resposta 5, na tabela do lado certo, com origem
     "entrevista AAAA-MM";
   - o resto continua `[padrão]`.
5. Mostre um resumo do que gravou (até 10 linhas).

## Entregar o bloco de configuração

1. Preencha o bloco de `configuracao/bloco-de-configuracao.md` com:
   - nome, OAB;
   - endereço do método;
   - **link da pasta** (não só o nome: pode haver pastas com o mesmo nome) ou caminho
     local.
2. Entregue o bloco **pronto para copiar**, com o passo a passo de onde colar em cada
   assistente que o advogado citou (`configuracao/ferramentas.md`).
3. Se você tiver memória e o advogado pedir, guarde o bloco nela também. **Só o bloco;
   nada sobre clientes.**
4. Peça o teste:
   - abrir uma conversa nova e perguntar "Onde ficam meus arquivos e qual método você
     segue?";
   - o assistente deve responder sem que ele repita.

## Opcional: aprender com os contratos do advogado

Se o advogado apontou contratos na pergunta 6:

1. Leia primeiro os **modelos** dele, depois os **contratos assinados**. A diferença entre
   os dois é a posição real.
2. Proponha as posições numa tabela, com origem anonimizada.
   - **Não grave sem o advogado confirmar.**
   - Com poucos documentos, marque `[poucos dados: N contratos]`.
3. Ofereça copiar os modelos, sem dados de clientes, para `_escritorio/modelos/`.

## Fechar

Termine com 3 sugestões de primeiro uso, adaptadas ao que ele contou. Por exemplo:

- "Me mande um contrato que está na sua mesa e eu reviso."
- "Vamos organizar a pasta de um cliente atual."
- "Me diga um contrato que você sempre redige e eu monto a partir do seu modelo."

## Configurar outro assistente depois

Se o advogado já tem a pasta e quer usar mais um assistente:

1. Não refaça a entrevista.
2. Entregue o mesmo bloco de configuração com o passo a passo daquele assistente.
3. Teste o acesso dele à pasta e acrescente uma linha em "Assistentes e acesso".

## Pausa e retomada

Se o advogado disser "pausa":

- grave o que já foi respondido;
- marque o restante como `[preencher]`;
- anote em "O que falta aprender": "configuração pausada na pergunta N".

Ao retomar, não repita o que já foi respondido.
