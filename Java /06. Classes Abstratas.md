# Classes Abstratas

Uma classe abstrata é uma **classe que não pode ser instanciada diretamente,** mas que serve como um **modelo** para outras classes derivadas. Ela geralmente contém métodos abstratos, ou seja, métodos sem implementação, que devem ser implementados pelas subclasses. O principal propósito de uma classe abstrata é **fornecer uma estrutura comum para suas subclasses**, garantindo que certos métodos estejam presentes e incentivando a consistência entre as classes derivadas.

Temos abaixo alguns conceitos importantes relacionados a classes abstratas: 

- **Métodos Abstratos:** Uma classe abstrata frequentemente contém métodos abstratos, que são declarados na classe base, mas não têm uma implementação concreta **(Não tem um corpo)**. Esses métodos devem ser implementados nas classes derivadas.

Exemplo:
```
public abstract void calcular();

```
>Através da palavrinha abstract definimos um método e/ou classe como abstrato

- **Não pode ser instanciada diretamente:** Você precisa criar uma subclasse que herda da classe abstrata e fornecer suas implementações especializadas para os métodos abstratos

-**Padronização:** Uma classe abstrata define uma interfacec ou conjunto de métodos que suas subclasses devem implementar

- **Pode ter métodos concretos:** Além dos nossos métodos abstratos, existe a possibilidade de métodos concretos (Com corpo e linhas de código) que podem ser herdados pelas subclasses, mas também podem ser sobrescritos, se necessário.

Exemplo de classe abstrata com métodos abstratos:

```
// Definindo a classe abstrata Forma
abstract class Forma {
    // Método abstrato para calcular a área
    public abstract double calcularArea();

    // Método abstrato para calcular o perímetro
    public abstract double calcularPerimetro();
}

// Subclasse Círculo que estende a classe abstrata Forma
class Circulo extends Forma {
    // Raio do círculo
    private double raio;

    // Construtor
    public Circulo(double raio) {
        this.raio = raio;
    }

    // Implementação do método para calcular a área de um círculo
    @Override
    public double calcularArea() {
        return Math.PI * Math.pow(raio, 2);
    }

    // Implementação do método para calcular o perímetro de um círculo
    @Override
    public double calcularPerimetro() {
        return 2 * Math.PI * raio;
    }
}

// Subclasse Quadrado que estende a classe abstrata Forma
class Quadrado extends Forma {
    // Lado do quadrado
    private double lado;

    // Construtor
    public Quadrado(double lado) {
        this.lado = lado;
    }

    // Implementação do método para calcular a área de um quadrado
    @Override
    public double calcularArea() {
        return Math.pow(lado, 2);
    }

    // Implementação do método para calcular o perímetro de um quadrado
    @Override
    public double calcularPerimetro() {
        return 4 * lado;
    }
}

// Exemplo de uso das classes
public class Main {
    public static void main(String[] args) {
        // Criando uma instância de Circulo
        Circulo circulo = new Circulo(5.0);
        System.out.println("Área do círculo: " + circulo.calcularArea());
        System.out.println("Perímetro do círculo: " + circulo.calcularPerimetro());

        // Criando uma instância de Quadrado
        Quadrado quadrado = new Quadrado(4.0);
        System.out.println("Área do quadrado: " + quadrado.calcularArea());
        System.out.println("Perímetro do quadrado: " + quadrado.calcularPerimetro());
    }
}

```

>Frequentemente verão uma **superclasse (Classe Pai)** sendo uma classe **abstract**, já que elas encapsulam conceitos gerais ou comportamentos que devem ser especializados pelas **subclasses (Classes filhas)**

## Link Auxiliar
- [Classe Abstrata](https://www.alura.com.brapostila-java-orientacao-objetos/classes-abstratas)
- [Métodos abstratos e mais sobre classes abstratas](https://codegym.cc/pt/groups/posts/pt.192.metodo-abstrato-java-e-classes)