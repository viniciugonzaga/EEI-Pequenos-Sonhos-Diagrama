# Estrutura de Dados e Classes (Diagrama de Classes)

## Objetivo do Diagrama

Este Diagrama de Classes (UML) modela a **estrutura estática** do sistema de gerenciamento da Escola de Educação Infantil. Ele define as entidades (classes), seus atributos (dados), seus métodos (comportamentos) e, fundamentalmente, os **relacionamentos** entre elas.

##  Classes Principais e Estruturais

O modelo é construído em torno das seguintes classes e seus agrupamentos:

### 1. Classes de Usuário (Atores do Sistema)

* **Visitante (Base):** A classe fundamental que provavelmente é herdada pelas outras.
    * **Atributos:** `id`, `senha`, `nivel`, etc.
* **Responsável:** Classe para pais/guardiões.
* **Professor:** Classe com atributos e métodos específicos para docência (`disciplinas`, `LigarAluno`).
* **Secretaria:** Classe com foco na gestão administrativa (`GerenciarProfessor`, `CadastrarAluno`).

### 2. Classes de Interface/Fluxo

* **Dashboard:** O ponto central de navegação no sistema.
    * Possui especializações para cada perfil: `SecretariaDashboard`, `ResponsavelDashboard`, e `ProfessorDashboard`.

### 3. Classes de Dados e Registros

* **Aluno:** Informações detalhadas do estudante (`turma`, `alergias`, `getInformacoes`).
* **Classe:** Informações sobre as turmas (`nivel`, `sala`).
* **Matricula:** Detalha o registro do aluno no sistema (`dataMatricula`, `cancelar`, `confirmar`).
* **Transporte:** Informações sobre o serviço de transporte escolar.
* **Feedback:** Registro de feedback de um Responsável.

### 4. Classes de Atividades e Documentação

* **Chamada:** Registro de presença e ausência.
* **PlanoAtividades:** Documentação do planejamento pedagógico.
* **Cadastros:** `CadastroProfessor` e `CadastroEquipe` (para gerenciar dados internos).
* **Cardapio / DocCardapio:** Estrutura para a documentação e detalhamento do cardápio escolar.
* **Refeicao:** Detalhamento dos tipos de refeição.

##  Relacionamentos Chave (Associações)

O diagrama mostra as conexões vitais entre as classes, definidas por cardinalidades (ex: $1..*$ um para muitos):

* Um **Professor** está associado a múltiplas **Classes** e múltiplos **Alunos**.
* Uma **Matricula** está ligada a exatamente um **Aluno** e uma **Classe**.
* Um **Responsável** pode enviar $0$ ou muitos **Feedbacks**.
* A **Secretaria** e os **Professores** interagem com as classes de **Cadastro** para manutenção dos dados.