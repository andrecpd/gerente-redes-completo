# Perguntas Gerenciais de Entrevista — Gerente de Redes e Telecomunicações

## 1. Como você prioriza investimentos?

Eu priorizo investimentos considerando impacto no negócio, criticidade da infraestrutura, risco operacional, capacidade, disponibilidade e retorno esperado.

Primeiro avalio quais pontos podem gerar indisponibilidade, perda de receita ou impacto no SLA. Depois classifico os projetos por prioridade, custo, benefício e urgência.

Exemplo de critérios:
- Risco de indisponibilidade
- Impacto nos clientes
- Capacidade atual e crescimento
- SLA
- Segurança
- Obsolescência tecnológica
- ROI
- CAPEX e OPEX

Minha prioridade seria primeiro eliminar riscos críticos, depois garantir capacidade para crescimento e, em seguida, investir em otimização e inovação.

---

## 2. Como você lidera NOC, campo e engenharia?

Eu trabalho com responsabilidades bem definidas e integração entre as equipes.

O NOC fica focado em monitoramento, incidentes, SLA e escalonamento.

A equipe de campo atua em instalação, manutenção física, fibra óptica, equipamentos e atendimento presencial.

A engenharia trabalha com arquitetura, capacidade, melhorias, expansão e resolução de problemas de maior complexidade.

Como gerente, acompanho indicadores, backlog, incidentes, projetos e capacidade da rede.

Também realizo reuniões periódicas para alinhar prioridades entre NOC, campo e engenharia, evitando que cada área trabalhe isoladamente.

---

## 3. Como você apresenta risco técnico à diretoria?

Eu evito apresentar apenas detalhes técnicos.

Transformo o risco técnico em impacto para o negócio.

Por exemplo, em vez de dizer:

> "O backbone está chegando a 85% de utilização."

Eu apresentaria:

> "Se mantivermos o crescimento atual, em aproximadamente três meses poderemos atingir saturação do backbone, aumentando o risco de perda de pacotes, degradação do serviço e impacto no SLA dos clientes."

Apresento sempre:
- Situação atual
- Risco
- Probabilidade
- Impacto
- Custo de não agir
- Alternativas
- Investimento necessário
- Recomendação

Dessa forma, a diretoria consegue tomar decisões com base em risco e impacto financeiro.

---

## 4. Como você lida com divergência técnica na equipe?

Primeiro procuro entender os argumentos de cada profissional.

Evito tomar decisões baseadas apenas em opinião ou senioridade.

Peço que as alternativas sejam avaliadas considerando:
- Disponibilidade
- Segurança
- Escalabilidade
- Complexidade operacional
- Custo
- Performance
- Suporte do fabricante
- Risco de implementação

Quando necessário, realizamos laboratório, PoC ou teste controlado.

A decisão final deve ser documentada tecnicamente para que toda a equipe entenda os motivos da escolha.

---

## 5. Como você escolhe fornecedores?

Eu avalio fornecedores utilizando critérios técnicos, comerciais e operacionais.

Entre os principais critérios estão:
- Qualidade da solução
- Compatibilidade com a arquitetura existente
- SLA de suporte
- Capacidade técnica
- Histórico do fornecedor
- Prazo de entrega
- Garantia
- Escalabilidade
- Segurança
- Custo total de propriedade
- CAPEX
- OPEX

Sempre que possível faço uma matriz de avaliação e PoC antes de decisões de maior impacto.

O menor preço nem sempre representa a melhor escolha. Avalio o custo total da solução durante seu ciclo de vida.

---

## 6. Como você controla CAPEX e OPEX?

Eu separo os investimentos entre despesas de expansão, modernização e operação.

CAPEX normalmente envolve:
- Equipamentos
- Backbone
- Fibra óptica
- Roteadores
- Switches
- Servidores
- Data Center
- Expansão da infraestrutura

OPEX envolve:
- Links
- Licenças
- Energia
- Contratos
- Manutenção
- Cloud
- Suporte
- Serviços de terceiros

Faço acompanhamento mensal do orçamento planejado versus realizado e analiso desvios.

Também acompanho indicadores como custo por cliente, custo por link, custo por site e custo por capacidade instalada.

---

## 7. Como você mede desempenho da área?

Eu utilizo KPIs técnicos, operacionais e financeiros.

Alguns exemplos:

### Operação
- Disponibilidade da rede
- SLA
- MTTR
- MTBF
- Quantidade de incidentes
- Incidentes recorrentes

### Rede
- Utilização dos links
- Latência
- Jitter
- Perda de pacotes
- Capacidade disponível
- Crescimento de tráfego

### Atendimento
- Tempo médio de atendimento
- Tempo de resolução
- Backlog
- Reincidência

### Projetos
- Prazo
- Custo
- Escopo
- Percentual de conclusão

### Financeiro
- CAPEX
- OPEX
- Budget versus realizado
- Custo por cliente
- Custo por site

Os indicadores precisam mostrar tendência e permitir decisões preventivas.

---

## 8. Como você conduz um incidente crítico?

Primeiro estabeleço uma sala de crise e defino responsabilidades.

Organizo o atendimento em quatro frentes:

1. Diagnóstico
2. Contenção
3. Recuperação
4. Comunicação

Durante o incidente acompanho impacto, clientes afetados, serviços comprometidos e tempo de indisponibilidade.

Evito alterações não controladas durante a crise.

Depois da normalização realizo uma análise de causa raiz.

O processo termina com:
- RCA
- Timeline do incidente
- Impacto
- Causa
- Solução
- Ações preventivas
- Responsáveis
- Prazo

O objetivo não é apenas resolver o incidente, mas impedir sua recorrência.

---

## 9. Como você profissionaliza uma operação informal?

Primeiro faço um diagnóstico da operação atual.

Identifico:
- Topologia
- Inventário
- Configurações
- Processos
- Monitoramento
- Documentação
- Responsabilidades
- Incidentes recorrentes
- Pontos únicos de falha

Depois implemento gradualmente:

1. Documentação da rede
2. Inventário
3. Monitoramento
4. Gestão de incidentes
5. Gestão de mudanças
6. Backup de configurações
7. Controle de acesso
8. KPIs
9. SLAs
10. Runbooks
11. Gestão de capacidade
12. Gestão de fornecedores

Também crio uma rotina de reuniões operacionais e revisão de indicadores.

O objetivo é transformar uma operação reativa em uma operação previsível e baseada em processos.

---

## 10. Como você equilibra estabilidade e inovação?

Eu separo claramente ambiente de produção, laboratório e homologação.

Não introduzo tecnologia nova diretamente em produção sem validação.

Normalmente sigo:

1. Identificação da necessidade
2. Análise técnica
3. Avaliação de riscos
4. PoC
5. Laboratório
6. Homologação
7. Piloto
8. Plano de rollback
9. Implementação controlada
10. Monitoramento

Inovação precisa resolver um problema real da operação ou do negócio.

Meu objetivo é modernizar a infraestrutura sem comprometer disponibilidade, segurança ou SLA.

---

# Perguntas adicionais para estudar

## 11. Como você realiza Capacity Planning?

Analiso histórico de crescimento de tráfego, utilização de interfaces, quantidade de clientes e projeções comerciais.

Defino thresholds para antecipar expansão.

Por exemplo:
- 60% — acompanhamento
- 70% — planejamento
- 80% — expansão prioritária

O objetivo é aumentar capacidade antes que exista impacto para os clientes.

---

## 12. Como você gerencia mudanças na rede?

Toda mudança deve possuir:
- Objetivo
- Escopo
- Equipamentos envolvidos
- Riscos
- Janela de manutenção
- Plano de implementação
- Plano de validação
- Plano de rollback
- Responsável

Mudanças críticas devem passar por aprovação antes da execução.

---

## 13. Como você reduz incidentes recorrentes?

Primeiro identifico os incidentes com maior frequência e impacto.

Depois aplico análise de causa raiz utilizando informações de monitoramento, logs, histórico e troubleshooting.

Crio planos de ação com responsável e prazo.

Também acompanho se o incidente voltou a ocorrer após a correção.

---

## 14. Como você gerencia crescimento da rede?

Utilizo Capacity Planning, previsão comercial e indicadores de utilização.

Avalio crescimento de:
- Clientes
- Backbone
- Links
- OLTs
- PON
- Roteadores
- Data Center
- Cloud
- Trânsito IP

Planejo expansão antes que o limite operacional seja atingido.

---

## 15. Como você gerencia uma equipe técnica?

Defino responsabilidades, prioridades e objetivos claros.

Procuro entender o nível técnico de cada profissional e distribuir atividades considerando experiência e desenvolvimento.

Também estimulo:
- Documentação
- Compartilhamento de conhecimento
- Treinamentos
- Certificações
- Laboratórios
- Automação

O gerente deve desenvolver a equipe e reduzir dependência de conhecimento concentrado em poucas pessoas.

---

## 16. Como você toma decisões técnicas?

Eu utilizo dados.

Analiso:
- Risco
- Custo
- Capacidade
- Segurança
- Disponibilidade
- Escalabilidade
- Complexidade
- Impacto operacional

Quando existem alternativas, documento os trade-offs e apresento a recomendação com justificativa técnica e financeira.

---

# Estrutura mental para responder perguntas gerenciais

Durante a entrevista, posso organizar minhas respostas utilizando:

**Cenário → Análise → Decisão → Execução → Indicador → Resultado**

Exemplo:

> "Primeiro eu analisaria os indicadores e o impacto no negócio. Depois classificaria o risco e definiria as alternativas. A decisão seria tomada considerando custo, disponibilidade, segurança e escalabilidade. Após a implementação, acompanharia os KPIs para validar o resultado."

Essa estrutura ajuda a demonstrar pensamento de gerente e não apenas conhecimento técnico.