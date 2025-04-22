# site-simples-com-html-e-css

Como criar um script para automatizar a instalação do apache2, juntamente com a criação, configuração e execução deste.

Step 1: Deve ser criado um arquivo utilizando o comando nano, o comando vai permitir a edição e deve ser colocado "#! /bin/bash" para representar que é um script;
Step 2: Verificar se o apache2 está instalado, utilizando o comando if na linha de código "if [ ! -x /etc/init.d/apache2 ] (onde a ! representa negação e o -x representa a execução), caso (then) não seja possível encontrar/executar o arquivo, as linhas de código "sudo apt-get update" e em seguida "sudo apt-get install apache2 -y" (onde -y irá confirmar algum pedido) irão instalar o apache2;
Step 3: Caso o apache2 já esteja instalado, o continuação else vai apenas informar (via comando echo) que já está instalado e finalizar o if com a linha "fi";
Step 4: Utilizando da linha de código "sudo mkdir -p /var/www/aluno/public_html" vai ser criado o diretório, e após isso, utiliza-se do "cd" para acessar esse mesmo diretório;
Step 5: Usando o comando "git clone https://github.com/link-do-codigo-git.git" vai ser clonado esse repositório no diretório que foi aberto;
Step 6: Copie o repositório criado no diretório já aberto utilizando da linha de código "sudo cp -r link-do-codigo-git/* . , onde "/* ." quer dizer que TUDO (/*) vai ser copiado pro diretório atual (.);


# Preview
![Como-Criar-um-SITE-Com-HTML-e-CSS-na-prática](/Como-Criar-um-SITE-Com-HTML-e-CSS-na-prática.png)
