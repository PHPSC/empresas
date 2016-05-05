INBEP
-----
http://inbep.com.br

- PHP5.6, PHP7
  - Composer
  - Silex
  - Phing
  - Doctrine (Migrations, ORM, Cache)
  - PHPUnit
  - Symfony Components
  - Monolog
  - Respect (Validation)
  - WordPress
- PostgreSQL, MariaDB, Redis
- Beanstalkd (Message Queues), NGINX
- AWS
- CloudFlare (DNS Zone)

Como Organizamos
----------------
Para os bandos de dados PostgreSQL e MariaDB utilizado o AWS RDS, que cuida dos backups e atualizações dos bancos.

Nossa plataforma fica em uma instancia EC2 junto com o Beanstalkd, responsável por gerenciar a fila de tarefas de latência.

O WordPress (blog) também fica em uma instancia EC2, para facilitar a manutenção, e não afetar nossa plataforma
caso ocorra um volume significarivo de acesso no blog, e não precisamos concorrer com nossa plataforma.
