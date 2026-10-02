# Ficha do assunto: [contrato, ex.: SaaS com Fornecedora Alfa]

- **IA pode ler esta pasta?** [sim | não]. Termo do cliente: [ver `../cliente.md`]

O estado atual deste assunto, numa página. O assistente lê este arquivo primeiro e o
mantém atualizado. Se "IA pode ler esta pasta?" disser "não", ele para e não abre mais
nada do assunto. A história completa fica em `historico.md`.

Nome da pasta do assunto: `AAAA-MM_assunto-curto`, neutro, ex.: `2026-10_saas-gestao-estoque`.
Nada de nomes de pessoas, motivos ou valores no nome: eles ficam aqui.

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
- **Aberto em:** [AAAA-MM-DD] · **Encerrado em:** [ ]
- **Guardar até:** [mínimo de 5 anos após o encerramento; acima disso, decisão do
  advogado]. Ao chegar a data, o assistente só avisa: nada é apagado sem o OK do advogado.

## O que o cliente quer

[De 2 a 5 frases: objetivo do negócio, o que preocupa o cliente, o que ele não aceita.]

## Exceções às minhas posições neste assunto

Combinações que valem só aqui e prevalecem sobre `_escritorio/posicoes.md`.

- [ex.: "cliente aceita teto de responsabilidade de 6 meses porque o fornecedor é o único
  do mercado"]

## Versões do contrato

Nunca sobrescrever: cada versão é um arquivo novo em `02_versoes/`.

Nome do arquivo: `vNN-AAAA-MM-DD-origem.ext`. Origem: `nossa`, `contraparte`, `cliente`
ou `assinada`.

| Versão | Data | Origem | Arquivo | O que mudou |
|---|---|---|---|---|
| v01 | [AAAA-MM-DD] | [contraparte] | `02_versoes/v01-AAAA-MM-DD-contraparte.docx` | Minuta inicial recebida |

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
