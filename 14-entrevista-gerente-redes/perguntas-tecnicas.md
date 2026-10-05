# Perguntas Técnicas de Entrevista — Gerente de Redes e Telecomunicações

## 1. Como você desenharia um backbone ISP redundante?

Eu começaria definindo os requisitos de capacidade, disponibilidade, crescimento, número de POPs e criticidade dos serviços.

A arquitetura deveria evitar pontos únicos de falha, utilizando:

- Dois ou mais equipamentos de core quando necessário
- Links físicos por caminhos distintos
- Redundância de operadoras ou trânsito IP
- BGP para conectividade externa
- OSPF ou IS-IS no IGP
- MPLS ou Segment Routing no backbone
- ECMP para utilização de múltiplos caminhos
- BFD para detecção rápida de falhas
- Proteção de energia e infraestrutura nos POPs
- Monitoramento de latência, perda e utilização

Também avaliaria capacidade atual e crescimento futuro para evitar que a redundância exista apenas fisicamente, mas não tenha capacidade suficiente para absorver o tráfego em uma falha.

O objetivo é garantir que a perda de um link, roteador ou POP não provoque indisponibilidade generalizada.

---

## 2. Como BGP e OSPF se complementam?

O OSPF normalmente é utilizado como protocolo de roteamento interno da rede.

Ele oferece:

- Convergência rápida
- Conhecimento da topologia interna
- Cálculo de melhor caminho baseado em custo
- Distribuição de rotas entre roteadores do backbone

O BGP é utilizado principalmente para:

- Comunicação com outros sistemas autônomos
- Internet Transit
- Peering
- Multihoming
- Controle de política de roteamento

Em uma arquitetura ISP, o OSPF pode transportar a conectividade interna entre os roteadores enquanto o BGP controla a distribuição de rotas de clientes, serviços e Internet.

Em ambientes maiores, também podemos utilizar iBGP com Route Reflectors para melhorar a escalabilidade.

---

## 3. Como dimensionar uma expansão FTTH?

Primeiro avalio a demanda atual e prevista da região.

Analiso:

- Quantidade de clientes atuais
- Potencial de novos clientes
- Taxa de ocupação das portas PON
- Quantidade de ONTs por porta
- Split ratio
- Banda média e pico por cliente
- Capacidade das interfaces de uplink
- Capacidade da OLT
- Disponibilidade de fibras
- Distância óptica
- Budget óptico

Também considero o crescimento comercial projetado.

Por exemplo, se uma região apresenta crescimento constante de clientes, não espero atingir 100% da capacidade para iniciar a expansão.

Defino thresholds para iniciar planejamento e implantação antes da saturação.

---

## 4. Como investigar saturação de backbone?

Primeiro verifico os indicadores de utilização das interfaces.

Analiso:

- Tráfego médio
- Tráfego de pico
- Percentil 95
- Drops
- Erros
- Descartes
- CPU
- Memória
- Latência
- Jitter
- Perda de pacotes

Depois verifico quais aplicações, clientes ou rotas estão gerando maior consumo.

Ferramentas como SNMP, NetFlow, sFlow, telemetria e sistemas de monitoramento ajudam nessa análise.

Também comparo o comportamento atual com o histórico de crescimento.

Caso confirme saturação, avalio:

- Upgrade de capacidade
- Agregação de links
- ECMP
- Redistribuição de tráfego
- Traffic Engineering
- Novo trânsito IP
- Alteração de política BGP

O importante é corrigir a causa e não apenas tratar o sintoma.

---

## 5. Como reduzir MTTR?

Para reduzir o Mean Time to Repair, procuro melhorar todo o processo de detecção, diagnóstico e recuperação.

Algumas ações importantes:

- Monitoramento proativo
- Alertas bem configurados
- Documentação atualizada
- Diagramas da rede
- Inventário
- Runbooks
- Automação
- Backup de configurações
- Definição de escalonamento
- Treinamento da equipe
- Base de conhecimento
- Acesso rápido às ferramentas de troubleshooting

Também analiso os incidentes anteriores para identificar quais etapas consumiram mais tempo.

O objetivo é diminuir o tempo entre a identificação da falha e a restauração completa do serviço.

---

## 6. Como estruturar redundância de POP?

Um POP crítico deve possuir redundância em vários níveis.

### Energia

- Dupla alimentação quando possível
- UPS
- Banco de baterias
- Gerador
- Monitoramento elétrico

### Rede

- Dois equipamentos de core ou agregação
- Links por rotas físicas diferentes
- Redundância de uplinks
- LACP ou ECMP quando aplicável

### Roteamento

- OSPF ou IS-IS
- BGP
- BFD
- Fast Convergence

### Óptico

- Rotas de fibra distintas
- Redundância de DIOs e infraestrutura
- Proteção de enlaces quando necessário

O principal cuidado é evitar redundância aparente, como dois links passando pelo mesmo duto ou pela mesma rota física.

---

## 7. Como planejar migração GPON para XGS-PON?

Primeiro analiso a necessidade da migração.

Avalio:

- Crescimento de banda por cliente
- Utilização das portas GPON
- Capacidade da OLT
- Perfil de clientes
- Serviços corporativos
- Necessidade de velocidades acima de 1 Gbps

Depois verifico compatibilidade da infraestrutura existente.

Analiso:

- OLT
- Placas
- ONTs
- Splitters
- Fibra
- Budget óptico
- Gerenciamento

Quando possível, utilizo coexistência entre GPON e XGS-PON utilizando elementos como coexistence elements para aproveitar a mesma ODN.

A migração pode ser gradual, priorizando clientes com maior necessidade de banda.

Isso reduz CAPEX e risco operacional.

---

## 8. Quando usar MPLS ou Segment Routing?

MPLS tradicional é adequado para redes já consolidadas que utilizam:

- LDP
- RSVP-TE
- L2VPN
- L3VPN
- Traffic Engineering

Segment Routing pode ser utilizado para simplificar o plano de controle e aumentar a programabilidade da rede.

Com Segment Routing é possível reduzir dependência de protocolos adicionais utilizados no MPLS tradicional.

Entre os benefícios estão:

- Simplificação
- Escalabilidade
- Traffic Engineering
- Automação
- Melhor integração com SDN
- Fast Reroute

A decisão depende da arquitetura atual, capacidade dos equipamentos, maturidade da equipe e necessidade de automação.

Eu não migraria simplesmente por ser uma tecnologia mais nova. Avaliaria benefício, custo, risco e compatibilidade.

---

## 9. Como tratar QoS para voz?

O primeiro passo é identificar e classificar corretamente o tráfego de voz.

Normalmente aplicaria:

- Classificação
- Marcação DSCP
- Filas prioritárias
- Controle de congestionamento
- Policing ou shaping quando necessário

Tráfego RTP de voz pode utilizar DSCP EF.

Também monitoraria:

- Latência
- Jitter
- Perda
- MOS

Para voz, valores elevados de jitter e perda podem causar cortes e degradação perceptível para o usuário.

Em ambientes SD-WAN, também utilizaria políticas de seleção de caminho baseadas na qualidade dos links.

Se um link apresentar perda, latência ou jitter acima do limite definido, o tráfego de voz pode ser direcionado para outro caminho.

---

## 10. Como validar um incidente óptico?

Começo identificando a extensão do problema.

Verifico se afeta:

- Um cliente
- Uma porta PON
- Uma região
- Um enlace
- Um POP inteiro

Depois analiso os níveis ópticos.

Utilizo informações da OLT, ONT ou equipamentos de transporte para verificar potência RX e TX.

Quando necessário, utilizo:

- Power Meter
- OTDR
- VFL

O OTDR ajuda a localizar eventos como:

- Rompimento
- Macrocurvatura
- Conector com perda elevada
- Emenda ruim
- Reflexão

Também comparo o resultado com o projeto óptico e o budget esperado.

Após a correção, valido novamente os níveis e monitoro o serviço para garantir estabilidade.

---

# Perguntas Técnicas Adicionais

## 11. Como você faria Capacity Planning de um backbone?

Eu utilizaria dados históricos de tráfego e projeções de crescimento.

Analisaria:

- Média de utilização
- Pico
- Percentil 95
- Crescimento mensal
- Quantidade de clientes
- Novos projetos
- Trânsito IP

Criaria thresholds, por exemplo:

- 60% — acompanhamento
- 70% — planejamento
- 80% — expansão prioritária

O objetivo é expandir antes que a saturação impacte os clientes.

---

## 12. Como você investigaria perda de pacotes?

Eu começaria identificando onde a perda ocorre.

Verificaria:

1. Interface física
2. Erros e drops
3. Utilização
4. CPU do equipamento
5. QoS
6. Roteamento
7. MTU
8. Congestionamento

Utilizaria ferramentas como:

- Ping
- Traceroute
- MTR
- Wireshark
- Telemetria
- SNMP

Também compararia diferentes caminhos para identificar se o problema está dentro da rede ou em um provedor externo.

---

## 13. Como você planeja redundância BGP com dois provedores?

Utilizaria BGP Multihoming.

O ambiente teria dois links de provedores distintos.

Configuraria políticas utilizando atributos como:

- Local Preference
- AS Path
- MED
- Communities
- Prefix Lists

Também poderia utilizar prepend para influenciar tráfego de entrada.

O objetivo é garantir continuidade caso um dos provedores falhe e também controlar como o tráfego entra e sai da rede.

---

## 14. Como evitar loops de roteamento?

Utilizo desenho adequado da arquitetura e filtros de rotas.

Algumas medidas:

- Prefix Lists
- Route Maps
- Filtros BGP
- Controle de redistribuição
- Uso correto de áreas OSPF
- Métricas consistentes

Ao redistribuir rotas entre protocolos, tenho atenção especial para evitar redistribuição bidirecional sem controle.

---

## 15. Como você estruturaria monitoramento de uma rede ISP?

Eu dividiria o monitoramento em camadas.

### Infraestrutura

- CPU
- Memória
- Temperatura
- Energia

### Interfaces

- Utilização
- Erros
- Drops
- Estado operacional

### Serviços

- BGP
- OSPF
- MPLS
- DNS
- DHCP
- CGNAT

### Experiência

- Latência
- Jitter
- Perda
- Disponibilidade

Também utilizaria dashboards para NOC e alertas baseados em criticidade.

---

## 16. Como você faria troubleshooting de uma rota BGP?

Minha sequência seria:

1. Verificar estado da sessão
2. Validar conectividade IP
3. Confirmar ASN
4. Verificar prefixes anunciados
5. Conferir filtros
6. Conferir Route Maps
7. Validar atributos BGP
8. Verificar RIB
9. Verificar FIB
10. Testar o caminho

Comandos comuns:

```bash
show bgp summary
show bgp ipv4 unicast
show ip route
show ip bgp neighbors
```

---

## 17. Como você diferencia problema de camada física de problema de roteamento?

Primeiro valido a camada física.

Verifico:

- Interface up/down
- Erros
- CRC
- Drops
- Potência óptica
- Velocidade
- Duplex

Depois valido camada 2 e camada 3.

Analiso:

- VLAN
- ARP
- Endereço IP
- Gateway
- Roteamento

Uma abordagem estruturada reduz o tempo de troubleshooting.

---

## 18. Como você desenharia uma rede para alta disponibilidade?

Eu evitaria pontos únicos de falha.

Consideraria:

- Redundância de equipamentos
- Redundância de links
- Rotas físicas diferentes
- Redundância elétrica
- Protocolos de convergência rápida
- Monitoramento
- Capacidade de contingência

Também realizaria testes periódicos de failover.

Alta disponibilidade precisa ser validada, não apenas desenhada.

---

# Estrutura para responder perguntas técnicas

Durante a entrevista, posso organizar as respostas utilizando:

**Diagnóstico → Métrica → Tecnologia → Ação → Validação**

Exemplo:

> "Primeiro eu analisaria utilização, latência, jitter, perda e erros das interfaces. Depois identificaria o ponto da rede onde ocorre a degradação. Com a causa localizada, faria a correção ou redirecionamento do tráfego e, por fim, validaria os indicadores para confirmar a normalização."

---

# Conceito importante para entrevista de Gerente de Redes

Uma boa resposta gerencial não deve ficar apenas na configuração técnica.

Procure sempre conectar:

**Tecnologia → Disponibilidade → SLA → Cliente → Risco → Custo**

Por exemplo:

> "Tecnicamente posso aumentar um link de 10 Gbps para 40 Gbps, mas como gerente também preciso avaliar crescimento de tráfego, custo do upgrade, prazo do fornecedor, impacto no SLA e em quanto tempo essa nova capacidade será consumida."

Isso demonstra conhecimento técnico aliado à visão de negócio.