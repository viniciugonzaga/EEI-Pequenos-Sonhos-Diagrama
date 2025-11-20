# Funcionalidades e Interações (Diagrama de Casos de Uso)

## Objetivo do Diagrama

Este Diagrama de Casos de Uso (UML) define as **fronteiras** do sistema "Escola Pequenos Sonhos", identificando os **atores** (usuários) e as **funcionalidades** (casos de uso) que eles podem realizar. Ele serve como um mapa de alto nível dos requisitos funcionais do projeto.

## Atores do Sistema

O sistema interage com quatro atores principais, organizados por herança (generalização):

* **Visitante:** O ator base, que pode se tornar Professor ou Responsável.
* **Secretário:** Responsável pelas tarefas administrativas e de gestão do sistema.
* **Professor:** Responsável pelas tarefas pedagógicas e de comunicação.
* **Responsável:** Pais ou guardiões que buscam informações e se comunicam.

## Casos de Uso Principais (Funcionalidades)

As funcionalidades do sistema estão agrupadas por responsabilidade:

### 1. Funcionalidades do Secretário (Gestão Completa)

O Secretário é o ator com mais permissões, sendo responsável pela manutenção de todas as entidades principais do sistema:
* **Manter Cardápio**
* **Manter Eventos e Festa**
* **Manter Professor**
* **Manter Classe**
* **Manter Responsável**

### 2. Funcionalidades do Professor

O Professor foca na comunicação e em um perfil de acesso:
* **Fazer Login do Professor**
* **Gerenciar Mensagens para Responsável**

### 3. Funcionalidades do Responsável

O Responsável foca na consulta de informações:
* **Fazer Login do Responsável**
* **Visualizar Eventos e Festas**
* **Visualizar Mensagens**

### 4. Funcionalidades do Visitante (Sem Login)

* **Acessar as Informações da Escola**
* **Realizar Cardápio** (Consulta)
* **Visualizar Cardápio**

## Relacionamentos Chave

O diagrama utiliza o relacionamento $\ll include \gg$ (inclusão) para mostrar a dependência entre os casos de uso:

* **«include» Login:** Tanto o "Fazer Login do Professor" quanto o "Fazer Login do Responsável" **incluem** o caso de uso **Utilizar Perfil**. Isso significa que, ao fazer o login, o sistema sempre executa a verificação e o carregamento do perfil.
* **«include» Visualização:** A funcionalidade "Manter Responsável" (Secretário) **inclui** a **Visualizar Eventos e Festas**, o que sugere que a gestão do Responsável está ligada à visualização desses dados.
