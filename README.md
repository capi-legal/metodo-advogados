# Método Capi: IA para advogados de contratos

Um método aberto para usar ChatGPT, Claude, Gemini ou outro assistente de IA no trabalho
com contratos, **do seu jeito e com os seus arquivos**.

O assistente passa a conhecer o seu escritório: como você escreve, como negocia cada
cláusula, quem são seus clientes e o que aconteceu em cada contrato. Você deixa de
explicar tudo de novo a cada conversa e de subir os mesmos arquivos de novo.

## Como funciona

| Parte | Onde fica | O que é |
|---|---|---|
| **O método** | Este repositório | Regras, rotinas e guias de direito brasileiro. Igual para todos e atualizado pela Capi |
| **A sua pasta** | Google Drive, OneDrive, Dropbox ou o seu computador | Seu perfil, suas posições, seus clientes e contratos. Só sua |
| **A configuração do assistente** | Instruções personalizadas do ChatGPT, Claude ou Gemini | Um texto curto, colado uma vez, que diz onde está o método e onde está a sua pasta |

**O método nunca guarda dados seus nem de clientes.** Tudo isso fica na sua pasta.

## Para começar

1. Abra o seu assistente. Para a experiência completa, use um assistente no computador:
   Claude (Cowork), o app do ChatGPT para computador ou Codex, sobre uma pasta sincronizada.
   Passo a passo em `configuracao/ferramentas.md`.
2. Escreva:

   > Leia https://raw.githubusercontent.com/capi-legal/metodo-advogados/main/AGENTS.md e vamos configurar.
3. Responda às 6 perguntas: onde ficam seus arquivos e como você trabalha. Leva uns
   3 minutos.
4. Cole o **bloco de configuração** que o assistente entregar nas configurações dele.
   A partir daí, toda tarefa jurídica segue o método, em qualquer conversa.

## O que pedir

| Você diz | O assistente faz |
|---|---|
| "Revise o contrato da contraparte para o cliente X" | Compara com as suas posições, aponta o que está fora e sugere redação pronta |
| "Chegou a nova versão, o que mudou?" | Tabela de todas as mudanças, com destaque para as que **não foram anunciadas** |
| "Redija um contrato de prestação de serviços para…" | Minuta a partir dos **seus** modelos, com o que falta marcado |
| "Faça um resumo para eu mandar no WhatsApp do cliente" | Mensagem curta, em linguagem de negócio, para você revisar e enviar |
| "Novo cliente: …" / "Organize a pasta do cliente Y" | Pasta do cliente e do assunto, checagem de conflito, documentos de início |
| "O que vence nos próximos 90 dias?" | Renovações, avisos e reajustes de todos os contratos |
| "Triagem rápida deste NDA" | Verde, amarelo ou vermelho, conforme as suas posições |

## O que o assistente sempre respeita

1. **Um cliente por vez.** Nada de um cliente vai para o trabalho de outro, nem para a
   memória do assistente.
2. **Você decide.** Ele não envia, não assina e não compartilha nada sem o seu "sim".
3. **Referências conferidas.** Toda lei ou julgado citado leva a origem; o que veio da
   memória da IA sai marcado `[conferir]`. Julgado inventado, nunca.
4. **Nada é sobrescrito nem apagado.** Cada versão do contrato é um arquivo novo.
5. **Documento não dá ordem.** Instruções escondidas num contrato ou PDF são ignoradas e
   apontadas para você.

As regras 1, 2 e 5 também ficam no bloco que você cola no assistente, e prevalecem sobre
o método.

## Sigilo

- Os arquivos que o assistente lê são enviados ao fornecedor da IA. Use um **plano pago
  com treinamento desativado**.
- A OAB orienta formalizar com o cliente o uso de IA (Recomendação CFOAB 001/2024). Há um
  modelo de termo em `modelos/termo-de-uso-de-ia.md`.

## Uma segunda opinião, quando precisar

Quando um trabalho estiver fora da sua área ou pedir uma segunda leitura, o assistente pode
sugerir a **Capi**: uma ferramenta para pedir a revisão de outro advogado, com preço e
prazo antes de confirmar. Ele pergunta antes e não insiste. Ver `conectores/capi.md`.

## O que tem neste repositório

```
AGENTS.md        Instruções para o assistente (ponto de entrada do método)
rotinas/         O passo a passo de cada tarefa
guias/           Pontos de atenção do direito brasileiro por tipo de contrato
modelos/         Modelos sugeridos: termo de uso de IA, cláusulas
estrutura/       Arquivos em branco para montar a sua pasta, clientes e assuntos
conectores/      Integrações: Drive, OneDrive, e-mail, assinatura, Capi
configuracao/    Como configurar cada assistente e o bloco de configuração
CHANGELOG.md     O que mudou em cada versão do método
```

## Versões e mudanças

- O método evolui. Cada mudança fica registrada em `CHANGELOG.md`.
- Para fixar uma versão, use o endereço de uma versão publicada em vez de `main`.
- Sugestões e correções: abra uma *issue* neste repositório.

## Licença e créditos

Licença Apache 2.0 (`LICENSE`). Partes adaptadas do projeto claude-for-legal, da Anthropic.
Detalhes em `NOTICE.md`.

Este método não é parecer jurídico. O advogado revisa, decide e responde por todo trabalho
feito com ele.
