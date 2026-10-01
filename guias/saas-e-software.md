# SaaS, licença de software e desenvolvimento

Use junto com `pontos-gerais.md`. Todas as referências são `[conferir]` (ver `LEIA-ME.md`).

---

## Pontos próprios deste tipo

1. **Natureza do negócio.**
   - É licença de uso (Lei 9.609/1998), serviço em nuvem (SaaS), desenvolvimento sob
     encomenda ou uma combinação?
   - A natureza afeta os tributos. Licenciamento e cessão de uso de software estão na
     lista do ISS (LC 116/2003, item 1.05), e o STF firmou a incidência de ISS sobre
     software (ADIs 1.945 e 5.659). Confira com o contador do cliente.
2. **Desenvolvimento sob encomenda.**
   - Salvo estipulação em contrário, pertencem ao contratante os direitos sobre programa
     desenvolvido durante o contrato, quando o desenvolvimento é o objeto contratado
     (Lei 9.609/1998, art. 4º).
   - Deixe isso **expresso**, inclusive quanto a código-fonte, documentação e componentes
     pré-existentes ou de terceiros (open source).
3. **Renovação e preço.** Renovação automática, aviso para cancelar, reajuste na
   renovação, fim de preço promocional. Cite a condição completa.
4. **Disponibilidade e suporte.** SLA (percentual mensal), janelas de manutenção, créditos
   e o teto dos créditos, prazos de atendimento por severidade.
5. **Dados do cliente.** Ver `pontos-gerais.md` §11 e confira:
   - papéis (o fornecedor costuma ser operador);
   - localização dos dados e transferência internacional;
   - suboperadores (lista e aviso de mudanças);
   - incidentes;
   - **exportação dos dados no fim, em formato utilizável, e prazo para exclusão**;
   - backups.
6. **IA e uso dos dados para treinamento.** Confira cinco pontos:
   1. Há permissão expressa para usar dados ou conteúdo do cliente para treinar ou
      melhorar modelos?
   2. Há permissão indireta, por remissão a uma política que o fornecedor pode mudar
      sozinho?
   3. "Anonimizado" está definido? Por qual padrão?
   4. Há opção de recusa (opt-out) que sobrevive a renovações e mudanças de termos?
   5. Quem é titular dos resultados (outputs) gerados para o cliente?
7. **Limitação de responsabilidade.** Faça a análise das quatro dimensões
   (`rotinas/revisar-contrato.md`). Em SaaS, o teto costuma excluir justamente o que mais
   acontece (vazamento de dados). Confira se dados e confidencialidade estão dentro ou
   fora do teto.
8. **Suspensão e encerramento.** Quando o fornecedor pode suspender o acesso (atraso,
   uso indevido) e com que aviso. O que acontece com os dados na suspensão.
9. **Fornecedor estrangeiro.**
   - lei e foro estrangeiros (`pontos-gerais.md` §8);
   - preço em moeda estrangeira (§16);
   - tributos sobre remessa ao exterior: IRRF, CIDE, PIS e COFINS importação, IOF;
   - termos "clique para aceitar" que mudam unilateralmente.
10. **Continuidade.** Se o fornecedor encerrar o produto ou falir:
    - aviso prévio;
    - exportação dos dados;
    - em desenvolvimento sob encomenda, depósito do código-fonte (escrow), se o valor
      justificar.

## Lado do cliente

| Se o cliente CONTRATA o software, cuide de… | Se o cliente FORNECE o software, cuide de… |
|---|---|
| Exportação de dados e prazo de exclusão | Termos de uso próprios prevalecendo sobre os do cliente |
| Proibição de treinar IA com seus dados | Teto de responsabilidade, exclusão de lucros cessantes |
| Teto que não exclua vazamento de dados | SLA com exclusões claras e créditos como único remédio |
| Aviso de não renovação curto; reajuste com teto | Reajuste anual e direito de suspender por inadimplência |
| Titularidade de customizações | Manter a plataforma e licenciar as customizações |
