# Contexto: Armac CRM & Growth

## Quem sou eu
- **Nome:** Guilherme Souza (Gui)
- **Papel:** Coordenador de CRM
- **Email:** guilherme.souza@armac.com.br
- **HubSpot Owner ID:** 2048492741
- **HubSpot Hub ID:** 8112947
- **Plano:** Claude Team · ARMAC-BR-SA

---

## A empresa

**Armac** é uma empresa B2B de locação de equipamentos pesados e venda de máquinas seminovas. Fundada há 30+ anos, capital aberto há ~5 anos.

---

## Estrutura de negócios (BUs)

### SPOT (Locação)
| Pipeline | Pipeline ID | Perfil |
|---|---|---|
| Rental Varejo | `801631254` | Ticket menor, locações a partir de 3 dias, esmagadoramente inbound, qualificados por SDRs |
| Locação de Equipamentos | `11389336` | Ticket maior, locações acima de 1 mês, caráter relacional e outbound. Inbounds com RRM > R$200K |
| Grandes Contas | `17385600` | Puramente outbound, carteira controlada, perfil corporativo |

### BUs de Longo Prazo
Ciclo longo, contratos de 12–48+ meses, ticket altíssimo, majoritariamente outbound. Podem incluir aluguel de mão de obra (operadores e mecânicos).
- Pipeline unificado: **Operações Contínuas** (`20204429`)
- BUs: Agroindústria/Indústria/Siderurgia, Portos/Terminais/Ferrovias, Mineração, Empilhadeiras (`2135392`)

**Territórios:**
- T1 = Sul
- T2 = SP
- T3 = MG, RJ, ES
- T4 = Centro-Oeste + TO
- T5 = Norte + MA
- T6 = Nordeste - MA

### Seminovos
| Pipeline | Pipeline ID |
|---|---|
| Seminovos | `3471619` |

Venda de máquinas pesadas usadas. Atende PF e PJ. Lojas em expansão: 15 lojas em 2025, meta de 18 em 2026. Meta de faturamento: R$500M.

---

## Propriedades-chave de deals no HubSpot

| O que eu digo | Propriedade HubSpot |
|---|---|
| Vendedor, consultor, proprietário do negócio | `hubspot_owner_id` |
| RRM, receita recorrente mensal, valor da locação | `hs_mrr` |
| Inbound / Outbound / Origem | `origem_do_negocio_2` |
| Fechado, aberto, perdido | `status_do_negocio` |
| Cidade da entrega | `cidade_da_entrega` |
| Estado da entrega, UF | `estado_da_entrega` |

### Valores válidos — `status_do_negocio`
- `"Aberto"`
- `"Fechado"`
- `"Perdido"`

### Valores válidos — `origem_do_negocio_2`
- `"Inbound"`
- `"Outbound"`
- `"Outbound com lead Inbound"`
- `"Inbound com lead Outbound"`

---

## Regras críticas para consultas HubSpot

1. **Timestamps sempre calculados via Python** antes de executar qualquer consulta com filtro de data. Nunca calcular mentalmente. Timezone: BRT (UTC-3) → converter para UTC em milissegundos.
2. **Consultas separadas por pipeline** quando precisar de contagens individuais — consultas combinadas produzem erros de contagem.
3. **HubSpot MCP é exclusivo para dados de CRM** — nunca usar para informações externas ao CRM.

---

## Subsidiárias em onboarding no HubSpot
- **Engelog** — Plano Pro, onboarding quase completo
- **Termov** — Plano Starter, em andamento
- **Braslift** — Ainda não iniciado

---

## Ferramentas do ecossistema
- **HubSpot Enterprise** — CRM principal (Hub ID: 8112947)
- **Blip** — Entrega de notificações WhatsApp
- **SAP** — Fonte de dados de faturamento e carteirização (integração com HubSpot planejada)
- **Lovable + Supabase** — Desenvolvimento de apps internos (CRM Calendar, Seminovos Geolocation, Gifts Management)
- **GitHub Desktop** — Controle de versão
- **Microsoft Power Automate + Forms** — Sistema interno de tickets (pipeline `885603374`)

---

## Pessoas-chave
- **Vinicius** — Gestor direto do Gui
- **Fernando** — Presidente da empresa. Ritmo acelerado, reage mal a timelines conservadoras. Comunicação: direta, objetiva, sem rodeios.
- **Daniela** — Coordenadora de pré-vendas

---

## Preferências de trabalho
- Soluções nativas no HubSpot sempre que possível (workflows, listas, propriedades)
- Não usar n8n
- Validar lógica end-to-end antes de gerar qualquer output
- Linguagem: português brasileiro
- Abordagem iterativa: discutir → validar → ajustar → executar
