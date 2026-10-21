# Formatação dos documentos

Como o assistente faz os documentos do advogado saírem **com a cara dos dele**, e não com
a formatação padrão do assistente.

As preferências de cada advogado ficam na pasta dele, em `_escritorio/formatacao.md`
(modelo em branco: `estrutura/_escritorio/formatacao.md`). Este arquivo explica o que se
registra, as 3 opções prontas oferecidas na configuração e como aplicar.

---

## O que se registra

| Item | Exemplos |
|---|---|
| **Fonte e tamanho** | Times New Roman 12; Arial 11; títulos no mesmo tamanho ou maiores |
| **Espaçamento e alinhamento** | 1,5 entre linhas, justificado; 6 pt depois do parágrafo |
| **Margens e papel** | A4; superior e esquerda 3 cm, inferior e direita 2 cm |
| **Títulos das cláusulas** | "CLÁUSULA PRIMEIRA – DO OBJETO"; "1. Objeto"; negrito, caixa alta ou não |
| **Numeração** | 1.1, 1.1.1; parágrafos "Parágrafo único", "§ 1º"; alíneas "a)", "i." |
| **Estrutura** | título do contrato; quadro-resumo no início ou não; considerandos; definições em cláusula própria ou ao longo do texto |
| **Qualificação das partes** | parágrafo corrido ou quadro; ordem dos dados |
| **Cabeçalho e rodapé** | logo ou nome do escritório; número de página "Página X de Y"; rubrica |
| **Bloco de assinaturas** | local e data; linha com nome, cargo e CNPJ; testemunhas; assinatura eletrônica |
| **Anexos** | "Anexo I – …"; numeração própria ou contínua |
| **Outros documentos** | memorandos de revisão, resumos e cartas: mesma fonte, ou formato próprio |

O que é **estilo de redação**, e não formatação, fica em `_escritorio/perfil.md`
("Particularidades de redação"): como chamar as partes, expressões que o advogado usa ou
evita.

## Como as preferências são coletadas

Na configuração (pergunta 4 do prompt de configuração) ou a qualquer momento, quando o
advogado pedir "formate como os meus contratos".

1. **Melhor caminho: um documento de que o advogado gosta.** Ele manda um contrato ou
   modelo dele, ou indica onde ele está na pasta. O resultado são **regras em texto
   simples**, confirmadas por ele e gravadas em `_escritorio/formatacao.md`. É o que vale
   para os próximos documentos, em qualquer assistente.
   - **Avise que leva tempo.** Assim que receber o arquivo, e antes de começar a ler,
     diga: "Recebi. A análise da formatação leva alguns minutos; eu aviso quando
     terminar." Sem o aviso, a pessoa acha que travou.
   - **Peça um `.docx`, se houver.** Dele se tiram fonte, tamanho, margens e espaçamento
     exatos. De um PDF com texto, fonte e tamanho são confiáveis, mas margens e
     espaçamento são estimados. De uma foto ou digitalização, tudo é aproximado. Diga
     isso ao advogado quando o arquivo não for `.docx`.
   - **Confira que você enxerga a formatação.** Se você só recebeu o texto do arquivo,
     sem fontes e tamanhos (acontece em conversas pela web; no ChatGPT, a leitura da
     formatação funciona no modo Work, com a pasta), não adivinhe: diga isso e peça o
     `.docx` na pasta, ou ofereça as opções prontas.
   - **Leia só a forma**, item por item da tabela "O que se registra": fontes, tamanhos,
     espaçamento, margens, títulos, numeração, a estrutura do documento (por exemplo, um
     quadro com os termos principais no início e depois as demais condições), partes,
     cabeçalho, rodapé, assinaturas e anexos. Num `.docx`, prefira os estilos e as
     propriedades do arquivo ao que parece visualmente.
   - **Documento misturado:** registre o padrão que predomina e diga o que foge dele
     ("2 cláusulas estão em Arial, o resto em Times; vou usar Times"). Não tire uma média
     em silêncio.
   - **O conteúdo não vai para `_escritorio/`.** O exemplo costuma ser um contrato real,
     com dados de cliente. Descreva a forma de modo genérico ("quadro no início com
     partes, preço e prazo"), nunca com nomes, valores ou cláusulas.
   - **Mostre as regras ao advogado** em texto simples, em até 12 linhas, na ordem da
     tabela. Marque o que o documento não define como "fica a meu critério".
   - **Mostre uma página de amostra:** gere um `.docx` de uma página com essas regras
     (título, quadro ou qualificação, duas cláusulas com subitens, assinaturas) e peça
     que ele confira olhando. Muita gente não sabe dizer se gosta de "espaçamento 1,5",
     mas reconhece a página.
   - **Pergunte se vale para todos os contratos** ou só para um tipo (por exemplo, NDA com
     outra cara). Se for por tipo, registre a seção "Por tipo de contrato".
   - Grave só depois do "sim".
   - **Cópia do arquivo, opcional:** o texto não reproduz tudo. Logo no cabeçalho, quadros
     com bordas e sombreados e assinaturas em tabela saem parecidos, não iguais. Se for um
     **modelo** do próprio advogado, sem dados de clientes, ofereça guardar uma cópia em
     `_escritorio/modelos/` e indicá-la como "arquivo de referência" em `formatacao.md`.
     Se o arquivo tiver dados de cliente, a cópia passa antes por
     `rotinas/salvar-modelo.md`.
     As regras em texto continuam valendo; o arquivo só completa o que elas não descrevem.
2. **Sem documento à mão:** ofereça as 3 opções prontas abaixo. O advogado escolhe uma e
   pode ajustar qualquer item.
3. **Sem preferência:** use a opção 2 (Moderno) marcada `[padrão]` e anote em "O que
   falta aprender", no `perfil`, que vale mandar um documento de referência depois.

## As 3 opções prontas

**1. Clássico** (o mais comum em escritórios brasileiros)
- Times New Roman 12, espaçamento 1,5, justificado. A4, margens 3 cm (superior e
  esquerda) e 2 cm (inferior e direita).
- Títulos: "CLÁUSULA PRIMEIRA – DO OBJETO", em negrito e caixa alta.
- Subitens "1.1", "1.2"; "Parágrafo único" quando houver só um.
- Qualificação das partes em parágrafo corrido.
- Rodapé: "Página X de Y". Assinaturas com local e data, linha, nome e CPF ou CNPJ, e duas
  testemunhas.

**2. Moderno** (mais fácil de ler na tela)
- Arial 11, espaçamento 1,15, alinhado à esquerda, 6 pt depois do parágrafo. A4, margens
  2,5 cm.
- Títulos: "1. Objeto", em negrito, sem caixa alta.
- Subitens "1.1", "1.1.1"; alíneas "(a)", "(b)".
- Quadro-resumo no início (partes, objeto, preço, prazo) e definições em cláusula
  própria.
- Rodapé: "Página X de Y". Assinaturas em tabela, com nome, cargo e CNPJ, e indicação de
  assinatura eletrônica.

**3. Compacto** (contratos longos ou para impressão)
- Calibri 10,5, espaçamento simples, justificado, 4 pt depois do parágrafo. A4, margens
  2 cm.
- Títulos: "1. OBJETO", em negrito e caixa alta.
- Subitens "1.1", "1.1.1"; alíneas "a)", "b)".
- Qualificação das partes em quadro.
- Cabeçalho com o título do contrato; rodapé "Página X de Y" e espaço para rubrica.

## Como aplicar

- **Todo documento** que o assistente cria para o advogado segue
  `_escritorio/formatacao.md`: minutas, aditivos, memorandos de revisão, cartas. A ficha do
  assunto pode trazer uma exceção (por exemplo, "usar o modelo da contraparte").
- **Minuta ou redline sobre um arquivo da contraparte:** mantenha a formatação do arquivo
  recebido. Formatação nova só no que o advogado redige do zero.
- **Com arquivo de referência:** crie o documento a partir dele (copie o arquivo e troque
  o conteúdo, mantendo os estilos), em vez de descrever o estilo do zero. É o caminho mais
  fiel. Se o arquivo e as regras em texto divergirem, valem as regras, que o advogado
  confirmou.
- **Por tipo de contrato:** se `formatacao.md` tiver uma regra para o tipo que você está
  redigindo, ela prevalece sobre a regra geral.
- **Sem arquivo de referência:** defina os estilos do documento (Normal, títulos, listas
  numeradas, margens, cabeçalho e rodapé), e não só a aparência de cada parágrafo. Assim o
  advogado consegue editar depois sem a formatação se desfazer.
- **Confira o arquivo gerado** antes de entregar: fonte, numeração e quebras. Se a
  ferramenta não conseguiu aplicar algum item (por exemplo, uma fonte que não está
  instalada, ou uma conversa na web que não gera `.docx`), diga qual, **uma vez**, e
  entregue.
- Não invente o que não está registrado. Item vazio: siga o arquivo de referência, se
  houver, ou a opção `[padrão]`.
- **Papel A4, sempre**, mesmo sem nada registrado. Sem essa regra, alguns assistentes
  geram o arquivo em papel Carta (padrão americano).
- **Numeração:** escreva os números no próprio texto ("1.1."), a menos que o arquivo de
  referência use a numeração automática do Word. A numeração automática some em alguns
  visualizadores (pré-visualização do celular ou do Mac, alguns editores na web).
- **Ao partir do arquivo de referência**, troque o que for só de exemplo (por exemplo, um
  cabeçalho com nome fictício) e limpe as propriedades herdadas: autor, empresa e a
  miniatura da primeira página, que pode mostrar o conteúdo do arquivo original.
- **Fontes:** o arquivo leva o nome da fonte, mas quem abre precisa tê-la instalada. Times
  New Roman e Arial existem em quase todo computador; Calibri vem com o Office; fontes
  menos comuns (Garamond, por exemplo) podem ser trocadas por outra na tela de quem não
  as tem. Se a fonte registrada for incomum, avise uma vez.
