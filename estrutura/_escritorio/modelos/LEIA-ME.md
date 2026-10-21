# Modelos

Seus modelos e cláusulas. **É a base preferida do assistente para redigir**, porque mantém
a sua estrutura, numeração e estilo. Quando usar um modelo seu, o assistente sempre avisa
qual.

## O que colocar aqui

- **Seus contratos-modelo**, um arquivo por tipo. Use nomes simples, como
  `prestacao-de-servicos.docx`, `nda-mutuo.docx`, `saas-contratada.docx`.
- **Seus documentos de início:**
  - proposta de honorários;
  - contrato de honorários;
  - procuração.

  Use os nomes `proposta-de-honorarios.docx`, `contrato-de-honorarios.docx` e
  `procuracao.docx`.
- **Cláusulas avulsas** que você reaproveita: em `clausulas.md`.
- **O índice** (`indice.md`): para que tipo de documento e em que casos cada modelo deve
  ser usado.

## Transformar um trabalho seu em modelo

No fim de uma conversa, diga "salve isto como modelo". O assistente segue
`rotinas/salvar-modelo.md`:
1. combina com você o tipo, o lado e quando usar o modelo;
2. tira tudo o que identifica o cliente (nomes, documentos, valores, detalhes do negócio,
   autor e comentários do arquivo) e troca por campos `[preencher: …]`;
3. mostra o modelo limpo e a lista do que removeu;
4. só grava aqui depois do seu "sim".

## Regras

- **Nada que identifique um cliente.** Vale para o modelo, para o nome do arquivo e para
  o índice.
- **Seus modelos ficam só nesta pasta.** O método (o repositório público) e o conector da
  Capi não leem nem recebem seus modelos.
- Prefira `.docx` ou `.md`. Google Docs nativo não pode ser lido por assistentes que
  trabalham na pasta do computador.
- **Nunca por cima.** Um modelo atualizado é um arquivo novo, com a data no nome; o
  índice indica qual é o atual.
