# Rotina: datas do contrato

**Quando usar:**
- um contrato foi assinado;
- o advogado pergunta "quando vence?", "até quando dá para cancelar?";
- o advogado pergunta "o que vence nos próximos 90 dias?".

**Princípio:** registrar e mostrar a conta, nunca apresentar como certo. O sistema oficial
de prazos do advogado continua sendo o dele (`perfil.md`).

---

## Modo 1: extrair as datas de um contrato

1. Leia a versão assinada (`versoes/vNN-...-assinada`). Se só houver minuta, avise que as
   datas podem mudar.
2. Extraia, citando a cláusula de cada uma:
   - início da vigência;
   - prazo e data de término;
   - renovação: automática ou não, por quanto tempo, quantas vezes;
   - **prazo para avisar que não vai renovar**;
   - reajuste: data-base, índice, periodicidade;
   - outras: marcos de entrega, pagamentos, vencimento de garantia ou seguro, fim da
     confidencialidade, carência para sair.
3. **Datas calculadas mostram a conta.** Exemplo: "Término 31/01/2027 menos 60 dias
   (cl. 12.2) = 02/12/2026 `[conferir]`".
   - Atenção a "dias úteis" e "dias corridos".
   - Atenção a "antecedência mínima de", que significa até aquela data, inclusive.
   - Atenção a datas que caem em fim de semana.
   - Se o contrato for ambíguo, mostre as duas leituras.
4. Grave em dois lugares:
   - na seção "Datas do contrato" da `ficha.md`;
   - no índice `_escritorio/datas-chave.md`: uma linha por data, com cliente, assunto, a
     conta e o status "aberta".
5. Sugira ao advogado levar as datas críticas para a agenda ou o sistema de prazos dele.
   Se houver conector de agenda, ofereça criar o lembrete. Só crie com confirmação.

## Modo 2: o que vence

Pedido como "o que vence nos próximos 90 dias?":

1. Leia **só** `_escritorio/datas-chave.md`. Não abra pastas de clientes para isso.
2. Agrupe:
   - ⛔ já passou e ainda está "aberta";
   - 🔴 até 14 dias;
   - 🟠 de 15 a 45 dias;
   - 🟡 de 46 a 90 dias.
3. Para cada linha: data, o quê, cliente, assunto e a ação típica. Exemplo: "decidir com
   o cliente se renova; se não, enviar notificação até X".
4. Ofereça abrir o assunto de uma linha específica para preparar a notificação ou o
   resumo ao cliente.

## Modo 3: carregar contratos antigos

Para contratos assinados antes de usar esta pasta, ofereça uma varredura **por cliente**:
o advogado aponta a pasta e o assistente aplica o Modo 1 a cada contrato. Sem cliente
definido, não varra pastas de vários clientes de uma vez.

## Fechar uma data

Quando a ação foi tomada (notificação enviada, renovação decidida), mova a linha para
"Encerradas" em `datas-chave.md`, com a resolução, e registre no `historico.md` do assunto.
