📱 Catálogo Interativo Mobile

Aplicativo mobile desenvolvido em React Native com Expo para apresentação de produtos de uma loja virtual, com organização por categorias masculina e feminina, navegação entre telas e consumo de dados de uma API REST.

O projeto foi desenvolvido como parte da disciplina de Mobile Development, com o objetivo de aplicar conceitos de desenvolvimento mobile, gerenciamento de estado, consumo de APIs, navegação entre telas e organização de componentes.

🎯 Objetivo do projeto

O objetivo deste projeto é desenvolver um catálogo de produtos mobile, responsivo e leve, permitindo que o usuário:

Realize um login com validação dos campos;
Acesse um catálogo de produtos;
Navegue entre as categorias masculina e feminina através de abas;
Visualize produtos organizados por categoria;
Consulte informações detalhadas de cada produto;
Visualize preço, desconto, descrição e imagem;
Navegue entre as telas de forma intuitiva;
Realize logout e retorne à tela de login.
🚀 Funcionalidades
🔐 Login

A aplicação possui uma tela inicial de login com:

Campo de e-mail;
Campo de senha;
Validação dos campos;
Armazenamento temporário das informações do usuário;
Redirecionamento para o catálogo após o login.
🛍️ Catálogo de produtos

A tela principal apresenta os produtos separados em duas categorias principais:

Masculino
Feminino

A navegação entre as categorias é realizada através de abas.

👕 Categorias masculinas

O catálogo masculino utiliza as seguintes categorias da API:

mens-shirts
mens-shoes
mens-watches
👗 Categorias femininas

O catálogo feminino utiliza as seguintes categorias:

womens-bags
womens-dresses
womens-jewellery
womens-shoes
womens-watches
🔎 Detalhes do produto

Ao selecionar um produto, o usuário é direcionado para uma tela de detalhes.

São apresentadas informações como:

Nome do produto;
Imagem;
Descrição;
Preço;
Percentual de desconto.

A navegação utiliza o ID do produto como parâmetro para buscar e apresentar os dados correspondentes.

🚪 Logout

A aplicação possui uma opção de logout que:

Remove os dados temporários do usuário;
Encerra a sessão;
Retorna o usuário para a tela de login.
🌐 Consumo da API

Os produtos são obtidos através da API REST DummyJSON.

Documentação oficial:

https://dummyjson.com/docs

As categorias são consultadas através do endpoint:

https://dummyjson.com/products/category/{categoria}


Exemplo:

https://dummyjson.com/products/category/mens-shoes


Para consultar os detalhes de um produto específico:

https://dummyjson.com/products/{id}


O consumo da API é realizado utilizando Axios.

🧰 Tecnologias utilizadas

O projeto utiliza as seguintes tecnologias:

React Native — desenvolvimento da aplicação mobile;
Expo — ambiente e ferramentas para desenvolvimento React Native;
TypeScript — tipagem estática e maior segurança no desenvolvimento;
Axios — consumo da API REST;
Redux Toolkit — gerenciamento de estado global;
React Navigation — navegação entre as telas;
DummyJSON — API REST utilizada para disponibilização dos produtos.
🗂️ Estrutura do projeto

A aplicação foi organizada buscando separar responsabilidades entre telas, componentes, serviços e gerenciamento de estado.

Uma estrutura utilizada no projeto é:

src/
├── components/
│   ├── ProductCard/
│   └── ...
│
├── screens/
│   ├── LoginScreen/
│   ├── ProductsScreen/
│   └── ProductDetailsScreen/
│
├── services/
│   └── api.ts
│
├── store/
│   ├── authSlice/
│   └── ...
│
├── routes/
│   └── ...
│
└── types/
    └── ...


Essa organização facilita a manutenção do código e contribui para a separação entre lógica de negócio, renderização e estilização.

🔄 Fluxo da aplicação

O fluxo principal da aplicação foi planejado da seguinte maneira:

┌──────────────┐
│    LOGIN     │
└──────┬───────┘
       │
       ▼
┌─────────────────────┐
│ CATÁLOGO DE PRODUTOS│
│                     │
│ Masculino | Feminino│
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ DETALHES DO PRODUTO │
│                     │
│ Imagem              │
│ Nome                │
│ Descrição           │
│ Preço               │
│ Desconto            │
└─────────────────────┘
           │
           │ Logout
           ▼
      ┌──────────┐
      │  LOGIN   │
      └──────────┘

⏳ Loading e tratamento de erros

Durante o consumo da API, a aplicação considera os diferentes estados da requisição:

Estado de carregamento (loading);
Sucesso na requisição;
Erro na comunicação com a API;
Ausência de produtos.

Enquanto os dados estão sendo carregados, é apresentado um indicador visual para informar o usuário.

Em caso de erro, a aplicação apresenta uma mensagem informando que não foi possível carregar os produtos.

Esses tratamentos são importantes para proporcionar uma melhor experiência de utilização e evitar que o usuário fique sem feedback durante uma requisição.

🧠 Conceitos aplicados

Durante o desenvolvimento foram aplicados conceitos estudados na disciplina, como:

Componentização;
Hooks do React;
Gerenciamento de estado;
Redux Toolkit;
Consumo de API REST;
Requisições assíncronas;
Axios;
Navegação entre telas;
Passagem de parâmetros entre telas;
Renderização de listas;
Tratamento de loading;
Tratamento de erros;
Organização de projetos React Native;
Responsividade e estilização para dispositivos móveis.
📸 Capturas de tela
Tela de Login

Adicione aqui o print da tela de login.

Catálogo — Masculino

Adicione aqui o print da aba masculina.

Catálogo — Feminino

Adicione aqui o print da aba feminina.

Detalhes do produto

Adicione aqui o print da tela de detalhes.

▶️ Como executar o projeto
Pré-requisitos

Antes de executar o projeto, é necessário ter instalado:

Node.js;
npm ou Bun;
Expo CLI ou utilizar o Expo através do projeto;
Expo Go em um dispositivo físico, caso queira executar pelo celular.
1. Clone o repositório
git clone https://github.com/williamjayjay/ecommerce-nike-stripe-redux-react-native.git

2. Acesse a pasta do projeto
cd ecommerce-nike-stripe-redux-react-native

3. Instale as dependências

Com npm:

npm install


ou utilizando Bun:

bun install

4. Inicie o projeto
npx expo start


Após iniciar o Expo, é possível executar a aplicação através do Expo Go, em um dispositivo físico, ou através de um emulador Android/iOS configurado.

📚 Fontes de pesquisa

As principais fontes utilizadas durante o desenvolvimento foram:

Figma do projeto — referência para o desenho e organização das telas;
DummyJSON — documentação da API utilizada para consulta dos produtos;
Axios — documentação para consumo de APIs REST;
React Native — documentação oficial;
Expo — documentação oficial;
React Navigation — documentação para navegação entre telas;
Redux Toolkit — documentação para gerenciamento de estado.
💭 Reflexão sobre o projeto

O desenvolvimento deste aplicativo permitiu aplicar conceitos fundamentais de desenvolvimento mobile em um cenário próximo de uma aplicação real de e-commerce. Aplicativos móveis são importantes para o comércio eletrônico por oferecerem praticidade, acessibilidade e uma experiência de compra adaptada aos dispositivos utilizados diariamente pelos consumidores.

Um dos principais desafios foi trabalhar com dados provenientes de uma API REST, considerando estados de carregamento, possíveis erros de comunicação e a organização dos dados recebidos. A utilização do Axios facilitou o processo de comunicação com a API, enquanto o Redux Toolkit contribuiu para o gerenciamento do estado da aplicação.

A navegação entre as telas também foi importante para criar um fluxo intuitivo entre login, catálogo e detalhes do produto. Dessa forma, o projeto permitiu colocar em prática conceitos estudados durante as aulas, como componentização, gerenciamento de estado, consumo de APIs, navegação e organização de aplicações React Native.

👨‍💻 Autor

Rodrigo

Projeto desenvolvido para a disciplina de Mobile Development.

