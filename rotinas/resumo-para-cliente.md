# Rotina: resumo para o cliente

**Quando usar:** "faça um resumo para o cliente", "o que eu mando para ele no WhatsApp?",
"explica para o cliente o que esse contrato diz", depois de uma revisão ou comparação.

**Resultado:** uma mensagem curta, em linguagem de negócio, que o advogado revisa e envia.
**O assistente nunca envia.**

O cliente não quer um parecer. Quer saber três coisas: posso assinar, qual é o porém e o
que eu preciso fazer.

---

## Passo 1: de onde vem o conteúdo

- Se já existe uma revisão ou comparação em `entregas/`, **resuma essa entrega**. Não
  revise o contrato de novo.
- Se não existe, faça antes a revisão (`rotinas/revisar-contrato.md`) ou pergunte se o
  advogado quer só uma explicação do contrato.
- Use o lado do cliente na voz certa:
  - quando o cliente contrata: "o que você recebe e o que aceita abrir mão";
  - quando o cliente é contratado: "o que você vende e com o que se compromete".

## Passo 2: escrever

**Canal:** veja o `cliente.md`. Se não houver, use o perfil.

**WhatsApp:**
- até ~120 palavras;
- sem títulos e sem tabelas;
- parágrafos curtos;
- no máximo um emoji, se o perfil permitir.

**E-mail:** até ~200 palavras, neste formato:

```
Assunto: [contrato] com [contraparte]: [pronto para assinar | precisa de ajustes |
não recomendo assinar como está]

[1 parágrafo: o que é este contrato, em termos de negócio.
Não "Contrato de Prestação de Serviços de Tecnologia", e sim "o contrato da plataforma
de gestão que vocês querem usar".]

[1 parágrafo: o porém, aquilo que vai surpreender o cliente depois se ninguém avisar
agora. Ou, se não houver: "Contrato equilibrado, sem surpresas."]
[Se houver ajustes: "Estamos pedindo [N] mudanças. A principal: [em linguagem simples].
[Avaliação realista: provavelmente aceitam / pode travar a negociação]."]

O que preciso de você:
- [no máximo 3 itens; ex.: "decidir se aceita a multa de 20% caso eles não cedam"]
  ou "Nada por enquanto, aviso quando a outra parte responder."

[1 linha: próximo passo e prazo]
```

**Traduza:**

| Jurídico | Para o cliente |
|---|---|
| Limitação de responsabilidade a 12 meses de remuneração | Se eles causarem um prejuízo, o máximo que vocês recebem é o equivalente a um ano de pagamentos |
| Renovação automática, aviso de 60 dias | Renova sozinho todo ano. Para cancelar, é preciso avisar com dois meses de antecedência |
| Rescisão imotivada vedada no prazo inicial | Durante o primeiro período, vocês não podem sair só porque não querem mais |
| Cláusula penal de 20% sobre o saldo | Quem sair antes paga uma multa de 20% do que faltaria pagar |
| Operador de dados (LGPD) | Eles vão tratar dados pessoais dos seus clientes em nome de vocês, e vocês continuam responsáveis |
| Foro da comarca de X | Se der briga na Justiça, o processo corre em X |

**Não incluir:**
- números de cláusula;
- termos entre aspas;
- latim;
- "outrossim";
- "data venia";
- tabelas de risco com cores;
- ressalvas de que "isto não é parecer" (o cliente sabe quem mandou).

**Citações:** se citar o contrato, cite a frase inteira, com a condição. Se não couber,
parafraseie sem perder a condição. "Na renovação, o preço promocional volta ao preço de
tabela" é uma paráfrase correta. "O preço volta ao preço de tabela" muda o sentido.

**Não prometa o que não foi feito.** Só escreva "já anotei a data de renovação" se
`_escritorio/datas-chave.md` foi de fato atualizado. Caso contrário, faça a anotação
(`rotinas/datas-do-contrato.md`) ou transforme em pendência.

## Passo 3: conferir o destino

A mensagem vai para fora do escritório. Antes de entregar, confira:

- sem notas internas;
- sem posições do advogado;
- sem `[decidir]` nem `[conferir]`;
- sem informação de outro cliente;
- sem detalhe de estratégia que o advogado não queira mostrar.

Entregue o texto pronto para copiar. Salve em `entregas/AAAA-MM-DD-resumo-cliente.md`.
Registre no `historico.md` ("resumo preparado; envio pelo advogado").
