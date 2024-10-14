Sistema de Pesquisa de Clima Organizacional

![2](https://github.com/user-attachments/assets/b3985546-f616-4f18-8fa7-52ebd6bd7810)

![1](https://github.com/user-attachments/assets/fbfd49af-d06b-4ec7-a009-d064a724738b)

Descrição do Projeto:
Este sistema de pesquisa de clima organizacional permite que uma empresa colete e analise respostas de seus funcionários sobre o ambiente de trabalho. Os funcionários podem responder a 10 perguntas-chave, cujas respostas são armazenadas em um banco de dados SQLite. O sistema oferece funcionalidades de login e cadastro de usuários, onde cada funcionário se cadastra com sua matrícula e empresa.

O sistema foi desenvolvido usando:

Frontend: HTML, CSS, JavaScript e Bootstrap.
Backend: Java (Spring Boot) para lidar com autenticação e salvar respostas no banco de dados.
Banco de Dados: SQLite para armazenar informações de usuários, suas respostas e perguntas.
Funcionalidades
Cadastro de Usuário: Cada funcionário pode se cadastrar informando nome, email, senha, matrícula e empresa.
Login de Usuário: Autenticação por email e senha.
Sistema de Perguntas: O sistema apresenta 10 perguntas-chave sobre o clima organizacional, exibindo uma pergunta por vez.
Armazenamento de Respostas: As respostas dos funcionários são armazenadas no banco de dados SQLite, junto com sua matrícula e empresa.
Interface Responsiva: Utilizando Bootstrap, o sistema é otimizado para dispositivos móveis e desktops.
Estrutura do Projeto
Frontend
O frontend é composto de:

HTML para a estrutura da página.
CSS e Bootstrap para estilização e responsividade.
JavaScript para controlar a navegação entre perguntas, login e envio de respostas.
Backend
O backend foi desenvolvido usando Java Spring Boot, com endpoints REST para lidar com:

/usuarios/login: Login dos funcionários.
/usuarios/cadastro: Cadastro de novos usuários.
/pesquisas/responder: Salvamento de respostas de cada pergunta.
Banco de Dados
O banco de dados utilizado é o SQLite. O schema inicial do banco de dados é:

Tabela usuarios: Armazena nome, email, senha (hasheada), matrícula e empresa.
Tabela respostas: Armazena as respostas de cada funcionário para cada pergunta.
Tecnologias Utilizadas
Frontend:

HTML5
CSS3
JavaScript (ES6)
Bootstrap 5
Backend:

Java 11 (Spring Boot)
SQLite
Requisitos do Sistema
Java 11 ou superior
Maven 3.6+ (para gerenciamento de dependências)
SQLite (integrado via JDBC)
Como Rodar o Projeto Localmente
Clonando o Repositório
bash
git clone https://github.com/seu-usuario/sistema-pesquisa-clima-organizacional.git
cd sistema-pesquisa-clima-organizacional
Executando o Backend (Java Spring Boot)
Certifique-se de ter o Java e Maven instalados.
No diretório do projeto, rode o seguinte comando para iniciar o servidor:
bash
mvn spring-boot:run
O backend estará rodando em http://localhost:8080.

