🛠️ O que você vai precisar instalar?
XAMPP: É o que faz o seu computador virar um servidor de internet.

PostgreSQL: É a gaveta onde guardamos todas as informações das quadras.

Node.js: É a ferramenta necessária para rodar o aplicativo de celular.

🚀 Passo a Passo (Do zero ao App)
1. Preparando o Banco de Dados (PostgreSQL)
Instale o PostgreSQL e use a senha 827#asimov (como definido no seu código).

Crie um banco de dados chamado map4play.

Dica de mestre: Você precisa ativar a função de "mapa" no banco. Abra a ferramenta de texto (Query Tool) e digite: CREATE EXTENSION postgis;.

2. Colocando o Servidor para Rodar
Copie seus arquivos PHP para a pasta C:\xampp\htdocs.

O arquivo config.php já está pronto para conectar ao seu banco de dados.

O arquivo .htaccess vai proteger suas senhas automaticamente para ninguém de fora ver.

3. Ligando o Aplicativo
Abra uma pasta preta (Terminal/PowerShell) na pasta Map4PlayApp.

Digite npm install e espere as barras carregarem.

Descubra o endereço do seu computador na rede (digite ipconfig no terminal e procure por "IPv4").

No arquivo App.js, troque o endereço IP pelo seu número encontrado.

4. Vendo a Mágica no Celular
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
