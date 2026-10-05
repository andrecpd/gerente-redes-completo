# Cabeamento Estruturado

Cabeamento estruturado é a infraestrutura física que organiza e padroniza as conexões de dados, voz e serviços dentro de prédios e Data Centers.

Uma infraestrutura bem organizada reduz falhas, facilita expansão e diminui o **MTTR**.

## Principais componentes

- Racks
- Patch Panels
- Patch Cords
- DIOs
- Fibra óptica
- Cabeamento metálico
- Organizadores horizontais e verticais
- Bandejas
- Identificação
- Aterramento

## Cabeamento metálico

Aplicações comuns:

- Usuários
- Access Points
- Telefonia IP
- Câmeras
- Equipamentos de rede
- Servidores

Categorias comuns:

- Cat5e
- Cat6
- Cat6A

Em novos projetos, Cat6 ou Cat6A são normalmente preferidos conforme distância, velocidade e requisitos.

## Fibra óptica

Utilizada principalmente em:

- Backbone
- Data Center
- Interligação entre racks
- Interligação entre prédios
- Links de alta capacidade

### Single Mode
Indicada para maiores distâncias.

### Multimode
Comum em ambientes internos e menores distâncias.

## Organização de racks

Boas práticas:

- Identificação de equipamentos e portas
- Organização de patch cords
- Separação de energia e dados
- Espaço para crescimento
- Fluxo de ar adequado
- Documentação atualizada

## Identificação

Exemplo:

```text
DC01-RACK03-PP01-P24
```

Onde:

```text
DC01   = Data Center
RACK03 = Rack 03
PP01   = Patch Panel 01
P24    = Porta 24
```

## Certificação

### Cobre
- Continuidade
- Comprimento
- NEXT
- Return Loss
- Perdas

### Fibra
- Atenuação
- Potência óptica
- Perdas em conectores
- Emendas

Ferramentas:

- Certificador de cabos
- Power Meter
- OTDR
- VFL

## Documentação

Manter registro de:

- Rack
- Patch Panel
- Porta
- Switch
- Porta do switch
- Fibra
- Origem
- Destino
- VLAN
- Equipamento conectado

| Rack | Patch Panel | Porta | Switch | Porta Switch | Destino |
|---|---|---|---|---|---|
| R01 | PP01 | 01 | SW01 | Gi1/0/1 | Server-01 |
| R01 | PP01 | 02 | SW01 | Gi1/0/2 | Server-02 |

## Gestão de capacidade

Manter reserva de:

- Portas de switches
- Portas de Patch Panels
- Espaço em rack
- Fibras
- Caminhos físicos

## Boas práticas

- Padronização
- Identificação
- Documentação
- Certificação
- Organização de racks
- Separação energia/dados
- Gestão de capacidade
- Controle de mudanças
- Manutenção preventiva

## Impacto operacional

```text
Organização
    ↓
Confiabilidade
    ↓
Troubleshooting
    ↓
Redução do MTTR
    ↓
Disponibilidade
```

## Resposta para entrevista

> Em projetos de cabeamento estruturado, considero padronização, identificação, organização de racks, patch panels, fibras e cobre, além da certificação dos pontos. Também considero documentação e reserva de capacidade para crescimento. Uma infraestrutura física bem organizada reduz falhas, facilita manutenção e ajuda diretamente na redução do MTTR.
