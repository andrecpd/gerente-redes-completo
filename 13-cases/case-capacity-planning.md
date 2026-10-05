# Case — Capacity Planning de Backbone

## Cenário
Backbone apresentando crescimento contínuo de tráfego e utilização próxima do limite operacional seguro.

## Desafio
Evitar saturação, perda de pacotes e impacto no SLA antes que o crescimento da base de clientes comprometa a qualidade do serviço.

## Análise
Avaliar:

- Histórico de utilização
- Pico de tráfego
- Percentil 95
- Crescimento mensal
- Headroom disponível
- Redundância
- Capacidade dos equipamentos
- Lead time de fornecedores
- Crescimento comercial

## Alternativas
- Upgrade de interfaces
- Novo link
- Novo fornecedor
- ECMP
- Redistribuição de tráfego
- Novo POP
- Expansão de backbone
- Traffic Engineering

## Visão Gerencial
Comparar cada alternativa considerando:

- CAPEX
- OPEX
- Prazo
- Risco
- SLA
- Escalabilidade
- Vida útil da solução

## KPIs
- Utilização do backbone
- Percentil 95
- Crescimento de tráfego
- Headroom
- Latência
- Perda
- Forecast de saturação

## Resultado Esperado
Realizar a expansão antes da saturação, garantindo capacidade para crescimento e reduzindo risco operacional.

## Resposta para entrevista
> Em Capacity Planning, eu utilizo histórico de tráfego, percentil 95 e projeção de crescimento para identificar quando um recurso poderá atingir níveis críticos. A partir disso comparo upgrade, novos links, fornecedores ou redesign considerando CAPEX, OPEX, prazo e risco, para ampliar a capacidade antes de existir impacto no cliente.
