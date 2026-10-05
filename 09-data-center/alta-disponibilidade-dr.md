# Alta Disponibilidade e Disaster Recovery

Alta disponibilidade e Disaster Recovery têm objetivos complementares.

- **Alta Disponibilidade (HA):** reduzir interrupções durante falhas locais.
- **Disaster Recovery (DR):** recuperar serviços após eventos graves que afetem o ambiente principal.

## Alta Disponibilidade

A arquitetura deve eliminar ou reduzir pontos únicos de falha.

### Rede
- Switches redundantes
- Links redundantes
- LACP/vPC/MLAG
- ECMP
- Roteamento dinâmico

### Segurança
- Firewalls em HA
- Balanceadores redundantes

### Servidores
- Clusters
- Hypervisors redundantes
- Failover

### Storage
- Controladoras redundantes
- Multipath
- RAID
- Replicação

### Energia
- Alimentação A/B
- UPS
- Geradores

## Disaster Recovery

Um plano de DR deve responder:

- Quais serviços são críticos?
- Qual prioridade de recuperação?
- Qual RPO?
- Qual RTO?
- Onde estão os backups?
- Existe replicação?
- Existe site secundário?
- Quem são os responsáveis?
- Como será feita a comunicação?

## Arquitetura básica

```text
          Data Center Principal
                  |
             Replicacao
                  |
          Data Center DR / Cloud
```

## Estratégias

### Active/Active
Dois ambientes operam simultaneamente.

Vantagens:
- Menor tempo de interrupção
- Melhor utilização de recursos

Desvantagens:
- Maior custo
- Maior complexidade

### Active/Passive
O ambiente secundário assume em caso de falha.

Vantagens:
- Menor custo

Desvantagens:
- Maior tempo de ativação
- Necessidade de testes frequentes

## RPO e RTO

### RPO
Define o máximo aceitável de perda de dados.

### RTO
Define o máximo aceitável de tempo para recuperação.

## Runbook de DR

O plano deve documentar:

1. Critérios para declarar desastre
2. Responsáveis
3. Sequência de recuperação
4. Dependências entre sistemas
5. Procedimentos de failover
6. Validação
7. Comunicação
8. Retorno ao ambiente principal

## Testes

Realizar testes periódicos:

- Failover de links
- Failover de firewalls
- Failover de servidores
- Restore de backup
- Ativação do site DR
- Teste de comunicação

## Indicadores

- Disponibilidade
- MTTR
- RPO atingido
- RTO atingido
- Sucesso de backup
- Sucesso de restore
- Tempo de failover
- Incidentes críticos

## Visão Gerencial

O nível de redundância deve ser proporcional ao impacto do serviço.

```text
Criticidade
    ↓
Impacto financeiro
    ↓
RPO / RTO
    ↓
Arquitetura HA / DR
    ↓
CAPEX / OPEX
    ↓
Plano de continuidade
```

## Resposta para entrevista

> Para estruturar alta disponibilidade, primeiro identifico os serviços críticos e os pontos únicos de falha. Depois defino redundância de rede, segurança, servidores, storage e energia. Para Disaster Recovery, alinho RPO e RTO com o negócio, defino estratégia de replicação e backup, site secundário ou cloud, runbooks e testes periódicos. O objetivo é reduzir tanto a probabilidade de indisponibilidade quanto o tempo necessário para recuperar o serviço.
