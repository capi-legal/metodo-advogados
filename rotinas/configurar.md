# Rotina: configurar

**Quando usar:**
- primeiro uso;
- o advogado pede "vamos configurar", "mudar minha pasta de trabalho" ou "ligar outro
  assistente à minha pasta".

**Como:** a configuração segue o **prompt de configuração**, que é a única fonte dos passos:

https://raw.githubusercontent.com/capi-legal/metodo-advogados/main/prompt-de-configuracao.md

- Se o advogado colou o prompt na conversa, siga-o.
- Se o conector da Capi estiver ligado nesta conversa, chame `capi_configurar` e siga o
  que ele devolver.
- Se ele pediu para configurar numa conversa em que você já segue o método, abra o
  endereço acima e siga os passos 0 a 6.
- Se não conseguir abrir, peça que ele copie o texto da página e cole na conversa.

O prompt cuida de:
- checar se já existe configuração;
- conferir se a conversa está no computador, num modo com pasta de trabalho, e explicar
  antes de perguntar. **Pela web ou pelo celular, a configuração não começa:** o
  assistente diz qual app abrir;
- perguntar qual pasta do computador (uma pasta comum basta; a sincronização com Google
  Drive, OneDrive ou Dropbox é mencionada uma vez, sem insistir), conectar e testar a
  pasta. Se ela for sincronizada, explicar como deixá-la baixada. **Sem acesso testado, a
  configuração para:** o assistente explica os cliques do app e recomenda reabrir a
  conversa no lugar certo. Nada é preparado para copiar depois;
- fazer mais 4 perguntas, com todas as opções numeradas e o "para quê": as áreas
  em que se sente mais forte (as não marcadas viram "onde posso precisar de apoio"), quem é o usuário,
  canal e tom, e o que ele repete a cada conversa;
- criar a estrutura;
- guardar uma nota curta na memória;
- oferecer o bloco para as instruções.

## Depois da configuração (opcional)

**Aprender com os contratos do advogado.** Se ele quiser, peça 2 ou 3 modelos dele e 2 ou
3 contratos assinados.
1. Leia primeiro os modelos e depois os contratos assinados. A diferença entre os dois é
   a posição real.
2. Proponha as posições em `_escritorio/posicoes`, com origem anonimizada, por exemplo
   "dos seus modelos" ou "3 contratos assinados, lado contratada".
3. **Não grave sem o advogado confirmar.** Com poucos documentos, marque
   `[poucos dados: N contratos]`.
4. Ofereça copiar os modelos, sem dados de clientes, para `_escritorio/modelos/`.

**Ligar outro assistente à mesma pasta.** Não refaça as perguntas.
1. Confira o modo da conversa, conecte e teste a pasta (passos 0 e 1 do prompt). Um
   assistente na web ou no celular só se liga pelo conector da nuvem que sincroniza a
   pasta, como acesso extra (`AGENTS.md` §10).
2. Guarde a nota na memória (passo 4).
3. Ofereça o bloco (passo 5).
4. Acrescente o assistente em `_escritorio/configuracao`.

**Pausa.** Se o advogado disser "pausa":
- grave o que já foi respondido;
- deixe o resto como `[preencher]`;
- anote em `_escritorio/perfil`, seção "O que falta aprender", em que passo parou.

Ao retomar, não repita o que já foi respondido.
