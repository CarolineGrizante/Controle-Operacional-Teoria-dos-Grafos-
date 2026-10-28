# Controle Operacional Web

## Descrição

O **Controle Operacional Web** é uma aplicação web acadêmica desenvolvida para simular o planejamento de operações logísticas.

O sistema permite selecionar origem, destino, motorista, veículo, cargas e condições das vias para calcular uma rota de transporte. Antes de autorizar a viagem, a aplicação também realiza validações de segurança e conformidade.

O projeto utiliza o algoritmo de Dijkstra para encontrar a melhor rota de acordo com o objetivo selecionado:

- Menor tempo
- Menor custo

> Este projeto foi desenvolvido para fins acadêmicos. Os dados utilizados são de demonstração e o trânsito apresentado é simulado.

## Funcionalidades

- Mapa interativo
- Seleção de origem e destino
- Seleção de motoristas e veículos
- Cálculo de rotas
- Escolha entre menor tempo e menor custo
- Seleção de encomendas
- Cadastro de paradas obrigatórias
- Cálculo do peso e volume da carga
- Validação da CNH do motorista
- Validação da categoria da CNH
- Validação do RNTRC do veículo
- Validação da licença MOPP
- Verificação de sobrecarga
- Verificação de cubagem excedida
- Simulação de chuva, tempestade, acidente e interdição
- Cálculo de pedágios
- Relatório operacional
- Sistema de auditoria
- Cenário de bloqueio por irregularidade
- Layout responsivo para computador e tablet

## Tecnologias utilizadas

- HTML5
- CSS3
- JavaScript
- Leaflet
- OpenStreetMap
- XAMPP ou Live Server

## Estrutura do projeto

```text
ControleOperacionalWeb/
├── index.html
├── styles.css
├── data.js
├── app.js
├── config.example.js
├── README.md
└── MANUAL.md
