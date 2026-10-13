# Configuração

Onde ficam as coisas e como cada assistente trabalha nesta pasta. É preenchida pela
configuração inicial (`rotinas/configurar.md`, no método).

O assistente lê este arquivo no início de cada sessão. Você pode editar à vontade.

**Configurado em:** [preencher]
**Método:** https://raw.githubusercontent.com/capi-legal/metodo-advogados/main/AGENTS.md. Versão ao configurar: [preencher]

---

## Pasta de trabalho

A pasta fica **no computador**. Ela pode estar sincronizada com uma nuvem, que dá cópia
fora do computador e acesso pela web e pelo celular.

- **Caminho no computador:** [preencher, ex.: ~/Library/CloudStorage/GoogleDrive-.../Meu Drive/Escritório IA]
- **Nome da pasta:** [preencher, ex.: Escritório IA]
- **Sincronizada com:** [Google Drive | OneDrive | Dropbox | nenhuma | outro]
- **Arquivos baixados no computador?** [sim: Drive "espelhar" ou "disponível off-line";
  OneDrive "Sempre manter neste dispositivo"; Dropbox "Disponibilizar off-line" | não]
- **Link da pasta na nuvem:** [preencher | sem nuvem]

  Serve para a web e o celular. O link é mais seguro que o nome, porque pode haver mais
  de uma pasta com o mesmo nome.
- **Pasta de clientes:** [padrão: `clientes/` dentro desta pasta]. Se você já tem pastas
  de clientes em outro lugar, indique aqui.
- **Pastas antigas:** [adaptar no lugar (padrão) | data de corte AAAA-MM-DD, material
  antigo em `_legado/`]. As duas opções estão em `estrutura/LEIA-ME.md`, no método.

## Formato dos arquivos

- **Registros** (configuração, perfil, posições, índices, ficha, histórico): `.md`.
- **Contratos e entregas:** [padrão: `.docx` para contratos, `.md` para notas internas].
  Nunca Google Docs nativo: no computador ele aparece só como atalho, e o assistente não
  lê.

## Assistentes e acesso

Preenchido com o teste feito na configuração. "Completo" significa ler, criar e editar,
inclusive `.docx`.

| Assistente | Onde roda | Como chega à pasta | Acesso testado | Data do teste |
|---|---|---|---|---|
| [ex.: Claude (Cowork)] | [computador] | [pasta no computador] | [completo] | [AAAA-MM-DD] |
| [ex.: ChatGPT] | [celular] | [conector Google Drive] | [ler e criar `.md`; não salva `.docx`] | [AAAA-MM-DD] |

Pela web ou pelo celular, o assistente segue `AGENTS.md` §10: registros em arquivos novos
com data, e contratos `.docx` salvos pelo advogado.

## Conectores

- **E-mail:** [nenhum | Gmail | Outlook]
- **Assinatura eletrônica:** [nenhum | Clicksign | D4Sign | ZapSign | DocuSign | gov.br]
- **Agenda:** [nenhum | Google Agenda | Outlook]
- **Capi:** [não conectado | conectado em AAAA-MM-DD]

## Sigilo

- **Plano de cada assistente:** [preencher]. Recomendado: plano pago com uso dos dados
  para treinamento desativado.
- **Memória entre conversas:** [ligada | desligada]. Se ligada, o assistente não guarda
  nela fatos de clientes.
