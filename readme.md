# Mini curso Rocketseat - 48h de rocketseat gratuita

## aula 01 - Intro Python e Flask
Já tinha realizado esse primeiro contato, com NLW em Python

## aula 02 - Roteamento e Modelos
Primeira vez criando e conigurando um BD emn SQLite

## aula 03 - Integração de BD e Autenticação do Usuário
## aula 04 - API de e-commerce
## aula 05 - Tópicos Avançados e Implantação



**Swagger** - ferramenta para documentar APIs

<!-- Se já tiver arquivo -->
pip3 install -r 
 
<!-- pip3 install Flask==2.3.0 -->
cria arquivo e instala os pacotes

## BD 
Object Relative Mapper - camada de abstração do BD 
**SQLite(ORM)** - armazenado em um arquivo de texto. Não tem um servidor para armazenar.
Possui limitações de registro e leitura. Não tem operarações paralelas na modificação do arquivo.


## Commands to create a DB 
flask shell
 - db.create_all()
 - db.session_commit()
 - exit()


## Commands to create a User in DB 
flask shell
 - db.drop_all() -- Deleta tudo
 - db.create_all()
 - db.session.commit()
 - exit()

flask shell
 - db.drop_all() -- Deleta tudo
 - db.create_all()
 - user = User(username="admin", password="123")
 - db.session.add(user)
 - db.session.commit()
 - exit()


from flask_login import 
 UserMixin = método adicional com utilidades para a tabela do usuário (    """
    This provides default implementations for the methods that Flask-Login
    expects user objects to have.
    """
    ), 
 login_user = função que loga o user, 
 LoginManager = função que realiza a condição para verificar se user esta logado, 
 login_required = metodo com utilidades para verificar se user esta logado, 
 logout_user = método que desloga usuário, 
 current_user - traz dados do user logado

<!-- Flask migrate é usado para realizar a migração quando ja tem dados -->

<!-- CRIA PARAMETROS 1 TIPO E A CHAVE -->
@app.route('/api/products/delete/<int:product_id>', methods=["DELETE"])

<!-- Response -->
product = Product.query.get(product_id)
127.0.0.1 - - [24/May/2024 20:00:51] "DELETE /api/products/delete/3 HTTP/1.1" 200 -

<!-- Flask Login -->
Usando Herança no  flask_login para usar a classe UserMixin contendo features pra usarmos




## Usando AWS Cloud para production
- AWS Free tier - tem que cadastrar cartão para usar o free

CONSOLE/TERMINAL(**AWS CLI**) - DASHBOARD.
 - aws cli install
 - aws Elastic Beanstalk
 - EB CLI SETUP (Instalar EB CLI para rodar mais comandos) - escolher por scripts de configuração **GITHUB**


MENU (services)
 - IAM
 - Users (create user)
 - Com o usuario criado - nele temos a aba SECURITY CREDENTIALS (Access Key) Guardar chave 

*google*: 
aws cli <beanstack>

 AWS CLI
  - whick aws (/bin/aws)
  - aws --version
  - aws configure
   - access key
   - secret key
   - def region_name(us-east-1)[enter]
   -[enter]

Vamos Rodar o python com o eb cli
<!-- Navegar na pasta clonada do github -->
aws-elastic-beanstak-cli-setup
git clone https://github.com/aws/aws-elastic-beanstalk-cli-setup.git
cd <pastaclonada>
cd *scripts
ls
 - ebcli_installler.py
 python <nomedoarquivo> 
python ./aws-elastic-beanstalk-cli-setup/scripts/ebcli_installer.py


<!-- Dentro da pasta do projeto -->
 EB CLI + Python
  - eb --version
  - eb init -p python3.11 <flask-tutorial> --region us-east-1

CRIANDO OS ENVIROMENTS
 - eb create flash-env-dev
 - eb open flask-env-dev

 Obs: ta sem rota /
 vai dar 404