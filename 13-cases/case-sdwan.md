# Case — SD-WAN, QoS e Voz

## Cenário
Usuários relatam cortes e atraso em Teams/VoIP enquanto aplicações web continuam funcionando normalmente.

## Hipótese
Aplicações em tempo real são mais sensíveis a:

- Latência
- Jitter
- Perda de pacotes
- Congestionamento

## Diagnóstico
Comparar os dois links de WAN:

- Latência
- Jitter
- Perda
- Utilização
- Drops
- Disponibilidade

## Ação
- Revisar QoS
- Classificar tráfego de voz
- Aplicar marcação DSCP
- Configurar filas prioritárias
- Revisar SD-WAN Path Preference
- Definir thresholds de SLA
- Testar failover

## Arquitetura

```text
                 Filial
                   |
              Firewall/SD-WAN
               /          \
          Link ISP-A     Link ISP-B
              |             |
              +----- Internet -----+
                       |
                 Teams / VoIP
```

## Resultado Esperado
O tráfego de voz utiliza automaticamente o caminho com melhor qualidade, reduzindo cortes e degradação durante problemas em um dos links.

## Resposta para entrevista
> Em um cenário de voz sobre SD-WAN, eu comparo latência, jitter e perda entre os links. Depois reviso QoS, classificação, DSCP e políticas de path preference. O objetivo é fazer o tráfego de voz utilizar o melhor caminho e executar failover quando os indicadores ultrapassarem os limites definidos.
