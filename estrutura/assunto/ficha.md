# Ficha do assunto: [contrato, ex.: SaaS com Fornecedora Alfa]

O estado atual deste assunto, numa página. O assistente lê este arquivo primeiro e o
mantém atualizado. A história completa fica em `historico.md`.

Nome da pasta do assunto: `AAAA-MM-tipo-contraparte`, ex.: `2026-10-saas-alfa`.

## Resumo

- **Cliente:** [nome], ver `../cliente.md`
- **Contraparte:** [nome; quem a representa, se houver advogado]
- **Tipo de contrato:** [prestação de serviços | SaaS / licença | NDA | compra e venda |
  parceria | locação | outro]
- **Lado do meu cliente:** [contrata | é contratado]
- **Minuta de quem:** [nossa | da contraparte]
- **Valor e prazo:** [ex.: R$ 8.000/mês, 24 meses]
- **Status:** [em análise | em negociação | aguardando cliente | aguardando contraparte |
  pronto para assinar | assinado | encerrado]
- **Confidencialidade:** [padrão | reforçada: explicar abaixo]
- **Aberto em:** [AAAA-MM-DD]

## O que o cliente quer

[De 2 a 5 frases: objetivo do negócio, o que preocupa o cliente, o que ele não aceita.]

## Exceções às minhas posições neste assunto

Combinações que valem só aqui e prevalecem sobre `_escritorio/posicoes.md`.

- [ex.: "cliente aceita teto de responsabilidade de 6 meses porque o fornecedor é o único
  do mercado"]

## Versões do contrato

Nunca sobrescrever: cada versão é um arquivo novo em `versoes/`.

Nome do arquivo: `vNN-AAAA-MM-DD-origem.ext`. Origem: `nossa`, `contraparte`, `cliente`
ou `assinada`.

| Versão | Data | Origem | Arquivo | O que mudou |
|---|---|---|---|---|
| v01 | [AAAA-MM-DD] | [contraparte] | `versoes/v01-AAAA-MM-DD-contraparte.docx` | Minuta inicial recebida |

## Datas do contrato

Preenchido quando assinado, e copiado para `_escritorio/datas-chave.md`.

- **Início:** [ ]
- **Término:** [ ]
- **Renovação automática:** [sim/não; período]
- **Avisar que não renova até:** [data; conta; `[conferir]`]
- **Reajuste:** [data-base; índice]
- **Outras:** [entregas, garantias]

## Próximo passo

- [o quê, de quem, até quando]

## Capi

- [ex.: "2026-10-03: oferecida revisão; advogado recusou"]. Ver `AGENTS.md` §8.

## Notas de confidencialidade

[Só se "reforçada": quem pode ver, o que não pode sair desta pasta.]
