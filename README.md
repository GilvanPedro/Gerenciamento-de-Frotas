# Sistema de Controle de Frotas – GynLog

Aplicação desktop desenvolvida em Java (Swing) seguindo o padrão
arquitetural MVC, permitindo o gerenciamento completo da frota de
veículos da empresa GynLog. O sistema oferece cadastro de veículos,
controle de despesas, registro de movimentações financeiras, geração de
relatórios e exportação de dados para planilhas.

## 📌 Visão Geral

Este sistema foi desenvolvido como parte do Projeto Integrador 2025/2 da
Faculdade SENAI FATESG, contemplando:

-   Elicitação e modelagem de requisitos
-   Modelagem BPMN dos principais processos
-   Diagrama de Classes UML
-   Desenvolvimento de uma aplicação completa em Java/Swing
-   Persistência dos dados em arquivos texto (CSV/TXT)
-   Geração e exportação de relatórios

## 🚀 Funcionalidades Principais

### 🔧 Cadastro de Veículos

-   Inserção, edição e exclusão de veículos
-   Atributos: placa, marca, modelo, ano e status (ativo/inativo)
-   Validação de placa duplicada
-   Organização visual em cartões (UI moderna)

### 🧾 Tipos de Despesas

-   Cadastro e manutenção de categorias (combustível, IPVA, manutenção
    etc.)

### 💰 Movimentações

-   Registro de despesas por veículo
-   Campos: tipo, data, valor e descrição
-   Validação de valores negativos, campos vazios e veículos inativos

### 📊 Relatórios

Geração e exportação dos seguintes relatórios: - Despesas por veículo
- Somatório geral mensal
- Gastos com combustível
- Somatório anual de IPVA
- Multas por veículo
- Listagem de veículos inativos
- Exportação para CSV

### 📂 Persistência

Os dados são armazenados em arquivos texto dentro da pasta dados/:

    dados/
     ├─ veiculos.txt
     ├─ tipos_despesas.txt
     └─ movimentacoes.txt

## 🏛 Arquitetura do Sistema

### 📐 Padrão MVC

-   Model: Classes de Veículo, Movimentação, Despesa
-   View: Interfaces Java Swing (telas, componentes e layouts)
-   Controller: Lógica de negócios, validações e persistência

### 💻 Tecnologias Utilizadas

-   Java 17
-   Maven
-   Java Swing (UI)
-   Java.io para persistência
-   Geração de planilhas e relatórios (CSV)

## 📁 Estrutura do Projeto

    Sistema-De-Frotas/
    ├─ dados/
    │  ├─ movimentacoes.txt
    │  ├─ tipos_despesas.txt
    │  └─ veiculos.txt
    ├─ src/main/java/br/com/
    │  ├─ Main.java
    │  ├─ controller/
    │  ├─ dao/
    │  ├─ model/
    │  ├─ ui/
    │  └─ view/
    ├─ resources/
    ├─ pom.xml
    └─ README.md

## ▶️ Como Executar

### 1️⃣ Via IDE (recomendado)

1.  Importar o projeto como Maven Project
2.  Executar a classe:
    br.com.Main
3.  O sistema abrirá a interface principal em Swing

### 2️⃣ Via terminal

Compilar:

    mvn clean compile

Executar:

    java -cp target/classes br.com.Main

### 3️⃣ Gerar JAR

    mvn clean package

Para execução direta via java -jar, é necessário configurar o manifesto
no pom.xml.

## 📌 Roadmap (Melhorias Futuras)

-   Migração para banco de dados (SQLite, PostgreSQL, H2)
-   Interface modernizada (JavaFX)
-   Sistema com múltiplos usuários e níveis de acesso
-   API para consulta de multas em tempo real
-   Versão Web do sistema (Spring Boot + React)

## 👥 Equipe de Desenvolvimento

-   [Gilvan Pedro de Castro Melo Campos](https://github.com/GilvanPedro)
-   [Sidney Emanuel Barbosa de Oliveira](https://github.com/Sidney-Emanuel-Oliveira)
-   [Guilherme Scarcela Bueno](https://github.com/Scarcela13)
-   [João Paulo Marques Ferreira](https://github.com/Joao-Paulo2007)

## 📄 Licença

Este projeto está sob a licença [MIT](LICENSE).
