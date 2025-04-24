# site-simples-com-html-e-css

Como criar um script para automatizar a instalação do apache2, juntamente com a criação, configuração e execução deste.

Step 1: Deve ser criado o arquivo "script.sh" utilizando o comando nano, o comando vai permitir a edição e deve ser colocado "#! /bin/bash" para representar que é um script;

Step 2: Verificar se o apache2 está instalado, utilizando o comando if na linha de código "if [ ! -x /etc/init.d/apache2 ] (onde a ! representa negação e o -x representa a execução), caso (then) não seja possível encontrar/executar o arquivo, as linhas de código "sudo apt-get update" e em seguida "sudo apt-get install apache2 -y" (onde -y irá confirmar algum pedido) irão instalar o apache2;

Step 3: Caso o apache2 já esteja instalado, o continuação else vai apenas informar (via comando echo) que já está instalado e finalizar o if com a linha "fi";

Step 4: Utilizando da linha de código "sudo mkdir -p /var/www/aluno/public_html" vai ser criado o diretório, e após isso, utiliza-se do "cd" para acessar esse mesmo diretório;

Step 5: Usando o comando "sudo git clone https://github.com/link-do-codigo-git.git" vai ser clonado esse repositório no diretório que foi aberto;

Step 6: Copie o repositório criado no diretório já aberto utilizando da linha de código "sudo cp -r link-do-codigo-git/* . , onde "/* ." quer dizer que TUDO (/*) vai ser copiado pro diretório atual (.);

Step 7: Após isso pode dar uma "sudo rm -rf link-do-codigo-git/" para excluir o diretório;

Step 8: Acesse o diretório /etc/apache2/sites-available por meio do comando cd;

Step 9: Crie um arquivo via "sudo tee aluno.conf" e insira "<<EOF" na mesma linha;

Step 10: Na linha seguinte coloque as informações "
<VirtualHost *:80>
    ServerAdmin admin@aluno
    ServerName aluno
    ServerAlias www.aluno
    DocumentRoot /var/www/aluno/public_html
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</Virtualhost> 
" e finaliza com "EOF";

Step 11: Agora para ativar o site vai precisar utilizar o código "sudo a2ensite aluno.conf";

Step 12: Insere a linha de código "sudo echo "127.0.0.1 aluno" | sudo tee -a /etc/hosts";

Step 13: Faça o restart do apache2 utilizando "sudo /etc/init.d/apache2 restart" e salve o script utilizando Ctrl + X;

Step 14: Altere as permissões do script com "sudo chmod +x script.sh";

Step 15: Execute o script utilizando o comando "./script.sh".

# Preview
![Como-Criar-um-SITE-Com-HTML-e-CSS-na-prática](/Como-Criar-um-SITE-Com-HTML-e-CSS-na-prática.png)
