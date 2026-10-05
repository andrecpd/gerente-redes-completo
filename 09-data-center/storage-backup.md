# Storage e Backup

Storage e backup são componentes críticos para disponibilidade, desempenho e continuidade dos serviços de Data Center.

## Tipos de Storage

### DAS
Storage conectado diretamente ao servidor.

### NAS
Storage acessado pela rede, normalmente usando:

- NFS
- SMB

### SAN
Rede dedicada de armazenamento, utilizando tecnologias como:

- Fibre Channel
- iSCSI

## RAID

RAID pode melhorar disponibilidade e/ou desempenho.

| RAID | Característica |
|---|---|
| RAID 1 | Espelhamento |
| RAID 5 | Paridade distribuída |
| RAID 6 | Dupla paridade |
| RAID 10 | Espelhamento + distribuição |

A escolha depende de capacidade, desempenho, tolerância a falhas e custo.

## Multipath

O Multipath permite múltiplos caminhos entre servidores e storage.

```text
Server
 |   \
 |    \
SAN-A SAN-B
 |     |
Storage Controllers
```

Benefícios:

- Redundância
- Failover
- Maior disponibilidade

## Indicadores de Storage

Acompanhar:

- Capacidade utilizada
- IOPS
- Latência
- Throughput
- Cache
- Falhas de disco
- Utilização de controladoras

## Backup

O backup protege contra:

- Falha de hardware
- Erro humano
- Exclusão acidental
- Corrupção
- Ransomware
- Desastres

## Regra 3-2-1

```text
3 copias dos dados
2 tipos de midia
1 copia externa
```

Quando aplicável, também considerar cópias imutáveis e isoladas.

## Tipos de Backup

- Full
- Incremental
- Diferencial
- Snapshot

Snapshots não devem ser tratados automaticamente como substitutos de backup independente.

## RPO e RTO

### RPO
Quanto de dados a organização aceita perder.

### RTO
Quanto tempo o serviço pode permanecer indisponível.

## Teste de Restore

Backup só é confiável quando a restauração é validada periodicamente.

Testar:

- Integridade
- Tempo de restauração
- Aplicação
- Banco de dados
- Máquinas virtuais
- Configurações

## Visão Gerencial

Acompanhar:

- Taxa de sucesso de backup
- Falhas de jobs
- Tempo de restore
- Capacidade
- Retenção
- RPO
- RTO
- Custos de storage
- CAPEX/OPEX

## Resposta para entrevista

> Em storage e backup, avalio capacidade, desempenho, redundância e continuidade. Dependendo do ambiente, posso trabalhar com SAN, NAS ou storage local, além de multipath e RAID. Para backup, considero políticas de retenção, regra 3-2-1, proteção externa e testes periódicos de restore. Também alinho RPO e RTO com a criticidade do negócio.
