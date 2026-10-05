# Case — Projeto Híbrido On-Premises, Cloud e SD-WAN

## Cenário
Empresa com Data Center local, matriz e filiais precisa integrar aplicações on-premises com workloads em Azure/AWS.

## Objetivo
Criar conectividade segura e resiliente entre usuários, filiais, Data Center e cloud.

## Arquitetura

```text
 Filial A ----\
               \
 Filial B ------ SD-WAN ----- Matriz / Data Center
               /                    |
 Filial C ----/               Firewall HA
                                    |
                         +----------+----------+
                         |                     |
                       Azure                  AWS
                       VNet                   VPC
```

## Tecnologias
- SD-WAN
- VPN IPsec
- BGP
- VLAN / VRF
- Azure VNet
- AWS VPC
- Transit Gateway
- ExpressRoute quando aplicável
- Firewalls
- Load Balancing
- DNS

## Fluxo de Projeto
1. Levantamento de aplicações
2. Planejamento IP
3. Segmentação
4. Definição de rotas
5. VPN/SD-WAN
6. Políticas de firewall
7. QoS
8. Testes de failover
9. Monitoramento
10. Documentação

## Segurança
- Segmentação LAN/WAN/Cloud
- VPN IPsec
- Firewall
- Menor privilégio
- Controle de acesso
- Logs
- Redundância

## Alta Disponibilidade
- Dois links nas filiais críticas
- SD-WAN
- Túneis redundantes
- Firewalls HA
- Redundância de gateways
- Failover testado

## Visão Gerencial
A decisão entre manter workloads localmente ou mover para cloud deve considerar:

- Latência
- Segurança
- Dependências
- Custo
- SLA
- Compliance
- Capacidade
- RTO/RPO

## Resultado Esperado
Uma arquitetura híbrida permite modernizar gradualmente a infraestrutura sem exigir migração total imediata, mantendo conectividade e continuidade entre ambientes.

## Resposta para entrevista
> Em projetos híbridos, eu integro rede corporativa, Data Center e cloud utilizando SD-WAN, VPN IPsec e BGP. Trabalho com segmentação, políticas de segurança, redundância e testes de failover. Também avalio quais aplicações devem permanecer on-premises e quais podem ir para Azure ou AWS considerando latência, segurança, custo e disponibilidade.
