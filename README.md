# desafio-tecnico-reactJS
Desafio técnico desenvolvido por mim em ReactJs. Descrição do desafio abaixo.

Teste Frontend estágio Neste teste serão avaliados seus conhecimentos em Javascript, HTML e CSS, a criatividade e metodologia aplicada no desenvolvimento, a usabilidade e design da aplicação final. Você é o desenvolvedor frontend de uma empresa que coleta dados de equipamentos utilizados em uma operação florestal. Dentre esses dados estão o histórico de posições e estados desses equipamentos. O estado de um equipamento é utilizado para saber o que o equipamento estava fazendo em um determinado momento, seja Operando, Parado ou em Manutenção. O estado é alterado de acordo com o uso do equipamento na operação, já a posição do equipamento é coletada através do GPS e é enviada e armazenada de tempo em tempo pela aplicação.

Seu objetivo é, de posse desses dados, desenvolver o frontend de aplicação web que trate e exibida essas informações para os gestores da operação.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Requisitos para rodar o projeto 

Setup de ambiente: 
Download Node
Download NPM

Como rodar na minha máquina? 
Clone o projeto
Rode npm install
Rode npm run dev
Pronto.

Estrutura do projeto:

./src/page/EquipmentPage: É a página principal do projeto onde todos os componentes principais que compõem a interface são renderizados.
./src/Components: Pasta onde se encontram todos os componentes usados na construção da interface, onde cada componente contém uma pasta própria divida em dois arquivos: JSX e CSS.

Função de cada um dos componentes principais: 

./src/Components/FilterComponent: Tem a função de filtrar os componentes de acordo com a opção selecionada no select e partir do método filter para filtrar e retornar uma nova array.

./src/Components/EquipsContainerComponent: Recebe a array com os equipamentos a serem exibidos e usa o método map para fazer o display de cada item da array. 

./src/Components/EquipmentComponent : É chamado a partir do método map usado no EquipsContainer e retorna a seção que exibe as informações de cada item como nome, modelo e estado. Informações acessadas através do método find para acessar as chaves estrangeiras. Seção que ao ser clicada abre o dropdown trazendo mais informações sobre determinado equipamento.

./src/Components/OpenEquipment: É chamado a partir do click em algum EquipmentComponent, recebe um objeto que contém a latitude e longitude de determinado equipamento e usa para exibir no mapa aonde o equipamento se encontra. Também recebe e exibe os ultimos estados do equipamento e a data e hora de cada um.

./src/Components/FullMapComponent: Mapa completo que fica separado de todos os outros, criado para mostrar todos os equipamentos ao mesmo tempo cada um em sua determinada localização usando o método map no equipmentPositionHistory para criar um marker para cada equipamento.

./src/Components/MarkerComponent: Tem o objetivo de exibir um marker para cada equipamento e exibir um icon diferente para cada modelo de equipamento.
