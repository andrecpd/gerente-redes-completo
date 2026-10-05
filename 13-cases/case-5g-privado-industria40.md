# Case — Rede 5G Privada para Indústria 4.0

## Cenário
Projeto de conectividade privada para ambiente industrial, com necessidade de mobilidade, baixa latência, disponibilidade e maior controle sobre dispositivos e aplicações da planta.

## Objetivo
Utilizar uma rede móvel privada 4G/5G para suportar aplicações de **Indústria 4.0**, integrando equipamentos industriais, sensores, sistemas de automação e plataformas de TI.

## Casos de Uso
- Sensores IoT
- AGVs e veículos autônomos
- Tablets industriais
- Câmeras
- Telemetria
- Automação de processos
- Manutenção remota
- Comunicação de máquinas
- Aplicações críticas de baixa latência

## Arquitetura

```text
        Dispositivos / Máquinas / IoT
                    |
                 4G / 5G
                    |
                  RAN
                    |
              Private Core
                    |
           Rede IP Industrial
              /          \
          OT / PLC      TI / Data Center
                           |
                      Cloud / Analytics
```

## Componentes
- RAN 4G/5G
- Core móvel privado
- SIM/eSIM
- Rede IP
- VLANs / VRFs
- Firewalls
- QoS
- Edge Computing quando aplicável
- Integração OT/IT
- Cloud

## Segurança
- Autenticação por SIM/eSIM
- Segmentação
- Firewall entre OT e TI
- Controle de acesso
- Políticas de menor privilégio
- Monitoramento
- Logs

## QoS e Criticidade
Aplicações industriais podem possuir requisitos diferentes.

Exemplo:

| Aplicação | Prioridade |
|---|---|
| Controle industrial | Crítica |
| AGV | Alta |
| Vídeo | Média/Alta |
| Telemetria | Média |
| Acesso administrativo | Normal |

## Atuação Técnica
- Planejamento de cobertura
- Integração da RAN com a rede IP
- Segmentação
- Roteamento
- Segurança
- QoS
- Validação de latência e disponibilidade
- Troubleshooting entre rede móvel e infraestrutura IP

## Visão Gerencial
Avaliar:

- Casos de uso
- Cobertura
- Disponibilidade
- SLA
- Segurança OT/IT
- CAPEX/OPEX
- Escalabilidade
- Fornecedor
- Continuidade operacional

## Resultado Esperado
Oferecer conectividade privada e controlada para aplicações industriais, permitindo maior mobilidade, automação, visibilidade e suporte à transformação digital da planta.

## Resposta para entrevista
> Tenho experiência e conhecimento em projetos de redes privadas 4G/5G voltadas à Indústria 4.0. Nesse tipo de ambiente, considero cobertura da RAN, integração com o core e rede IP, segmentação entre OT e TI, segurança, QoS, latência e disponibilidade. O objetivo é suportar aplicações como IoT, AGVs, telemetria e automação industrial com maior controle e previsibilidade do que uma rede pública convencional.
