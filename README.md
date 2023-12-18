# Sistema de Biblioteca - Projeto Final da Disciplina

## Descrição do Sistema para o Trabalho Prático

### 1. Objetivo
Neste trabalho prático, o objetivo é projetar e implementar um sistema de biblioteca de porte muito pequeno, proporcionando aos alunos a aplicação prática dos conhecimentos adquiridos em Linguagem de Programação II.

### 2. Visão Geral do Sistema
O sistema de biblioteca gerencia e mantém registros de livros em uma biblioteca acadêmica. Quatro tipos de usuários (alunos, alunos de pós-graduação, técnicos administrativos e professores) podem realizar empréstimos e devoluções. Cada livro possui um código, título, editora, autores, edição e ano de publicação. Os usuários têm regras específicas para empréstimos, com períodos diferentes, conforme a Tabela 1.

#### Tabela 1: Tempo de Empréstimo de Cada Tipo de Usuário

| Tipo de Usuário          | Sigla | Tempo de Empréstimo |
|--------------------------|-------|----------------------|
| Aluno                    | alu   | 5 dias               |
| Aluno de Pós-graduação   | pos   | 10 dias              |
| Técnico Administrativo   | tec   | 14 dias              |
| Professor                | pro   | 21 dias              |

### 3. Funcionalidades
1. **Cadastro de Usuário**
   - Comando: `usu|<código>|add|<tipo>|<nome>`
   - Exemplo: `usu|200|add|pro|Alexsandra Prata`
   - O sistema emite uma mensagem de sucesso ou insucesso.

2. **Alterar usuário **
   - Comando: `usu|<código anterior >|alt|<código novo>|<tipo>|<nome>`
   - Exemplo: `usu|200|alt|201|tec|Alexsandra Melo`
   - O sistema emite uma mensagem de sucesso ou insucesso.   

3. **Excluir usuário **
   - Comando: `usu|exc|<código>`
   - Exemplo: `usu|exc|200`
   - O sistema emite uma mensagem de sucesso ou insucesso.   

4. **Empréstimo de Livros**
   - Comando: `emp|<código_usuario>|<código_livro>`
   - Exemplo: `emp|123|100`
   - O sistema emite uma mensagem de sucesso ou insucesso, indicando o nome do usuário e o título do livro.

5. **Devolução de Livro**
   - Comando: `dev|<código_usuario>|<código_livro>`
   - Exemplo: `dev|123|401`
   - O sistema emite uma mensagem de sucesso ou insucesso, indicando o nome do usuário e o título do livro.

4. **Consultas**
   - a. Consulta de todos os livros cadastrados.
      - Comando: `liv|*`
      - Exemplo: `liv|*`
   - b. Consulta detalhada de um livro.
      - Comando: `liv|<código_livro>`
      - Exemplo: `liv|401`
   - c. Consulta detalhada de um usuário.
      - Comando: `usu|<código_usuario>`
      - Exemplo: `usu|200`

6. **Saída do Programa**
   - Comando: `sai`

### 4. Observações
- As mensagens de insucesso devem incluir informações sobre a causa do problema.
- O sistema registra as operações de empréstimo, devolução e cadastro de usuários.
- Certifique-se de seguir as regras específicas para cada tipo de usuário durante as operações.
