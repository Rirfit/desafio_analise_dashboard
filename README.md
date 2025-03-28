0 - As instruções deste documento serão realizadas ou dentro do arquivo main.ipynb ou dentro do prompt de comando (cmd).

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





<b>Certifique-se de que suas bibliotecas estejam nestas versões ou superiores:</b>

Requirement already satisfied: pandas in c:\python312\lib\site-packages (2.2.3)Note: you may need to restart the kernel to use updated packages.

Requirement already satisfied: openpyxl in c:\python312\lib\site-packages (3.1.5)
Requirement already satisfied: mysql-connector-python in c:\python312\lib\site-packages (9.2.0)
Requirement already satisfied: sqlalchemy in c:\python312\lib\site-packages (2.0.39)
Requirement already satisfied: pymysql in c:\python312\lib\site-packages (1.1.1)
Requirement already satisfied: requests in c:\python312\lib\site-packages (2.32.3)
Requirement already satisfied: xlrd in c:\python312\lib\site-packages (1.2.0)
Requirement already satisfied: dash in c:\python312\lib\site-packages (3.0.1)
Requirement already satisfied: cryptography in c:\python312\lib\site-packages (44.0.2)
Requirement already satisfied: numpy>=1.26.0 in c:\python312\lib\site-packages (from pandas) (2.2.4)
Requirement already satisfied: python-dateutil>=2.8.2 in c:\python312\lib\site-packages (from pandas) (2.9.0.post0)
Requirement already satisfied: pytz>=2020.1 in c:\python312\lib\site-packages (from pandas) (2025.1)
Requirement already satisfied: tzdata>=2022.7 in c:\python312\lib\site-packages (from pandas) (2025.2)
Requirement already satisfied: et-xmlfile in c:\python312\lib\site-packages (from openpyxl) (2.0.0)
Requirement already satisfied: greenlet!=0.4.17 in c:\python312\lib\site-packages (from sqlalchemy) (3.1.1)
Requirement already satisfied: typing-extensions>=4.6.0 in c:\python312\lib\site-packages (from sqlalchemy) (4.12.2)
Requirement already satisfied: charset-normalizer<4,>=2 in c:\python312\lib\site-packages (from requests) (3.4.0)
Requirement already satisfied: idna<4,>=2.5 in c:\python312\lib\site-packages (from requests) (3.10)
Requirement already satisfied: urllib3<3,>=1.21.1 in c:\python312\lib\site-packages (from requests) (2.2.3)
Requirement already satisfied: certifi>=2017.4.17 in c:\python312\lib\site-packages (from requests) (2024.8.30)
Requirement already satisfied: Flask<3.1,>=1.0.4 in c:\python312\lib\site-packages (from dash) (3.0.3)
Requirement already satisfied: Werkzeug<3.1 in c:\python312\lib\site-packages (from dash) (3.0.6)
Requirement already satisfied: plotly>=5.0.0 in c:\python312\lib\site-packages (from dash) (6.0.1)
Requirement already satisfied: importlib-metadata in c:\python312\lib\site-packages (from dash) (8.6.1)
Requirement already satisfied: retrying in c:\python312\lib\site-packages (from dash) (1.3.4)
Requirement already satisfied: nest-asyncio in c:\python312\lib\site-packages (from dash) (1.6.0)
Requirement already satisfied: setuptools in c:\python312\lib\site-packages (from dash) (75.2.0)
Requirement already satisfied: cffi>=1.12 in c:\python312\lib\site-packages (from cryptography) (1.17.1)
Requirement already satisfied: pycparser in c:\python312\lib\site-packages (from cffi>=1.12->cryptography) (2.22)
Requirement already satisfied: Jinja2>=3.1.2 in c:\python312\lib\site-packages (from Flask<3.1,>=1.0.4->dash) (3.1.4)
Requirement already satisfied: itsdangerous>=2.1.2 in c:\python312\lib\site-packages (from Flask<3.1,>=1.0.4->dash) (2.2.0)
Requirement already satisfied: click>=8.1.3 in c:\python312\lib\site-packages (from Flask<3.1,>=1.0.4->dash) (8.1.8)
Requirement already satisfied: blinker>=1.6.2 in c:\python312\lib\site-packages (from Flask<3.1,>=1.0.4->dash) (1.9.0)
Requirement already satisfied: narwhals>=1.15.1 in c:\python312\lib\site-packages (from plotly>=5.0.0->dash) (1.32.0)
Requirement already satisfied: packaging in c:\python312\lib\site-packages (from plotly>=5.0.0->dash) (24.1)
Requirement already satisfied: six>=1.5 in c:\python312\lib\site-packages (from python-dateutil>=2.8.2->pandas) (1.16.0)
Requirement already satisfied: MarkupSafe>=2.1.1 in c:\python312\lib\site-packages (from Werkzeug<3.1->dash) (3.0.1)
Requirement already satisfied: zipp>=3.20 in c:\python312\lib\site-packages (from importlib-metadata->dash) (3.21.0)
Requirement already satisfied: colorama in c:\python312\lib\site-packages (from click>=8.1.3->Flask<3.1,>=1.0.4->dash) (0.4.6)