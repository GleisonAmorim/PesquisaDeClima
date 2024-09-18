Sistema de Pesquisa de Clima Organizacional
Descrição do Projeto
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

Executando o Frontend
Abra o arquivo index.html em um navegador.
Interaja com o sistema normalmente, realizando o login e respondendo às perguntas.
Estrutura do Projeto
bash
.
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── empresa
│   │   │           └── pesquisa
│   │   │               ├── controller
│   │   │               │   └── UsuarioController.java
│   │   │               │   └── PesquisaController.java
│   │   │               ├── model
│   │   │               │   └── Usuario.java
│   │   │               │   └── Resposta.java
│   │   │               ├── repository
│   │   │               │   └── UsuarioRepository.java
│   │   │               │   └── RespostaRepository.java
│   │   │               ├── service
│   │   │               │   └── UsuarioService.java
│   │   │               │   └── PesquisaService.java
│   │   │               └── PesquisaApplication.java
│   └── resources
│       ├── application.properties
│       └── data.sql
└── README.md
Estrutura do Banco de Dados
As tabelas serão criadas automaticamente com o seguinte esquema:

sql
CREATE TABLE usuarios (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    nome TEXT NOT NULL,
    email TEXT NOT NULL UNIQUE,
    senha TEXT NOT NULL,
    matricula TEXT NOT NULL,
    empresa TEXT NOT NULL
);

CREATE TABLE respostas (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    usuario_id INTEGER,
    pergunta TEXT NOT NULL,
    resposta TEXT NOT NULL,
    FOREIGN KEY(usuario_id) REFERENCES usuarios(id)
);
Testando o Sistema
Acesse o frontend (HTML).
Realize o cadastro de um novo usuário.
Efetue o login com o email e senha cadastrados.
Responda às 10 perguntas exibidas.
Verifique as respostas sendo armazenadas no banco de dados.
Melhorias Futuras
Exportação dos resultados da pesquisa em formato Excel ou PDF.
Criação de uma interface administrativa para visualizar e filtrar as respostas coletadas.
Implementação de gráficos e dashboards para análise dos resultados.
Contribuindo
Contribuições são bem-vindas! Sinta-se à vontade para enviar pull requests ou abrir issues para discutir melhorias no projeto.

Fork este repositório.
Crie uma branch com sua nova feature (git checkout -b feature/nova-feature).
Commit suas mudanças (git commit -m 'Adiciona nova feature').
Envie para sua branch (git push origin feature/nova-feature).
Abra um Pull Request.
Licença
Este projeto está licenciado sob a Licença MIT.
