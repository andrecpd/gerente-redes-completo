# Case — Arquitetura Cloud Híbrida e Multicloud

## Cenário
Integração entre Data Center/on-premises e ambientes de nuvem pública, utilizando Azure e AWS.

## Objetivo
Garantir comunicação segura, redundante e escalável entre redes locais e cloud, permitindo migração gradual de aplicações sem interromper os serviços existentes.

## Arquitetura

```text
                On-Premises / Data Center
                         |
                  Firewall / SD-WAN
                    /           \
             VPN IPsec       Link Dedicado
                |                |
              Azure             AWS
              VNet              VPC
                |                |
           ExpressRoute     Transit Gateway
                \              /
                 \            /
                 Integração Multicloud
```

## Tecnologias
- Azure VNet
- AWS VPC
- VPN Site-to-Site IPsec
- BGP
- ExpressRoute
- Transit Gateway
- Route Tables / UDR
- Firewalls
- SD-WAN
- DNS
- Load Balancing

## Segurança
- Segmentação por sub-redes
- Firewalls
- VPN IPsec
- Controle de rotas
- Princípio de menor privilégio
- Logs e monitoramento
- Redundância de túneis

## Atuação Técnica
- Planejamento de endereçamento IP
- Definição de rotas
- Configuração de VPNs
- Integração BGP
- Validação de conectividade
- Troubleshooting de rotas e políticas
- Testes de failover

## Visão Gerencial
Avaliar:

- Disponibilidade
- Segurança
- Desempenho
- Latência
- Custo mensal
- Dependência de fornecedor
- Crescimento
- Continuidade do negócio

## Resultado Esperado
Criar uma arquitetura híbrida que permita manter sistemas críticos on-premises enquanto aplicações e serviços são migrados ou integrados à nuvem de forma controlada.

## Resposta para entrevista
> Em um projeto híbrido, eu começo pelo endereçamento, segmentação e requisitos de segurança. Depois defino a conectividade entre on-premises e cloud usando VPN IPsec ou links dedicados, com BGP para troca de rotas. Em ambientes Azure e AWS, considero VNet, VPC, ExpressRoute, Transit Gateway, firewalls e redundância. Como gestor, também avalio custo, SLA, risco e dependência de fornecedor.
