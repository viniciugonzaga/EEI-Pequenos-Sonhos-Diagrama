# Fluxo de Acesso e Funcionalidades - Projeto IBM

##  Objetivo do Diagrama

Este Diagrama de Atividade modela o **fluxo de controle e as permissões de acesso** do sistema de gerenciamento da Escola de Educação Infantil (Projeto IBM). Ele ilustra as ações que cada tipo de usuário pode realizar após a autenticação.

## 🗝 Fluxo Principal (Login e Decisão)

1.  **Acessar Sistema** $\rightarrow$ **Fazer Login**.
2.  O ponto crucial é a **Validação de Credenciais** (losango), que direciona o usuário para um dos três *dashboards* exclusivos, dependendo do seu perfil:
    * **Professor**
    * **Secretário**
    * **Responsável** (Pais/Guardões)

## Funcionalidades por Perfil

O diagrama segmenta claramente as ações disponíveis:

| Perfil | Ações Exclusivas e Fluxos |
| :--- | :--- |
| **Professor** | Focado em atividades pedagógicas: Consultar Turma, Fazer Chamada e Planejar Atividades. |
| **Secretário** | Focado em gestão administrativa: Gerenciar Alunos, Gerenciar Professores, Enviar Notificações e Atualizar Estatísticas. |
| **Responsável** | Focado em informações do aluno: Consultar Informações, Consultar Aulas e Consultar Eventos. |

## Junção de Dados

As funcionalidades que requerem acesso à base de dados (como Gerenciar Alunos ou Consultar Informações) convergem no ponto **"Disponibilizar BD"**, indicando que essas ações interagem com a camada de dados do sistema.

---
**Status:** Diagrama de Atividade inicial concluído