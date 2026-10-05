# Servidores e Infraestrutura

Servidores são componentes fundamentais do Data Center e precisam ser integrados corretamente à rede, storage, segurança, backup e virtualização.

O objetivo é garantir **disponibilidade, desempenho, segmentação e redundância**.

## Servidores físicos

Um servidor pode possuir:

- CPU
- Memória RAM
- Discos
- Interfaces de rede
- Fontes redundantes
- Controladora RAID
- Interface de gerenciamento

Exemplos de gerenciamento remoto:

- iLO
- iDRAC
- CIMC

## Redundância de rede

Servidores críticos devem utilizar múltiplas interfaces quando possível.

```text
              Switch-01
                 |
               NIC-01
                 |
              Server
                 |
               NIC-02
                 |
              Switch-02
```

Tecnologias:

- NIC Teaming
- Bonding
- LACP

## VLANs

Exemplo de segmentação:

```text
VLAN 10 - Management
VLAN 20 - Aplicacao
VLAN 30 - Banco de Dados
VLAN 40 - Backup
VLAN 50 - Storage
```

## Virtualização

Plataformas comuns:

- VMware
- Hyper-V
- KVM

```text
             Servidor Fisico
                    |
              Hypervisor
          +---------+---------+
          |         |         |
        VM-01     VM-02     VM-03
        WEB        APP        DB
```

## Cluster

Benefícios:

- Alta disponibilidade
- Failover
- Balanceamento
- Manutenção com menor impacto
- Mobilidade de workloads

## Storage

Opções:

- SAN
- NAS
- Storage local

Protocolos comuns:

- Fibre Channel
- iSCSI
- NFS
- SMB

Também considero:

- Multipath
- RAID
- IOPS
- Latência
- Capacidade

## Load Balancer

```text
               Usuarios
                   |
             Load Balancer
              /    |    \
          WEB-01 WEB-02 WEB-03
```

Benefícios:

- Alta disponibilidade
- Escalabilidade
- Distribuição de carga
- Health Checks

## Backup

Estratégia 3-2-1:

```text
3 copias dos dados
2 tipos de midia
1 copia externa
```

Além de fazer backup, é fundamental testar a restauração.

## Monitoramento

Acompanhar:

- CPU
- Memória
- Disco
- Interfaces
- Temperatura
- Processos
- Disponibilidade
- Latência
- IOPS

## Capacity Planning

```text
CPU / Memoria / Storage / Rede / IOPS
                ↓
             Historico
                ↓
             Forecast
                ↓
             Expansao
```

## Troubleshooting

Sequência sugerida:

1. Estado do servidor
2. Interface física
3. NIC
4. VLAN
5. Gateway
6. Roteamento
7. Firewall
8. DNS
9. Aplicação
10. Storage

## Segurança

- Segmentação
- Firewall
- Controle de acesso
- Patching
- EDR
- Logs
- Backup
- Rede de gerenciamento separada

## Visão Gerencial

Acompanhar:

- Disponibilidade
- Capacidade
- Incidentes
- MTTR
- Lifecycle
- Garantia
- Contratos de suporte
- CAPEX
- OPEX

## Resposta para entrevista

> Tenho experiência com ambientes de servidores físicos e virtualizados integrados à infraestrutura de rede. Na parte de redes, considero VLANs, redundância de interfaces, NIC Teaming, conectividade com switches, storage e balanceadores. Também considero backup, monitoramento, capacidade e alta disponibilidade para reduzir pontos únicos de falha e melhorar a continuidade dos serviços.
