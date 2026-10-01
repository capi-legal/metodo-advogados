# Minhas posições em contratos

Como você negocia cada cláusula, conforme o lado do seu cliente. O assistente compara
todo contrato com esta tabela.

**Começa com valores `[padrão]`, que são pontos de partida usuais de mercado e não
recomendação.** Fica precisa conforme você trabalha. Quando você aceita ou recusa algo
diferente do que está aqui, o assistente pergunta se deve registrar.

Regras deste arquivo:

- **Nunca identifica clientes.** A coluna "Origem" diz de onde veio a posição, por
  exemplo: "entrevista 2026-10", "aprendido em 2026-11, SaaS, lado contratante",
  "dos meus modelos". Nunca nomes.
- **"Só com o cliente"** é o que você não aceita sem uma decisão do cliente. Num
  escritório pequeno, quem decide o risco comercial é o cliente.
- **Exceções de um assunto específico ficam na `ficha.md` daquele assunto**, não aqui.

---

## A coisa que sempre olho primeiro

Se um contrato tiver só um problema que me faria recusar, é este:

- [preencher, ex.: "responsabilidade ilimitada para o meu cliente", "multa rescisória
  desproporcional", "foro em outro estado"]

---

## Quando meu cliente CONTRATA (compra, toma o serviço, licencia)

| Cláusula | Minha posição | Aceito (recuo) | Só com o cliente | Origem |
|---|---|---|---|---|
| Limitação de responsabilidade | Teto para a responsabilidade da contratada não inferior a 12 meses de valores pagos; fora do teto: dolo, culpa grave, confidencialidade, dados pessoais | Teto de 6 meses | Teto abaixo de 6 meses, ou dados pessoais dentro do teto | [padrão] |
| Multa rescisória | Só para a contratada, se houver; ou proporcional ao prazo restante | Multa mútua e proporcional | Multa fixa que não diminui com o tempo | [padrão] |
| Prazo, renovação e saída | Rescisão imotivada com aviso de 30 dias | Aviso de até 90 dias | Sem saída imotivada no prazo inicial | [padrão] |
| Renovação automática | Aceita, com aviso de não renovação de até 30 dias | Até 60 dias | Mais de 60 dias, ou reajuste automático na renovação sem teto | [padrão] |
| Reajuste | Anual, IPCA | IGP-M | Índice não definido ou reajuste unilateral | [padrão] |
| Dados pessoais (LGPD) | Contratada como operadora, com acordo de tratamento, incidente comunicado em prazo curto, exclusão ou devolução ao fim | Prazo de comunicação maior | Uso dos dados para fins próprios da contratada, incluindo treinar IA | [padrão] |
| Propriedade intelectual | Entregáveis feitos sob encomenda passam ao cliente | Licença perpétua e irrevogável de uso | Contratada fica com tudo, sem licença | [padrão] |
| Foro | Domicílio do meu cliente | Capital do estado do meu cliente, ou arbitragem com câmara reconhecida | Foro sem ligação com as partes ou com o contrato | [padrão] |
| Confidencialidade | Mútua, 5 anos após o fim | 3 anos | Só para o meu cliente | [padrão] |

## Quando meu cliente É CONTRATADO (vende, presta o serviço, licencia o próprio produto)

| Cláusula | Minha posição | Aceito (recuo) | Só com o cliente | Origem |
|---|---|---|---|---|
| Limitação de responsabilidade | Teto de 12 meses de valores pagos; exclui lucros cessantes e danos indiretos | Teto de 24 meses; exceções só para dolo e confidencialidade | Responsabilidade ilimitada ou teto acima de 24 meses | [padrão] |
| Multa rescisória | Contratante que sai antes paga proporcional ao prazo restante | Sem multa, com aviso longo | Multa só para o meu cliente | [padrão] |
| Prazo, renovação e saída | Prazo inicial mínimo com renovação automática | Saída imotivada com aviso de 60 dias | Saída imotivada a qualquer momento, sem aviso | [padrão] |
| Reajuste | Anual, IPCA ou IGP-M, o maior | IPCA | Sem reajuste em contrato acima de 12 meses | [padrão] |
| Pagamento e atraso | Multa de 2% mais juros e correção; suspensão do serviço após aviso | Sem suspensão, com multa | Pagamento só após "aceite" sem prazo definido | [padrão] |
| Propriedade intelectual | Meu cliente mantém a plataforma e o conhecimento prévio; cliente recebe licença de uso | Customizações exclusivas passam ao contratante | Cessão de toda PI, inclusive a pré-existente | [padrão] |
| Foro | Domicílio do meu cliente | Domicílio do contratante | Foro sem ligação com as partes ou com o contrato | [padrão] |
| Tributos | Preço sem tributos; reequilíbrio se a reforma tributária mudar a carga | Preço com tributos e cláusula de reequilíbrio | Preço fixo sem reequilíbrio em contrato longo | [padrão] |

---

## Outras cláusulas: ainda sem posição

Para estas cláusulas, o assistente usa os `guias/` e marca `[decidir]` até você definir
uma posição: garantias (fiança, caução, seguro), exclusividade, não concorrência e não
aliciamento, ausência de vínculo e responsabilidade trabalhista, anticorrupção, cessão e
mudança de controle, moeda estrangeira, lei estrangeira, arbitragem.

## Triagem de NDA

| Ponto | Verde | Amarelo | Vermelho | Origem |
|---|---|---|---|---|
| Mutualidade | Mútuo | Unilateral a favor do meu cliente | Unilateral contra o meu cliente | [padrão] |
| Prazo após o fim | Até 5 anos | 5 a 10 anos | Perpétuo | [padrão] |
| Multa por violação | Sem multa fixa, ou fixa e moderada | Fixa e alta | Fixa e desproporcional ao negócio | [padrão] |
| Obrigações extras (não aliciamento, exclusividade, licença) | Nenhuma | Qualquer uma: amarelo automático | — | [padrão] |
| Foro | Domicílio do meu cliente ou capital | Outro foro no Brasil | Exterior | [padrão] |

**Verde só vale com posições confirmadas por você.** Enquanto esta tabela estiver em
`[padrão]`, a melhor classificação possível é amarelo.

## Histórico de mudanças nas posições

Uma linha por mudança, a mais recente primeiro: data, o que mudou, por quê. Sem nomes de
clientes.

- [vazio]
