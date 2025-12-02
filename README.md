# Sistema de Frotas

Aplicação desktop em Java (Swing) para gestão de frotas: cadastro de veículos, tipos de despesas, registro de movimentações e geração de relatórios. Persistência simples em arquivos texto dentro da pasta `dados/`.

## Visão Geral

- **Tipo de app**: Desktop (Java Swing)
- **Módulos principais**: Veículos, Tipos de Despesas, Movimentações, Relatórios
- **Persistência**: Arquivos `.txt` em `dados/`
- **Ponto de entrada**: `br.com.Main` (inicia `TelaPrincipal`)

## Tecnologias

- **Java 17**
- **Maven** (build e gestão de dependências)

## Requisitos

- JDK 17 instalado (`java -version` deve mostrar 17)
- Maven 3.8+ (`mvn -v`)
- Sistema operacional: Windows, macOS ou Linux

## Como Executar

### 1) IDE (recomendado)

1. Importar o projeto como Maven Project.
2. Localizar a classe `br.com.Main`.
3. Executar o método `main`.

### 2) Linha de comando (sem configurar plugin exec)

1. Compilar o projeto:
   ```bash
   mvn clean compile
   ```
2. Executar a aplicação usando o classpath de `target/classes`:
   ```bash
   java -cp target/classes br.com.Main
   ```

### 3) Gerar artefato (JAR)

```bash
mvn clean package
```

Observação: o `pom.xml` não define `Main-Class` no manifest. Para executar o JAR diretamente (`java -jar ...`), é necessário configurar o plugin apropriado no `pom.xml`. Caso deseje, posso adicionar essa configuração futuramente.

## Estrutura do Projeto

```
Sistema-De-Frotas/
├─ dados/
│  ├─ movimentacoes.txt
│  ├─ tipos_despesas.txt
│  └─ veiculos.txt
├─ src/
│  └─ main/
│     ├─ java/
│     │  └─ br/com/
│     │     ├─ Main.java
│     │     ├─ controller/
│     │     ├─ dao/
│     │     ├─ model/
│     │     ├─ ui/ (componentes e layouts Swing)
│     │     └─ view/ (telas como TelaPrincipal, TelaMovimentacao etc.)
│     └─ resources/
├─ pom.xml
└─ README.md
```

## Funcionalidades

- **Cadastro de Veículos**: criação, edição e listagem.
- **Cadastro de Tipos de Despesas**.
- **Movimentações**: registro e visualização de entradas/saídas.
- **Relatórios**: geração e exportação (ex.: CSV) a partir das movimentações e dados cadastrados.
- **Interface**: componentes visuais customizados (Modern UI) e layout `WrapLayout` para melhor responsividade no Swing.

## Dados e Persistência

- Arquivos texto em `dados/`:
  - `veiculos.txt`
  - `tipos_despesas.txt`
  - `movimentacoes.txt`
- A aplicação lê/escreve diretamente nesses arquivos. Faça backup antes de edições manuais.

## Capturas de Tela

Inclua aqui imagens das telas principais para facilitar o entendimento do uso.

## Roadmap (Ideias Futuras)

- Persistência em banco de dados (ex.: H2, SQLite ou PostgreSQL)
- Empacotamento com manifest `Main-Class` para `java -jar`
- Testes automatizados
- Internacionalização (i18n)
- Melhorias de UX e acessibilidade

## Como Contribuir

1. Faça um fork do repositório
2. Crie um branch: `git checkout -b feature/minha-feature`
3. Commit: `git commit -m "feat: descreva sua mudança"`
4. Push: `git push origin feature/minha-feature`
5. Abra um Pull Request

## Equipe

- Gilvan Pedro de Castro Melo Campos — https://github.com/GilvanPedro
- Sidney Emanuel Barbosa de Oliveira — https://github.com/Sidney-Emanuel-Oliveira
- Guilherme Scarcela Bueno — https://github.com/Scarcela13
- João Paulo Marques Ferreira — https://github.com/Joao-Paulo2007

## Licença

Este projeto está sob a licença [MIT](LICENSE).
