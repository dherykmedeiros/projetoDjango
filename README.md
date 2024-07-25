
# projetoDjango

Este é um projeto básico de cadastro de usuários desenvolvido com o framework Django. O sistema permite o cadastro de usuários com nome, idade e um ID gerado automaticamente como chave primária.

## Funcionalidades

- Cadastro de novos usuários com nome e idade.
- Visualização da lista de usuários cadastrados.


## Tecnologias Utilizadas

- Python
- Django
- SQLite (banco de dados padrão do Django)

## Requisitos

- Python 3.8 ou superior
- Django 3.0 ou superior

## Instalação

1. Clone este repositório:
   \`\`\`bash
   git clone https://github.com/dherykmedeiros/projetoDjango.git
   cd projetoDjango1
   \`\`\`

2. Crie e ative um ambiente virtual:
   \`\`\`bash
   python -m venv venv
   source venv/bin/activate   # Para Linux/Mac
   venv\Scripts\activate      # Para Windows
   \`\`\`

3. Instale as dependências:
   \`\`\`bash
   pip install -r requirements.txt
   \`\`\`

4. Execute as migrações do banco de dados:
   \`\`\`bash
   python manage.py migrate
   \`\`\`

5. Inicie o servidor de desenvolvimento:
   \`\`\`bash
   python manage.py runserver
   \`\`\`

6. Acesse o aplicativo em seu navegador:
   \`\`\`
   http://127.0.0.1:8000/
   \`\`\`

## Estrutura do Projeto

\`\`\`
projetoDjango1/
│
├── manage.py
├── db.sqlite3
├── requirements.txt
├── cadastro_de_usuarios/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── app_cad_usuarios/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── migrations/
│   │   └── __init__.py
│   ├── models.py
│   ├── tests.py
│   ├── urls.py
│   ├── views.py
│   └── templates/
│       └── usuarios/
│           ├── base.html
│           ├── home.html
│           └── usuarios.html
\`\`\`

## Modelos

O modelo de usuário está definido no arquivo \`models.py\` do aplicativo \`app_cad_usuarios\`:

\`\`\`python
from django.db import models

class Usuario(models.Model):
    id_usuario = models.AutoField(primary_key=True)
    nome = models.TextField(max_length=255)
    idade = models.IntegerField()

\`\`\`

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request.
