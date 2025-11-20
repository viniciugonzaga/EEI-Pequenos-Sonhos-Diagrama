# ⏳ Fluxos de Interação Detalhados (Diagrama de Sequência)

## Objetivo do Diagrama

Este Diagrama de Sequência (SD) detalha a **ordem cronológica** e as **interações** entre os diferentes atores (Usuário, Responsável, Professor) e os objetos do sistema (Sistema, BD, Relatório) ao longo de fluxos específicos, como Login e funcionalidades críticas.

## Atores e Componentes (Linhas de Vida)

O diagrama envolve os seguintes participantes:

* **Atores:** Usuário (Geral), Responsável, Professor.
* **Componentes:** Sistema (Controlador principal), BD (Banco de Dados), RD (Geração de Relatórios).

## 🚀 Fluxos Modelados

O diagrama aborda diversas interações chave do sistema:

### 1. Fluxo de Login (Itens 1-9)

* **Início:** Demonstra o processo de Login, onde o usuário insere as credenciais (via "Sistema").
* **Validação:** O Sistema consulta o **BD** ("Validar Login") para checar as credenciais.
* **Resultado:** O sistema retorna a validação e, em caso de sucesso, direciona o usuário para o *Dashboard* apropriado (ex: "Dashboard Responsável").

### 2. Fluxos de Consulta e Gestão (Itens 10 em diante)

O diagrama ilustra interações específicas, como:

* **Consulta do Responsável:** O Responsável consulta informações, o Sistema busca as informações solicitadas no **BD** ("Buscar Dados do Aluno") e as retorna.
* **Gestão de Professores:** Detalha como o sistema lida com o "Remover Prof/Usuário" e "Ativar/Desativar Professor", interagindo com o **BD** para atualizar o cadastro.
* **Geração de Relatórios:** Mostra a interação direta com o objeto **RD** ("Gerar Relatórios") para atender a solicitações de consultas e relatórios.

## Foco do Detalhamento

O Diagrama de Sequência é essencial para entender:

* A **sequência exata de mensagens** trocadas para completar uma tarefa.
* Qual componente (Sistema, BD, RD) é **responsável** por cada etapa da operação.

