Mamô:  Sistema de gerenciamento de clientes, pedidos e equipamentos para a empresa Mamô.

Objetivo: O projeto tem como objetivo facilitar a organização das reservas e o controle operacional da empresa, substituindo controles informais por um sistema centralizado.

Funcionalidades

Cadastro e consulta de clientes.
Cadastro e gerenciamento de pedidos.
Acompanhamento do status dos pedidos.
Controle de barris de chopp.
Controle de máquinas.
Cálculo de lucro estimado por pedido.
Painel inicial com resumo dos pedidos.

Tecnologias utilizadas

Python
Flask
Flask-SQLAlchemy
PostgreSQL
SQLite para testes automatizados
HTML, CSS e Bootstrap
Pytest
Requisitos

Python 3.11 ou superior
Git
Banco de dados PostgreSQL
Instalação

Clone o repositório:

git clone https://github.com/andressasiqueirra/mamo.git
cd Mamô 
Crie e ative o ambiente virtual no Windows:

python -m venv .venv
.\.venv\Scripts\Activate.ps1
Instale as dependências:

pip install -r requirements.txt
Configuração do banco de dados

Crie um arquivo .env na raiz do projeto e configure a variável:

DATABASE_URL=postgresql+psycopg2://USUARIO:SENHA@HOST/BASE?sslmode=require
Substitua os valores de exemplo pelas credenciais do seu banco PostgreSQL.

Inicialize as tabelas:

python -m app.database.init_db
Executar o sistema

python -m app.main
Acesse no navegador:

http://127.0.0.1:5000
Executar os testes

pytest -v
Os testes automatizados utilizam SQLite em memória, sem alterar os dados do banco PostgreSQL de desenvolvimento.

Estrutura do projeto

Mamô /
├── app/
│   ├── database/
│   ├── models/
│   ├── services/
│   ├── static/
│   ├── templates/
│   ├── __init__.py
│   ├── main.py
│   └── routes.py
├── tests/
├── .env
├── .gitignore
├── pytest.ini
├── requirements.txt
└── README.md
