Controle Operacional Web

Descrição

O Controle Operacional Web é uma aplicação web acadêmica desenvolvida para simular o planejamento de operações logísticas de transporte.

O sistema permite selecionar origem, destino, motorista, veículo, objetivo da rota, condição das vias e paradas obrigatórias. Antes de autorizar a viagem, são realizadas validações de segurança, conformidade e capacidade de carga.

A aplicação utiliza o algoritmo de Dijkstra para encontrar a melhor rota conforme o objetivo selecionado:

•
Menor tempo;

•
Menor custo.

As cidades são representadas como nós e as rodovias como arestas do grafo. As arestas possuem atributos como distância, velocidade média, pedágio e condição da via.


Este projeto foi desenvolvido para fins acadêmicos. Os dados de motoristas, veículos, encomendas, pedágios, trânsito e condições das vias são simulados.




Funcionalidades

•
Grafo operacional interativo;

•
Zoom e arrasto no grafo;

•
Cidades representadas como nós;

•
Rodovias representadas como arestas;

•
Vias alternativas entre cidades;

•
Nomes das rodovias;

•
Marcadores de pedágios;

•
Camada de trânsito simulado;

•
Ativação e desativação das camadas do mapa;

•
Seleção de origem e destino;

•
Seleção de motoristas e veículos;

•
Cálculo de rotas por menor tempo ou menor custo;

•
Seleção de paradas obrigatórias;

•
Filtragem automática de encomendas por origem e destino;

•
Inclusão opcional de cargas perigosas;

•
Cálculo do peso e do volume da carga;

•
Validação da CNH do motorista;

•
Validação da categoria da CNH;

•
Validação do RNTRC do veículo;

•
Validação da licença MOPP;

•
Verificação de sobrecarga;

•
Verificação de cubagem excedida;

•
Simulação de chuva, tempestade, acidente e interdição;

•
Cálculo de pedágios;

•
Relatório operacional;

•
Sistema de auditoria;

•
Cenário de bloqueio por irregularidade;

•
Layout responsivo para computador e tablet;

•
Camada de mapa real opcional, sem substituir o grafo operacional.




Tecnologias utilizadas

•
HTML5: estrutura da aplicação, formulários, botões, painéis, listas e janelas de diálogo;

•
CSS3: estilização da interface, cores, espaçamentos, painéis e layout responsivo;

•
JavaScript ES6+: lógica da aplicação, validações, cálculo das rotas, manipulação do DOM, relatórios e auditoria;

•
Leaflet: biblioteca utilizada para zoom, arrasto, marcadores, linhas, camadas e interação com o mapa;

•
Grafo operacional: cidades como nós e rodovias como arestas;

•
Algoritmo de Dijkstra: utilizado para encontrar rotas por menor tempo ou menor custo;

•
XAMPP: utilizado para executar o projeto localmente através do Apache;

•
Visual Studio Code com Live Server: alternativa para execução durante o desenvolvimento;

•
GitHub: utilizado para versionamento e disponibilização do código-fonte.




Estrutura do projeto

Plain Text


ControleOperacionalWeb/
├── index.html
├── styles.css
├── data.js
├── app.js
├── config.example.js
├── README.md
├── MANUAL.md
└── imagens/
    ├── TelaInicial.png
    ├── TestePerfeito.png
    ├── TesteBloqueado.png
    ├── SemCamadasMapa.png
    └── RelatorioSistema.png



Principais arquivos

•
index.html: estrutura visual da aplicação;

•
styles.css: estilos, cores, dimensões e responsividade;

•
data.js: cidades, rodovias, pedágios, motoristas, veículos e encomendas;

•
app.js: regras de negócio, Dijkstra, validações, trânsito simulado, relatórios e auditoria;

•
config.example.js: modelo para futura integração com uma API externa de trânsito.




Imagens da aplicação

Tela principal











Rota autorizada com carga válida











Cenário de bloqueio preventivo











Grafo operacional sem camadas adicionais











Relatório operacional














Como executar localmente

Opção 1 — XAMPP

1.
Faça o download ou clone este repositório:

Bash


git clone https://github.com/CarolineGrizante/Controle-Operacional-Teoria-dos-Grafos-.git



1.
Copie a pasta do projeto para o diretório htdocs do XAMPP:

Plain Text


C:\xampp\htdocs\ControleOperacionalWeb



O nome da pasta pode ser diferente, mas deve ser utilizado no endereço do navegador.

1.
Abra o XAMPP.

2.
Inicie o módulo Apache.

3.
Acesse no navegador:

Plain Text


http://localhost/ControleOperacionalWeb/



Caso a pasta tenha outro nome, substitua ControleOperacionalWeb pelo nome correto.

Opção 2 — Visual Studio Code com Live Server

1.
Abra a pasta do projeto no Visual Studio Code;

2.
Instale a extensão Live Server;

3.
Clique com o botão direito no arquivo index.html;

4.
Selecione Open with Live Server;

5.
A aplicação será aberta automaticamente no navegador.

O XAMPP é recomendado quando se deseja simular uma estrutura de servidor local mais próxima de uma hospedagem tradicional.




Funcionamento do grafo

O mapa principal da aplicação representa a rede logística como um grafo:

•
Cada cidade ou centro de distribuição é um nó;

•
Cada rodovia é uma aresta;

•
A distância, a velocidade, o pedágio e a condição da via são atributos da aresta;

•
Uma cidade pode ser acessada por mais de uma rodovia;

•
O algoritmo de Dijkstra compara os caminhos disponíveis;

•
A rota final é destacada visualmente no grafo.

A versão web mantém o mesmo conceito da versão WPF, mas utiliza HTML, CSS e JavaScript para oferecer mais interações, como zoom, arrasto, camadas, marcadores e janelas de relatório.




Carga e encomendas

As encomendas são filtradas conforme a origem e o destino selecionados para a viagem.

Quando a opção de carga perigosa está desmarcada, são consideradas as encomendas normais. Quando a opção é ativada, as cargas perigosas também podem ser incluídas, desde que o motorista possua a licença MOPP.

O sistema calcula automaticamente:

•
Peso total da carga;

•
Volume total da carga;

•
Percentual de utilização do veículo;

•
Excesso de peso;

•
Excesso de cubagem;

•
Necessidade de MOPP.




Trânsito e condições das vias

O projeto possui condições simuladas para demonstrar o impacto das vias no cálculo da rota:

•
Normal;

•
Chuva;

•
Tempestade;

•
Acidente;

•
Interdição.

As condições alteram o tempo estimado ou podem impedir a utilização de determinadas ligações.

O trânsito apresentado é simulado. A aplicação não consulta, por padrão, dados de trânsito em tempo real.




Mapa real opcional

O modo principal utiliza um grafo operacional estilizado semelhante ao protótipo WPF. Esse grafo não depende de um mapa externo para funcionar.

A aplicação possui uma opção de camada geográfica real. Quando ativada, ela tenta adicionar um mapa de referência por baixo do grafo. Essa camada é opcional e não substitui:

•
Os nós;

•
As arestas;

•
Os nomes das rodovias;

•
Os pedágios;

•
A rota calculada;

•
As regras logísticas.

Caso o provedor externo não esteja disponível, o grafo operacional continua funcionando.




Integração futura com trânsito real

Para utilizar dados reais de trânsito, será necessário integrar uma API externa, como Google Maps Platform, TomTom ou HERE.

O processo normalmente envolve:

1.
Escolher um provedor;

2.
Criar uma chave de API;

3.
Restringir a chave ao domínio da aplicação;

4.
Consultar o tráfego por rodovia ou coordenadas;

5.
Atualizar as condições das arestas;

6.
Recalcular a rota;

7.
Nunca publicar uma chave sem restrição de domínio.




Observações

O sistema foi desenvolvido para fins acadêmicos e de demonstração.

As informações de motoristas, veículos, encomendas, condições das vias, pedágios e trânsito são simuladas e não representam dados reais de uma operação logística.

O algoritmo, os valores financeiros, as velocidades e as regras de validação foram criados para demonstrar a aplicação de conceitos de teoria dos grafos, desenvolvimento web e controle operacional.

