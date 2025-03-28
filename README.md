1 - Instale todas as dependencias necessarias, são elas: pandas ; openpyxl ; mysql-connector-python ; sqlalchemy ; pymysql ; requests ; xlrd ; dash ; cryptography
este passo pode ser executado com "pip% install pandas openpyxl mysql-connector-python sqlalchemy pymysql requests xlrd dash cryptography" caso realizar a instalação pelo proprio código, lembre-se de abrir como adminstrador .

2 - Realize todos as importações dentro do código

3 - faça o download via api dos arquivos em excel, caso a api pare de funcionar deixei o os arquivos na pasta backup, somente arraste eles para a pasta dados e siga com o tutorial

4 - Criar o banco de dados e conectar-se com ele, no código há dois trechos, o primeiro com conexão para SQL Server e o segundo com conexão para MySQL, escolha somente um dos dois trechos para rodar e ignore o outro, não esqueça de mudar as informações nas variaveis de conexão

5 - Execute a parte de limpeza e exportação dos dados até fim, no final faça a verificação de dados com os testes que deixei para garantir que os dados foram exportados corretamente.

6 - Execute a parte de criação do dashboard

7 - acesse http://127.0.0.1:8050/ no navegador para efetivamente visualizar o dashboard, faça uso da filtragem de ano e país e também das ferramentas do proprio Dash, como a exportação em png do grafico. Lembrando que a navegação para as outras paginas está na parte superior.

Qualquer duvida, contatar no email : gabriel_o_tech@outlook.com

Obrigado!