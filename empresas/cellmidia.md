Cellmidia Marketing Digital LTDA
--------------------------------
http://www.cellmidia.com.br

Repositórios em: https://cellmidia.github.io


- PHP7
  - Composer
  - Silex 2
  - Symfony (EventDispatcher, DI, Console)
  - Doctrine (Migrations, ORM, Cache)
  - Willdurand/hateoas
  - Lcobucci (di-builder, jwt)
  - Monolog
  - Respect (Validation)
  - PHPUnit
  - Phing
  - Wordpress
- PHP 5.3 (Legacy)
  - Zend Framework 1.4
- MySQL, Elasticsearch, Redis
- CloudAMQP (Message Queues)
- NGNIX
- Heroku
- AWS SNS/Lambda
- Digital Ocean (Legacy)
- CircleCI

Como Organizamos
----------------
Temos um legado que precisamos manter em php 5.3 com MySQL 5.1 este legado usa a infra de droplets na Digital Ocean.

Os novos projetos e melhorias no legado nascem na nova stack com PHP 7 rodando em micro instancias no Heroku que 
para nós tem se mostrado uma ótima alternativa ao EC2 da AWS.

As filas são gerenciadas pelo CloudAMQP em conjunto com funções lambdas rodando na AWS devido a restrição do Heroku para tarefas de background/Foreground.
Usamos o SNS para notificar os diferentes serviços já que toda a nossa stack é baseada em microserviços.

Os bancos de dados MySQL movemos recentemente para instâncias ClearDB fornecida pela plataforma Heroku, antes eram instancias do Aurora DB na AWS RDS.

O banco relacional é a nossa plataforma de persitência enquanto o ElasticSearch é nosso repositório de dados de onde tiramos todas as estatisticas e relatórios
requeridos por nossos sistemas entre outras atividades.

O WordPress (site e blog) residem em um droplet na Digital Ocean mas em breve será movido para a plataforma do Heroku.

Todos o processo de deploy é orquestrato pelo CircleCI.


Colaboradores
----------------

Trabalham na empresa 2 programadores PHP

Nosso Líder técnico ZCE

- https://github.com/mingomax

