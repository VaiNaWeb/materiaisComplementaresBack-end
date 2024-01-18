# Interface

Em Java, uma interface é uma **coleção de métodos abstratos** (sem implementação) e **constantes** (variáveis finais), que **define um contrato que as classes que a implementam devem seguir**. Uma interface permite que você defina um conjunto de métodos que qualquer classe pode implementar, independentemente de sua hierarquia de herança. Ela fornece um mecanismo para alcançar a abstração e o polimorfismo.

Detalhando mais a interface: 

- **Métodos abstratos:** Interfaces em Java consistem principalmente em métodos abstratos, que são declarados sem uma implementação. Cada classe que implementa a interface deve fornecer uma implementação concreta para todos os métodos definidos na interface.
- **Constantes:** Além de métodos, interfaces podem conter constantes (variáveis finais). Essas variáveis são implicitamente públicas, estáticas e finais, o que significa que são constantes que podem ser acessadas através do nome da interface.
- **Sem métodos concretos:** Ao contrário das classes abstratas, as interfaces não podem ter implementações de métodos. Cada método declarado em uma interface é implicitamente abstrato e público, mesmo que você não use as palavras-chave abstract ou public.
- **Implementação multipla:** Uma classe em Java pode implementar múltiplas interfaces. Isso permite que a classe adote comportamentos de várias fontes sem a necessidade de herança múltipla, o que não é suportado diretamente em Java.

Exemplo do código em Java:

```
// Definindo a interface Pessoa
interface Pessoa {
    void apresentar();
}

// Implementando a classe Professor que implementa a interface Pessoa
class Professor implements Pessoa {
    private String nome;
    private String disciplina;

    // Construtor
    public Professor(String nome, String disciplina) {
        this.nome = nome;
        this.disciplina = disciplina;
    }

    // Implementação do método da interface Pessoa
    @Override
    public void apresentar() {
        System.out.println("Olá, eu sou o Professor " + nome + " e leciono " + disciplina + ".");
    }
}

// Implementando a classe Estudante que implementa a interface Pessoa
class Estudante implements Pessoa {
    private String nome;
    private int matricula;

    // Construtor
    public Estudante(String nome, int matricula) {
        this.nome = nome;
        this.matricula = matricula;
    }

    // Implementação do método da interface Pessoa
    @Override
    public void apresentar() {
        System.out.println("Oi, eu sou o Estudante " + nome + " e minha matrícula é " + matricula + ".");
    }
}

// Exemplo de uso das classes
public class ExemploInterface {
    public static void main(String[] args) {
        // Criando uma instância de Professor
        Professor professor = new Professor("Samuel", "Back-end");
        professor.apresentar();

        // Criando uma instância de Estudante
        Estudante studante = new Estudante("Fulanis", 1234);
        estudante.apresentar();
    }
}

```

>Quando temos interfaces, utilizamos a palavra **implements** para "firmar" os contratos

No exemplo acima temos a interface  Pessoa que define o método apresentar(). As subclasses usam esse método e os especializam (Adicionam as próprias caracteristicas)

## Mais caracteristicas: 

- **Métodos em Interfaces:** Consistem principalmente em métodos abstratos. **Todos** os métodos de uma interface são implicitamente ***public*** e ***abstract***
```
// Definindo uma interface com métodos abstratos
interface Exemplo {
    void metodoAbstrato();
    int calcularAlgo();
}

```
- Constantes em Interfaces: Interfaces também podem conter constantes, que são implicitamente public, static, e final. Essas constantes são geralmente usadas para definir valores que são compartilhados por todas as implementações da interface.

```
// Definindo uma interface com uma constante
interface Exemplo {
    String MENSAGEM = "Olá, mundo!";
}

```

- **Implementação multipla:** Uma classe em Java pode implementar Várias interfaces 

```
// Definindo duas interfaces
interface InterfaceA {
    void metodoA();
}

interface InterfaceB {
    void metodoB();
}

// Implementando ambas as interfaces em uma classe
class MinhaClasse implements InterfaceA, InterfaceB {
    @Override
    public void metodoA() {
        System.out.println("Implementação de InterfaceA");
    }

    @Override
    public void metodoB() {
        System.out.println("Implementação de InterfaceB");
    }
}
```
## Beneficios

Proprocionam um alto nível de abstração, permitindo a criação de contratos claros entre classe e promovendo a flexibilidade e o polimorfismo em Java


## Links Auxiliares

- [Entendendo interfaces em Java](https://www.devmedia.com.br/entendendo-interfaces-em-java/25502)

- [Interfaces x Classes Abstratas](https://www.dio.me/articles/interfaces-x-classes-abstratas)
