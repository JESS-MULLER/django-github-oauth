
# TECH - Autenticação OAuth 2.0 com GitHub

Aplicação web desenvolvida em Django demonstrando a implementação de autenticação social via protocolo OAuth 2.0 integrado ao GitHub utilizando o pacote `django-allauth`, com rotas restritas e gerenciamento seguro de credenciais via variáveis de ambiente.

---

## 🚀 Funcionalidades

- **Autenticação Social:** Login rápido e seguro utilizando a conta do GitHub via OAuth 2.0.
- **Área Restrita:** Controle de acesso para membros autenticados (`/members/`), redirecionando visitantes não autorizados.
- **Segurança de Credenciais:** Separação estrita de segredos e chaves de API do código-fonte através do `python-dotenv`.
- **Interface Integrada:** Templates dinâmicos em Django consumindo arquivos estáticos e contexto de autenticação.

---

## 🛠️ Tecnologias Utilizadas

- [Python 3.12](https://www.python.org/)
- [Django 6.1.2](https://www.djangoproject.com/)
- [django-allauth](https://docs.allauth.org/)
- [python-dotenv](https://github.com/theskumar/python-dotenv)


---

## ⚙️ Configuração e Instalação

Siga os passos abaixo para executar a aplicação localmente:

### 1. Clonar o repositório
```bash
git clone [https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git](https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git)
cd TECH
2. Criar e ativar o ambiente virtual
Windows (PowerShell):

PowerShell
python -m venv venv
.\venv\Scripts\Activate.ps1
Linux/macOS:

Bash
python3 -m venv venv
source venv/bin/activate
3. Instalar as dependências
Bash
pip install -r requirements.txt
4. Configurar as variáveis de ambiente
Crie um arquivo chamado .env na raiz do projeto tomando como base o .env.example:

Bash
cp .env.example .env
Preencha os valores dentro do .env:

Ini, TOML
SECRET_KEY=sua_secret_key_aqui
DEBUG=True
GITHUB_CLIENT_ID=seu_client_id_do_github
GITHUB_SECRET_KEY=seu_client_secret_do_github
Nota: Para obter as credenciais do GitHub, crie uma OAuth App em GitHub > Settings > Developer settings > OAuth Apps, definindo a Authorization callback URL como http://localhost:8000/accounts/github/login/callback/.

5. Executar as migrações do banco de dados
Bash
python manage.py migrate
6. Iniciar o servidor de desenvolvimento
Bash
python manage.py runserver
Acesse a aplicação no navegador através de: http://localhost:8000/

📁 Estrutura do Projeto
Plaintext
TECH/
├── setup/            # Configurações globais do Django (settings, urls, wsgi)
├── tech/             # Aplicação principal (views, models, rotas locais)
├── templates/        # Arquivos HTML e parciais
│   ├── static/       # Arquivos estáticos (CSS, imagens, ícones)
│   ├── index.html    # Página inicial pública
│   └── members.html  # Página da área de membros autenticados
├── .env.example      # Modelo de variáveis de ambiente
├── .gitignore        # Arquivos e diretórios ignorados pelo Git
├── manage.py         # Utilitário de linha de comando do Django
├── requirements.txt  # Lista de dependências do projeto
└── README.md         # Documentação do projeto
📝 Licença
Este projeto está sob a licença MIT. Consulte o arquivo LICENSE para mais detalhes.


---

### Como versionar o arquivo adicionado:

No terminal com o ambiente ativado, adicione e envie o novo arquivo para o repositório:

```powershell
git add README.md
git commit -m "docs: adiciona README com instrucoes de instalacao e uso"
git push origin main
