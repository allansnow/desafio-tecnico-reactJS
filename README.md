Requisitos para rodar o projeto 

Setup de ambiente: 
Download Node
Download NPM

Como rodar na minha máquina? 
Clone o projeto
Rode npm install
Rode npm run dev
Pronto.

Estrutura do projeto 

./src/page/EquipmentPage: É a página principal do projeto onde todos os componentes principais que compõem a interface são renderizados.
./src/Components: Pasta onde se encontram todos os componentes usados na construção da interface, onde cada componente contém uma pasta própria divida em dois arquivos: JSX e CSS.

Função de cada um dos componentes principais: 

./src/Components/FilterComponent: Tem a função de filtrar os componentes de acordo com a opção selecionada no select e partir do método filter para filtrar e retornar uma nova array.

./src/Components/EquipsContainerComponent: Recebe a array com os equipamentos a serem exibidos e usa o método map para fazer o display de cada item da array. 

./src/Components/EquipmentComponent : É chamado a partir do método map usado no EquipsContainer e retorna a seção que exibe as informações de cada item como nome, modelo e estado. Informações acessadas através do método find para acessar as chaves estrangeiras. Seção que ao ser clicada abre o dropdown trazendo mais informações sobre determinado equipamento.

./src/Components/OpenEquipment: É chamado a partir do click em algum EquipmentComponent, recebe um objeto que contém a latitude e longitude de determinado equipamento e usa para exibir no mapa aonde o equipamento se encontra. Também recebe e exibe os ultimos estados do equipamento e a data e hora de cada um.

./src/Components/FullMapComponent: Mapa completo que fica separado de todos os outros, criado para mostrar todos os equipamentos ao mesmo tempo cada um em sua determinada localização usando o método map no equipmentPositionHistory para criar um marker para cada equipamento.

./src/Components/MarkerComponent: Tem o objetivo de exibir um marker para cada equipamento e exibir um icon diferente para cada modelo de equipamento.