# Backup-e-Gerenciador-de-Backup-MYSQL

**Como funciona:**

**Backup:**

O sistema de backup permite realizar cópias de segurança de dois bancos de dados distintos. Nele, você configura qual banco deseja salvar e qual nome deseja atribuir ao arquivo gerado.

Cada backup será salvo automaticamente com a data e a hora de sua execução, facilitando a identificação e a organização das cópias.

Como o MySQL exige usuário e senha para acessar o banco de dados, é utilizado o arquivo `mysql.cnf`. Nele, você configura o usuário, a senha e o local do banco de dados. Assim, quando o programa for realizar a cópia, ele utilizará as informações contidas nesse arquivo para acessar o banco e executar o backup.

Caso queira automatizar esse processo para que seja realizado todos os dias, basta configurar a execução no Agendador de Tarefas do Windows.

**Gerenciador de cópias:**

O gerenciador é responsável por controlar a quantidade de backups armazenados, sempre priorizando a exclusão das cópias mais antigas.

Por exemplo: se você configurar o limite para manter 20 cópias, ao ser gerada a 21ª cópia, o sistema excluirá automaticamente a cópia mais antiga, mantendo sempre as 20 cópias mais recentes.

Dessa forma, você mantém um histórico atualizado de backups sem ocupar espaço desnecessário no armazenamento.
