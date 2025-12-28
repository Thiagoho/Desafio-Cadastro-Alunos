#Projeto: Cadastro de Alunos - Spring Boot

Este projeto tem como objetivo criar uma API simples para **cadastro e listagem de alunos** utilizando o framework **Spring Boot** com o padrão arquitetural **MVC (Model-View-Controller)**.

---

## Tecnologias Utilizadas
- Java 21+
- Spring Boot
- Spring Web
- Spring Data JPA
- Banco de Dados H2 (ou MySQL)
- Maven
- Swagger UI

## Estrutura do Projeto
src/main/java/com/Cadastro/Aluno/<br>
├── model/ # Entidade Aluno<br>
├── repository/ # Interface que acessa o banco<br>
├── controllers/ # Endpoints para cadastro e listagem<br>
└── Application.java # Classe principal
##
---
## Listar todos os alunos cadastrados<br>
Método: GET<br>
Rota: /aluno<br>
Resposta: Lista com todos os alunos no banco<br>
Explicação das Camadas<br>
model/Aluno.java<br>
Representa a entidade Aluno com os atributos:<br>

matricula (chave primária, gerada automaticamente)<br>
nome<br>
idade<br>
repository/AlunoRepository.java<br>
Interface que estende JpaRepository, permitindo:<br>
Salvar, buscar e listar alunos sem escrever SQL manualmente.<br>
controllers/AlunoController.java<br>
Controlador que expõe os endpoints HTTP REST:<br>
@PostMapping: cadastra novo aluno.<br>
@GetMapping: retorna todos os alunos.<br>
Como Executar o Projeto<br>
Clone o repositório:<br>
git clone https://github.com/seu-usuario/cadastro-aluno.git<br>
Abra no Eclipse, IntelliJ ou VS Code com suporte ao Spring Boot.<br>
Rode o projeto pela classe Application.java ou use:<br>
./mvnw spring-boot:run<br>
Teste os endpoints com Postman, Insomnia ou navegador (GET).<br>
## Funcionalidades

### Criar um novo aluno

- **Método**: `POST`
- **Rota**: `/aluno`
- **Corpo da requisição (JSON)**:

```json
{
  "nome": "Thiago Henrique",
  "idade": 36
}
{
  "matricula": 1,
  "nome": "Thiago henrique",
  "idade": 36
}





