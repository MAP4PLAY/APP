🛠 Passo a Passo de Instalação e Configuração
1. Ambiente de Servidor e Banco de Dados
XAMPP: Baixe e instale o XAMPP. Mova todos os seus arquivos PHP (conexao_pg.php, config.php, api_quadras_pg.php, etc.) para a pasta C:\xampp\htdocs\map4play.

PostgreSQL + PostGIS:

Instale o PostgreSQL e o pgAdmin.

No pgAdmin, crie um banco chamado map4play.

Abra a Query Tool no banco e execute: CREATE EXTENSION postgis; para habilitar funções geográficas como ST_Distance e ST_DWithin.

Execute o conteúdo do seu arquivo database.sql para criar a tabela quadras com as colunas de acessibilidade, iluminação e localização.

Configuração de Senha: Abra o arquivo config.php e altere o campo 'password' para a nova senha que você definiu na instalação do PostgreSQL.

2. Ambiente de Desenvolvimento Mobile (Node.js & Expo)
Node.js: Instale a versão LTS. Isso corrigirá o erro de comando npx não reconhecido que você teve anteriormente.

Dependências: No terminal, dentro da pasta APP-main, execute:

Bash

npm install
npx expo install react-native-maps expo-location
Isso instalará as bibliotecas necessárias para o mapa e o GPS do celular.

3. Configuração do Android Studio (Emulador)
SDK: No Android Studio, vá em Settings > Android SDK. Clique em Edit e defina um caminho (ex: C:\Android\SDK). Não instale na raiz C:\.

Variáveis de Ambiente: Adicione o caminho do SDK às variáveis de ambiente do Windows (ANDROID_HOME) para que o Expo reconheça o emulador.
1. Colocando o Servidor para Rodar
Copie seus arquivos PHP para a pasta C:\xampp\htdocs.

O arquivo config.php já está pronto para conectar ao seu banco de dados.

O arquivo .htaccess vai proteger suas senhas automaticamente para ninguém de fora ver.

2. Ligando o Aplicativo
Abra uma pasta preta (Terminal/PowerShell) na pasta Map4PlayApp.

Digite npm install e espere as barras carregarem.

Descubra o endereço do seu computador na rede (digite ipconfig no terminal e procure por "IPv4").

No arquivo App.js, troque o endereço IP pelo seu número encontrado.

3. Comando para abrir no celular
Digite npx expo start no computador.

Instale o app Expo Go no seu celular (Android ou iPhone).

Abra o Expo Go e leia o código quadrado (QR Code) que apareceu na tela do computador.

🧐 O que o App faz?
Mostra Quadras Perto de Você: O app usa o GPS do celular para achar as quadras no banco de dados.

Filtra por Zona: Você pode escolher ver só quadras da Zona Leste ou Zona Sul, por exemplo.

Inclusão: O mapa avisa se a quadra tem rampa ou banheiro adaptado.

Segurança: Seus dados estão protegidos por um sistema que bloqueia curiosos no servidor.

🆘 Problemas Comuns
O celular não conecta: Verifique se o celular e o computador estão no mesmo Wi-Fi.

Erro de Banco: Verifique se a senha no config.php é a mesma que você colocou no PostgreSQL.

MAP 4 PLAY © 2025 - Desenvolvido pela Equipe de alunos na UNIVESP.
