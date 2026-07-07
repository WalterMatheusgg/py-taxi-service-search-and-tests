# Taxi Service Search and Tests

## Descrição

O **Taxi Service Search and Tests** é uma aplicação web desenvolvida com **Django** para praticar funcionalidades de busca e testes automatizados em um sistema de gerenciamento de serviço de táxi.

O projeto possui páginas para gerenciamento de motoristas, carros e fabricantes. Esta versão tem como foco a implementação de filtros de busca nas principais listagens do sistema e a validação do comportamento da aplicação por meio de testes.

## Funcionalidades

- Listagem de motoristas, carros e fabricantes;
- Busca de motoristas por nome de usuário;
- Busca de carros por modelo;
- Busca de fabricantes por nome;
- Visualização de detalhes de carros e motoristas;
- Proteção de páginas com autenticação;
- Uso de Class-Based Views;
- Testes automatizados para funcionalidades do sistema;
- Uso de fixture para carregamento de dados iniciais.

## Tecnologias utilizadas

- Python
- Django
- SQLite
- HTML
- CSS
- Django Templates
- Django Crispy Forms
- Django TestCase
- Git
- GitHub

## Estrutura do projeto

```text
py-taxi-service-search-and-tests/
├── taxi/
│   ├── migrations/
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── models.py
│   ├── urls.py
│   └── views.py
├── taxi_service/
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
├── templates/
├── static/
├── manage.py
├── requirements.txt
└── README.md
```

## Modelos principais

### Manufacturer

Representa uma fabricante de carros.

Principais campos:

- `name`: nome da fabricante;
- `country`: país de origem.

### Driver

Representa um motorista cadastrado no sistema.

Principais campos:

- `username`: nome de usuário;
- `first_name`: primeiro nome;
- `last_name`: sobrenome;
- `license_number`: número da licença.

### Car

Representa um carro associado a uma fabricante e a um ou mais motoristas.

Principais campos:

- `model`: modelo do carro;
- `manufacturer`: fabricante;
- `drivers`: motoristas associados.

## Funcionalidades de busca

O projeto inclui busca nas principais entidades do sistema:

- Motoristas podem ser buscados pelo nome de usuário;
- Carros podem ser buscados pelo modelo;
- Fabricantes podem ser buscados pelo nome.

Essas funcionalidades tornam a navegação mais prática e simulam um cenário mais próximo de uma aplicação real, principalmente quando há muitos registros cadastrados.

## Testes

O projeto também tem como objetivo praticar testes automatizados no Django.

Os testes ajudam a validar:

- Comportamento dos models;
- Acesso às views;
- Funcionamento das páginas de listagem;
- Funcionalidades de busca;
- Proteção de páginas que exigem autenticação.

## O que foi praticado

Este projeto permitiu praticar:

- Filtros de busca em views Django;
- Uso de parâmetros GET;
- Escrita de testes com Django;
- Organização de models, views, forms e templates;
- Proteção de páginas com autenticação;
- Uso de Class-Based Views;
- Carregamento de dados iniciais com fixtures.

## Como executar o projeto

### 1. Clone o repositório

```bash
git clone https://github.com/WalterMatheusgg/py-taxi-service-search-and-tests.git
```

### 2. Acesse a pasta do projeto

```bash
cd py-taxi-service-search-and-tests
```

### 3. Crie um ambiente virtual

```bash
python -m venv venv
```

### 4. Ative o ambiente virtual

No Windows:

```bash
venv\Scripts\activate
```

No Linux/macOS:

```bash
source venv/bin/activate
```

### 5. Instale as dependências

```bash
pip install -r requirements.txt
```

### 6. Execute as migrações

```bash
python manage.py migrate
```

### 7. Execute os testes

```bash
python manage.py test
```

### 8. Carregue os dados iniciais

```bash
python manage.py loaddata taxi_service_db_data.json
```

### 9. Inicie o servidor

```bash
python manage.py runserver
```

Depois, acesse no navegador:

```text
http://127.0.0.1:8000/
```

## Usuário padrão

Após carregar os dados iniciais, é possível acessar com:

```text
Username: admin.user
Password: 1qazcde3
```

## Autor

Desenvolvido por **Walter Matheus** como parte da trilha de estudos em Django.
