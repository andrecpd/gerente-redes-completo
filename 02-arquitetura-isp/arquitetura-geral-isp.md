# Arquitetura Geral de ISP

Uma arquitetura ISP deve equilibrar disponibilidade, capacidade, escalabilidade, simplicidade operacional, segurança e custo.

## Camadas
- Acesso: FTTH/GPON/XGS-PON
- Agregação: switches/routers de distribuição
- Backbone: IP/MPLS ou Segment Routing
- Borda: BGP, trânsito IP, IX/peering
- Serviços: CGNAT, DNS, DHCP, AAA, segurança
- Observabilidade: NMS, telemetria, logs e alertas

## Critérios de desenho
Redundância, convergência rápida, crescimento modular, ausência de SPOF, documentação e capacidade planejada.