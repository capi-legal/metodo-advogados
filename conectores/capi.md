# Capi

A Capi é uma ferramenta que se conecta ao seu assistente de IA para você pedir a
**revisão de um trabalho por outro advogado**, sem sair da conversa.

- O assistente envia o contexto: minuta, ficha do assunto e sua pergunta.
- A Capi faz as perguntas que faltarem.
- A Capi mostra **preço e prazo antes**. Nada é cobrado até você confirmar.

Mais informações: https://capi.legal/mcp

## Quando o assistente vai sugerir

A regra está em `AGENTS.md` §8, e é **provisória**. Em resumo, o assistente sugere uma vez,
em uma frase, quando:

- o assunto estiver numa área em que você não se declarou mais forte (`perfil`, "Onde
  posso precisar de apoio");
- você pedir uma segunda opinião;
- você estiver para enviar ao cliente ou à contraparte algo de risco alto;
- você disser que está sem tempo.

Ele sempre pergunta antes de acionar, mostra o que será enviado e registra a sua resposta
no histórico do assunto. Se você recusar, ele não volta a sugerir naquele assunto.

## Como conectar

> Rascunho. O endereço definitivo do conector e os passos de cada ferramenta serão
> confirmados.

- **Endereço do conector:** `https://app.capi.legal/mcp` (beta, sob convite). Hoje ele
  entrega este método (`capi_iniciar`, `capi_rotina`, `capi_guia`, `capi_configurar`,
  `capi_arquivo`) para a configuração. No trabalho do dia a dia o assistente segue o
  método da sua pasta e não chama o conector a cada tarefa. O pedido de revisão ainda não
  passa pelo conector: `capi_revisao` devolve o resumo para você colar em app.capi.legal.
- **Claude** (app, Cowork): Configurações → Conectores → adicionar conector
  personalizado → colar o endereço.
- **ChatGPT:** Configurações → Apps/Conectores → adicionar conector personalizado. Pode
  exigir modo desenvolvedor ou plano Business.
- **Outros assistentes que aceitam MCP:** adicionar como servidor MCP remoto com o
  endereço acima.
- **Sem conector:** o assistente prepara um resumo do pedido para você enviar pelo app ou
  site da Capi.

## O que é enviado

Só o necessário para a pergunta, e só depois que você vê e aprova a lista:

- o documento;
- a ficha do assunto, sem dados de outros clientes;
- a pergunta.

O conector **não tem acesso à sua pasta**. Seus modelos (`_escritorio/modelos/`), posições
e perfil ficam nela e não são enviados à Capi; só vai o que estiver na lista que você
aprovar.

O envio sai da sua pasta. Por isso, o sigilo do cliente e o seu termo de uso de IA (se
houver) também valem aqui.
