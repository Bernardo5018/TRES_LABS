# Computação Móvel – Projetos em Kotlin

Este ficheiro reúne, de forma organizada, os conteúdos de três projetos desenvolvidos no contexto da unidade curricular de **Computação Móvel**: a aplicação **Hello World**, a aplicação **HelloWorld Optional** e o projeto **TP1 – Kotlin Programming Exercises**. A descrição, objetivos, estrutura e funcionalidades abaixo resultam da consolidação dos três ficheiros fornecidos pelo utilizador. fileciteturn0file0 fileciteturn0file1 fileciteturn0file2

---

## Índice

1. [Enquadramento Geral](#enquadramento-geral)
2. [Tecnologias Utilizadas](#tecnologias-utilizadas)
3. [Projeto 1 – Hello World](#projeto-1--hello-world)
4. [Projeto 2 – HelloWorld Optional](#projeto-2--helloworld-optional)
5. [Projeto 3 – TP1 Kotlin Programming Exercises](#projeto-3--tp1-kotlin-programming-exercises)
6. [Competências Trabalhadas](#competências-trabalhadas)
7. [Possíveis Melhorias Futuras](#possíveis-melhorias-futuras)
8. [Autor](#autor)
9. [Licença](#licença)

---

## Enquadramento Geral

Este conjunto de projetos foi desenvolvido como base de aprendizagem prática em **Kotlin** e no ecossistema **Android**, permitindo consolidar conceitos fundamentais de desenvolvimento móvel e programação orientada a objetos. No total, os trabalhos cobrem desde a criação de uma primeira aplicação Android até à implementação de exercícios de consola e de um pequeno sistema de gestão de biblioteca virtual. fileciteturn0file0 fileciteturn0file1 fileciteturn0file2

Os projetos foram pensados para:

- compreender a estrutura de projetos Android e Kotlin;
- explorar a criação de interfaces simples;
- trabalhar com **Activities**;
- obter informação do sistema Android;
- praticar sintaxe, funções, arrays, classes, herança e organização de código em Kotlin. fileciteturn0file0 fileciteturn0file1 fileciteturn0file2

---

## Tecnologias Utilizadas

Ao longo dos três projetos foram utilizadas as seguintes tecnologias e ferramentas:

- **Kotlin**
- **Android Studio**
- **Android SDK**
- **Gradle**
- **IntelliJ IDEA**
- **Maven**
- **JVM**
- **ConstraintLayout** fileciteturn0file0 fileciteturn0file1 fileciteturn0file2

---

## Projeto 1 – Hello World

### Descrição

O projeto **Hello World** consiste numa aplicação Android introdutória desenvolvida em **Kotlin** no **Android Studio**. O objetivo principal é demonstrar a criação de uma primeira aplicação Android e perceber o funcionamento base de uma **Activity**, da interface e da estrutura do projeto. fileciteturn0file0

### Objetivos

Neste projeto foram trabalhados os seguintes pontos:

- compreender a estrutura de um projeto Android;
- criar uma aplicação simples em Kotlin;
- explorar o funcionamento de uma **Activity**;
- executar a aplicação num emulador ou dispositivo físico;
- utilizar recursos Android, como **layouts** e **strings**. fileciteturn0file0

### Estrutura Principal

```text
HelloWorld
│
├── app
│   ├── src
│   │   ├── androidTest
│   │   ├── main
│   │   │   ├── java
│   │   │   │   └── cm_a15033
│   │   │   │        └── helloworld
│   │   │   │             └── MainActivity.kt
│   │   │   ├── res
│   │   │   │   ├── layout
│   │   │   │   │     activity_main.xml
│   │   │   │   ├── values
│   │   │   │   │     strings.xml
│   │   │   │   └── mipmap
│   │   │   │         ic_launcher
│   │   │   └── AndroidManifest.xml
│   │   └── test
│   └── build.gradle.kts
└── build.gradle
```

Estrutura consolidada a partir do ficheiro do projeto. fileciteturn0file0

### Funcionamento da Aplicação

A aplicação possui uma **Activity principal**, chamada `MainActivity`, responsável por:

- iniciar a aplicação;
- carregar o layout da interface;
- executar o código quando a aplicação é aberta. fileciteturn0file0

A classe herda de `AppCompatActivity` e utiliza o método `onCreate()` para inicialização. O ficheiro original apresenta um exemplo simplificado semelhante ao seguinte: fileciteturn0file0

```kotlin
class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)

        setContentView(R.layout.activity_main)

        println("MainActivity iniciada")
    }
}
```

### Interface Gráfica

A interface é definida no ficheiro `activity_main.xml`, onde se encontra a estrutura visual da aplicação. Este ficheiro organiza os elementos apresentados ao utilizador e define o layout principal da app. fileciteturn0file0

### Execução

Para executar o projeto:

1. abrir o projeto no **Android Studio**;
2. sincronizar o **Gradle**;
3. clicar em **Run**;
4. escolher um emulador Android ou dispositivo físico. fileciteturn0file0

### Resultado

Este projeto demonstra corretamente a base do desenvolvimento Android com Kotlin, funcionando como ponto de partida para aplicações mais completas. fileciteturn0file0

---

## Projeto 2 – HelloWorld Optional

### Descrição

O projeto **HelloWorld Optional** é uma aplicação Android desenvolvida em **Kotlin** cujo objetivo é apresentar, no ecrã, várias informações sobre o dispositivo Android onde está a correr. Entre essas informações encontram-se o fabricante, modelo, marca, tipo de build, utilizador, versão do sistema e versão SDK. Estes dados são obtidos através da classe `Build` do Android. fileciteturn0file1

### Objetivos

Os principais objetivos deste projeto foram:

- criar uma aplicação Android funcional em Kotlin;
- explorar a estrutura base de um projeto Android;
- trabalhar com **Activities**;
- utilizar componentes de interface gráfica;
- obter informação do sistema Android através da classe `Build`;
- apresentar dados dinamicamente na interface. fileciteturn0file1

### Estrutura Principal

```text
helloworldOptional
│
├── app
│   ├── src
│   │   ├── main
│   │   │   ├── java/cm_a15033/helloworldoptional
│   │   │   │   └── MainActivity.kt
│   │   │   ├── res
│   │   │   │   ├── layout
│   │   │   │   │   └── activity_main.xml
│   │   │   │   ├── values
│   │   │   │   │   ├── colors.xml
│   │   │   │   │   ├── strings.xml
│   │   │   │   │   └── themes.xml
│   │   │   └── AndroidManifest.xml
│   └── build.gradle.kts
├── gradle
├── gradlew
└── settings.gradle.kts
```

Estrutura consolidada a partir do ficheiro do projeto. fileciteturn0file1

### Interface da Aplicação

A interface foi criada no ficheiro `activity_main.xml` e inclui dois elementos principais:

- um **TextView** para o título;
- um **EditText multiline** para mostrar as informações recolhidas do dispositivo. fileciteturn0file1

O ficheiro original apresenta exemplos de ambos os componentes, incluindo a definição de texto, cor e tipo de input. fileciteturn0file1

### Funcionamento da Aplicação

A lógica principal encontra-se em `MainActivity.kt`. A aplicação:

1. inicia a Activity;
2. carrega o layout;
3. obtém dados do dispositivo através da classe `Build`;
4. mostra esses dados no campo de texto. fileciteturn0file1

Exemplo consolidado a partir do código apresentado no ficheiro original: fileciteturn0file1

```kotlin
class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)

        setContentView(R.layout.activity_main)

        val editText = findViewById<EditText>(R.id.editTextTextMultiLine)

        val informações =
            "Manufacturer: " + Build.MANUFACTURER + "\n" +
            "Model: " + Build.MODEL + "\n" +
            "Brand: " + Build.BRAND + "\n" +
            "Type: " + Build.TYPE + "\n" +
            "User: " + Build.USER + "\n" +
            "SDK: " + Build.VERSION.SDK_INT + "\n" +
            "Version: " + Build.VERSION.RELEASE + "\n"

        editText.setText(informações)
    }
}
```

### Informações Obtidas

Segundo o ficheiro fornecido, alguns dos dados apresentados incluem:

- `Manufacturer`
- `Model`
- `Brand`
- `Type`
- `SDK`
- `Version` fileciteturn0file1

### Execução

A execução segue os passos normais de um projeto Android:

1. abrir o projeto no **Android Studio**;
2. escolher **File → Open**;
3. abrir a pasta do projeto;
4. executar com o botão **Run**;
5. selecionar um emulador ou dispositivo físico. fileciteturn0file1

### Resultado

Este projeto permite explorar a API Android de forma simples, apresentando dinamicamente no ecrã dados reais do dispositivo onde a app é executada. fileciteturn0file1

---

## Projeto 3 – TP1 Kotlin Programming Exercises

### Descrição

O projeto **TP1 – Kotlin Programming Exercises** reúne a resolução do Trabalho Prático 1 da unidade curricular de **Computação Móvel**. O seu objetivo é explorar conceitos fundamentais de **Kotlin**, incluindo estruturas básicas da linguagem, arrays, funções, controlo de fluxo, programação orientada a objetos, herança e organização de código em packages. O projeto foi desenvolvido em **IntelliJ IDEA** com estrutura baseada em **Maven**. fileciteturn0file2

### Objetivos

Os principais objetivos deste trabalho foram:

- compreender a sintaxe base de Kotlin;
- aplicar estruturas de controlo e coleções;
- desenvolver pequenos programas de consola;
- implementar conceitos de **Programação Orientada a Objetos**;
- criar um pequeno sistema de gestão de biblioteca virtual. fileciteturn0file2

### Estrutura Principal

```text
TP1
│
├── src
│   ├── main
│   │   └── kotlin
│   │        └── cm
│   │             ├── exer_1
│   │             │      exer_1.kt
│   │             ├── exer_2
│   │             │      exer_2.kt
│   │             ├── exer_3
│   │             │      exer_3.kt
│   │             └── virtual_library
│   │                    Book.kt
│   │                    DigitalBook.kt
│   │                    PhysicalBook.kt
│   │                    Library.kt
│   │                    LibraryManager.kt
│   │                    Main.kt
└── pom.xml
```

Estrutura consolidada a partir do ficheiro do projeto. fileciteturn0file2

### Exercícios Implementados

#### Exercise 1

Este exercício explora:

- declaração de variáveis;
- utilização de arrays;
- manipulação de valores numéricos;
- impressão de resultados no terminal. fileciteturn0file2

#### Exercise 2

Este exercício trabalha:

- manipulação de listas;
- ciclos e iterações;
- funções;
- processamento de dados. fileciteturn0file2

#### Exercise 3

Este exercício aprofunda:

- estruturas de controlo;
- manipulação de dados;
- organização de código. fileciteturn0file2

### Virtual Library

A componente principal do projeto é o sistema **Virtual Library**, que simula a gestão de livros numa biblioteca e foi desenvolvido com base em conceitos de **Programação Orientada a Objetos**. Este sistema inclui classes, herança, polimorfismo e encapsulamento. fileciteturn0file2

#### Classes Implementadas

**Book**  
Classe base que representa um livro, contendo atributos como título, autor e ano de publicação. Serve de superclasse para outros tipos de livros. fileciteturn0file2

**DigitalBook**  
Subclasse de `Book` que representa um livro digital, podendo incluir propriedades adicionais como formato e tamanho do ficheiro. fileciteturn0file2

**PhysicalBook**  
Subclasse de `Book` que representa um livro físico, podendo incluir atributos como número de páginas e localização. fileciteturn0file2

**Library**  
Classe responsável pela gestão da biblioteca, com operações como adicionar, remover e listar livros. fileciteturn0file2

**LibraryManager**  
Classe responsável pela organização da lógica e interação com a biblioteca. fileciteturn0file2

**Main**  
Classe principal do programa, contendo `fun main()` para iniciar a aplicação e testar o sistema. fileciteturn0file2

### Execução

Para executar o projeto:

1. abrir o projeto no **IntelliJ IDEA**;
2. compilar o projeto;
3. executar o ficheiro `Main.kt`. fileciteturn0file2

### Resultado

Este trabalho demonstra com sucesso a utilização da linguagem Kotlin, a organização de código em packages e a implementação de conceitos de POO num sistema funcional de consola. fileciteturn0file2

---

## Competências Trabalhadas

Ao juntar os três projetos, é possível identificar um conjunto de competências desenvolvidas ao longo do trabalho:

- introdução ao desenvolvimento Android;
- criação e gestão de **Activities**;
- construção de interfaces com layouts XML;
- utilização de recursos Android;
- interação com classes do sistema, como `Build`;
- prática de sintaxe Kotlin;
- utilização de arrays, listas, ciclos e funções;
- aplicação de herança, polimorfismo e encapsulamento. fileciteturn0file0 fileciteturn0file1 fileciteturn0file2

---

## Possíveis Melhorias Futuras

Com base nas melhorias sugeridas nos ficheiros originais, podem ser consideradas as seguintes evoluções:

- adicionar novos ecrãs e mais **Activities**;
- melhorar a interface gráfica das aplicações Android;
- criar navegação entre páginas;
- integrar persistência de dados;
- guardar informação em ficheiros ou bases de dados;
- expandir o sistema da biblioteca com utilizadores e empréstimos;
- adicionar funcionalidades mais interativas. fileciteturn0file0 fileciteturn0file1 fileciteturn0file2

---

## Autor

Projeto desenvolvido por:

**Bernardo Rocha – 15033**  
Estudante de Engenharia Informática  
Unidade Curricular: **Computação Móvel** fileciteturn0file0 fileciteturn0file1 fileciteturn0file2

---

## Licença

Todos os ficheiros indicam que os projetos foram desenvolvidos para fins académicos ou educacionais. fileciteturn0file0 fileciteturn0file1 fileciteturn0file2
