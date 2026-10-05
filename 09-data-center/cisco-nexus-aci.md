# Cisco Nexus e Cisco ACI

Cisco Nexus e Cisco ACI são soluções voltadas a redes de Data Center com foco em **alta disponibilidade, desempenho, automação, segmentação e escalabilidade**.

# Cisco Nexus

Os switches Cisco Nexus podem atuar em:

- Core
- Aggregation
- Leaf
- Spine
- Top of Rack

## Tecnologias importantes

### vPC — Virtual Port Channel

Permite que dois switches Nexus forneçam conectividade redundante e ativa para equipamentos conectados.

```text
          Nexus-01 -------- Nexus-02
             |                 |
             |------ vPC ------|
                    |
                 Server
```

Benefícios:

- Redundância
- Utilização ativa de links
- Maior disponibilidade
- Menor dependência de STP em cenários compatíveis

### VXLAN

VXLAN permite construir redes Layer 2 sobre uma infraestrutura Layer 3.

Benefícios:

- Escalabilidade
- Segmentação
- Mobilidade de workloads
- Melhor utilização da infraestrutura IP

# Cisco ACI

O **Application Centric Infrastructure (ACI)** utiliza uma fabric Spine-Leaf baseada em políticas.

```text
                  APIC Cluster
                       |
              +--------+--------+
              |                 |
          Spine-01          Spine-02
          /      \          /      \
      Leaf-01  Leaf-02  Leaf-03  Leaf-04
         |        |        |        |
      Servers   Apps     Firewall  Storage
```

## APIC

O **Application Policy Infrastructure Controller** centraliza o gerenciamento da fabric.

Permite configurar:

- Tenants
- VRFs
- Bridge Domains
- EPGs
- Contracts
- Políticas

## Tenant

Cria separação lógica da infraestrutura.

Exemplos:

```text
Tenant-Producao
Tenant-Homologacao
Tenant-Desenvolvimento
```

## VRF

Mantém tabelas de roteamento separadas.

```text
VRF-PRODUCAO
VRF-DMZ
VRF-MGMT
```

## Bridge Domain

Define comportamento Layer 2/Layer 3 para grupos de endpoints.

## EPG — Endpoint Group

Agrupa endpoints com políticas semelhantes.

```text
EPG-WEB
EPG-APP
EPG-DATABASE
```

## Contracts

Controlam a comunicação entre EPGs.

```text
WEB
 |
 | HTTPS
 ↓
APP
 |
 | TCP específico
 ↓
DATABASE
```

## Benefícios do ACI

- Automação
- Gerenciamento centralizado
- Segmentação
- Microsegmentação
- Escalabilidade
- Padronização
- Visibilidade

## Nexus tradicional x ACI

| Nexus tradicional | ACI |
|---|---|
| Configuração por dispositivo | Configuração centralizada |
| VLANs | EPGs |
| ACLs | Contracts |
| CLI | APIC |
| Mais configuração manual | Políticas e automação |

## Troubleshooting

Verificar:

- Interfaces
- vPC
- VLANs
- VXLAN
- BGP EVPN quando aplicável
- Endpoints
- EPGs
- Contracts
- Faults no APIC

## Visão Gerencial

Avaliar adoção considerando:

- Escala do Data Center
- Necessidade de automação
- Segurança
- Treinamento da equipe
- Compatibilidade
- CAPEX
- OPEX
- Suporte

## Resposta para entrevista

> Tenho conhecimento de ambientes Cisco Nexus usados em Data Center, com foco em switching, alta disponibilidade e redundância. No Cisco ACI, a arquitetura utiliza uma fabric Spine-Leaf gerenciada pelo APIC e baseada em políticas, usando conceitos como Tenant, VRF, Bridge Domain, EPG e Contracts. O benefício é tornar a operação mais centralizada, automatizada, segmentada e escalável.
