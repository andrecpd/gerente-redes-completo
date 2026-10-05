# Arquitetura de Data Center

Uma arquitetura de Data Center deve ser planejada considerando **alta disponibilidade, segurança, capacidade, escalabilidade, redundância e continuidade do negócio**.

## Principais componentes

- Rede LAN e Data Center
- Switching e Routing
- Firewalls e balanceadores
- Servidores físicos e virtualizados
- Storage
- Backup
- Segurança
- Energia, UPS e geradores
- Climatização
- Cabeamento estruturado
- Monitoramento e observabilidade
- Disaster Recovery

## Arquitetura de rede

O desenho deve evitar **Single Points of Failure (SPOF)**.

```text
                    Internet / WAN
                         |
                  +---------------+
                  | Firewalls HA  |
                  +-------+-------+
                          |
                 +--------+--------+
                 |                 |
              CORE-01           CORE-02
                 |                 |
           +-----+-----+     +-----+-----+
           |           |     |           |
       ACCESS-01   ACCESS-02 ACCESS-03 ACCESS-04
           |           |     |           |
        Servers      Storage     Virtualização
```

Em ambientes modernos, uma arquitetura **Spine-Leaf** pode melhorar escalabilidade e previsibilidade de tráfego.

## Alta disponibilidade

### Rede
- Core redundante
- Uplinks redundantes
- LACP
- vPC/MLAG quando aplicável
- ECMP
- Convergência rápida

### Segurança
- Firewalls em HA
- Redundância WAN
- Segmentação
- Políticas centralizadas

### Servidores
- Cluster
- NIC Teaming/Bonding
- Hypervisors redundantes

### Storage
- Controladoras redundantes
- Multipath
- RAID
- Replicação

### Energia
- Alimentação A/B
- UPS
- Banco de baterias
- Geradores

## Segmentação

Exemplo:

```text
VLAN 10 - Management
VLAN 20 - Servidores
VLAN 30 - Banco de Dados
VLAN 40 - Aplicações
VLAN 50 - Backup
VLAN 60 - Storage
VLAN 70 - DMZ
```

A segmentação melhora segurança, troubleshooting, controle de acesso e gestão de mudanças.

## Segurança

- Firewalls
- ACLs
- IDS/IPS
- NAC
- MFA
- Menor privilégio
- Logs e SIEM
- Patching
- Gestão de vulnerabilidades
- Backup

## Capacity Planning

Acompanhar:

- CPU
- Memória
- Storage
- IOPS
- Interfaces
- Banda
- Energia
- Espaço em rack
- Portas de switches

## Monitoramento

### Rede
- Disponibilidade
- Latência
- Jitter
- Perda
- Utilização
- Erros e drops

### Servidores
- CPU
- Memória
- Disco
- Interfaces

### Infraestrutura
- Temperatura
- Umidade
- Energia
- UPS e geradores

## Disaster Recovery

Uma estratégia de continuidade pode incluir:

- Backup local
- Backup externo
- Replicação
- Segundo Data Center
- Cloud
- Site de contingência

### RPO
**Recovery Point Objective:** quanto de dados a empresa pode perder.

### RTO
**Recovery Time Objective:** quanto tempo o serviço pode ficar indisponível.

## Visão Gerencial

```text
Disponibilidade
      ↓
Capacidade
      ↓
Segurança
      ↓
Risco
      ↓
SLA
      ↓
CAPEX / OPEX
      ↓
Continuidade do negócio
```

## Resposta para entrevista

> Para projetar um Data Center, começo entendendo os requisitos de disponibilidade, capacidade, segurança e crescimento. Depois estruturo redundância de rede, energia, servidores e storage, evitando pontos únicos de falha. Também considero segmentação, firewalls, backup, monitoramento e Disaster Recovery. Como gestor, acompanho capacidade, SLA, riscos, CAPEX e OPEX para garantir que a infraestrutura suporte o crescimento do negócio.
