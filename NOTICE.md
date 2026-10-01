# Créditos e licença

Este método é mantido pela Capi (capi.legal).

Partes das instruções e rotinas foram **adaptadas** do projeto **claude-for-legal**, da
Anthropic (https://github.com/anthropics/claude-for-legal), plugin `commercial-legal`.
O projeto é distribuído sob a **Licença Apache 2.0**. Uma cópia da licença está em
`LICENSE`.

## O que foi adaptado e como

| Arquivo desta pasta | Baseado em (claude-for-legal) | Modificações |
|---|---|---|
| `AGENTS.md` | `commercial-legal/CLAUDE.md` (regras comuns, formato de entrega, confiança em conteúdo recuperado, proporcionalidade, leitura de documentos grandes) e `skills/matter-workspace` | Traduzido; adaptado à advocacia brasileira de contratos; reorganizado como instruções universais para qualquer assistente; pastas de cliente visíveis em vez de configuração oculta; regras de sigilo entre clientes |
| `rotinas/configurar.md` | `skills/cold-start-interview` | Reduzido a 6 perguntas (cerca de 2 minutos); lado do cliente no formato contratante/contratado; aprendizado opcional com os contratos do advogado |
| `rotinas/revisar-contrato.md` | `skills/vendor-agreement-review`, `skills/nda-review`, `skills/review` | Posições por lado; gravidade simplificada; pontos de direito brasileiro; sem rota de aprovação corporativa |
| `rotinas/comparar-versoes.md` | `skills/amendment-history` | Acrescentada a comparação de rodadas de negociação e a detecção de mudanças não anunciadas |
| `rotinas/resumo-para-cliente.md` | `skills/stakeholder-summary` | Voltado ao cliente do advogado; formatos WhatsApp e e-mail |
| `rotinas/datas-do-contrato.md` | `skills/renewal-tracker` | Registro em arquivo comum; regra de mostrar a conta e conferir |
| `estrutura/_escritorio/posicoes.md` | Seção "Playbook" do perfil de prática | Cláusulas e posições padrão do mercado brasileiro; coluna de origem anonimizada |

Os guias (`guias/`), os modelos (`modelos/`), a estrutura da pasta do advogado
(`estrutura/`), o bloco de configuração (`configuracao/`), as regras de sigilo entre
clientes e a integração com a Capi foram escritos pela Capi.

Este material não é parecer jurídico. As referências legais dos guias devem ser conferidas
antes do uso.
