#  📚 API STREAM 

A API Streams introduzida no Java 8 se tornou um recurso muito utilizado no processamento de Coleções de dados (Collections). Através dela conseguimos alcançar códigos limpos, de fácil manutenção e evitamos os efeitos indesejados em tempo de execução.

Elaa trabalha como uma sequência de instruções que suportam vários métodos encadeados que nos retornam um resultado.

Esse processo simplificado se tornou possível graças a inserção do *Paradigma Funcional* que foi introduzido. Para sua utilização combinamos esse paradigma com as *Expressões Lambda*.

Na prática, temos um pipeline de operações que formam um *fluxo*



Nas Streams temos dois tipos:

- **Operações intermediárias**: Se encontram no meio do aglomerado de funções e trazem um retorno para que as próximas funções consigam ser executadas.
- **Operações Terminais**: Retornam o resultado geral das operações. Depois de implementadas, não conseguimos mais utilizar nenhum método.

>**Importante:** É muito comum confundir Streams como uma estrutura de dados, mas isso não é verdade. **Collections** são estruturas de dados que armazenam os mesmos na memória. Já as **Streams** são estruturas de dados fixas que tem como finalidade realizar alguma ação.

Quando se trata de Streams, temos que ressaltar:

- Uma Stream **não é uma estrutura de dados**, em vez disso, recebe uma Collection
- **Os dados não são alterados**, elas apenas fornecem o resultado de acordo com a sequência de métodos que definirmos.

---

## Métodos intermediários.
Mencionamos esses queridos no começo desse arquivo, mas não explicamos o que são. **Métodos Intermediários ou Operações Intermediarias** são Métodos que *`retornam um novo Stream`*, para que novas operações intermediárias sejam executadas.

### Vamos conhecer alguns métodos ?

- ###  Map()
É o método usado pra executar uma operação das suas collections. Vamos criar uma nova lista que armazena alguns nomes com letras maiúsculas. 

```java 
import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class MapUpperCaseExample {
    public static void main(String[] args) {
        List<String> nomes = Arrays.asList("Samuel", "Joao", "Joy", "Dandara");

        // Usando map para transformar cada nome em letras maiúsculas
        List<String> nomesEmMaiusculo = names.stream()
                                           .map(String::toUpperCase)
                                           .collect(Collectors.toList());

        System.out.println("Lista original: " + nomes);
        System.out.println("Lista com nomes em letras maiúsculas: " + nomesEmMaiusculo);
    }
}
```
##### ↘ Resultado no console

```console
Lista original: [Samuel, Joao, Joy, Dandara]
Lista com nomes em letras maiúsculas: [SAMUEL, JOAO, JOY, DANDARA]
```

>Neste exemplo, a stream **nomes** é transformada utilizando o método `map()`, que aplica a função `String::toUpperCase` a cada elemento da stream. Esta função transforma cada string em letras maiúsculas. O resultado é então coletado em uma nova lista usando o método `collect(Collectors.toList()).`

--- 

- ###  filter()
O método filter é utilizado para filtrar os resultados de acordo com as condições pré definidas. Agora vamos considerar que queremos filtrar os números pares da lista de números de 1 a 10.

```java
import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class StreamFilterExample {
    public static void main(String[] args) {
        List<Integer> numeros = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);

        // Usando filter para filtrar apenas os números pares
        List<Integer> numerosPares = numeros.stream()
                                           .filter(n -> n % 2 == 0)
                                           .collect(Collectors.toList());

        System.out.println("Lista original: " + numeros);
        System.out.println("Números pares: " + numerosPares);
    }
}
```
##### ↘ Resultado no console

```console
Lista original: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
Números pares: [2, 4, 6, 8, 10]
```

- ### sorted()
  
O método **Sorted** é utilizado para classificar a Collection fornecida. Veja o exemplo abaixo da organização em código na ordenação de alguns números:

```java
import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class StreamSortExample {
    public static void main(String[] args) {
        List<Integer> numeros = Arrays.asList(3, 1, 4, 1, 5, 9, 2, 6, 5);

        // Usando sorted para ordenar os números em ordem crescente
        List<Integer> numerosOrdenados = numeros.stream()
                                             .sorted()
                                             .collect(Collectors.toList());

        System.out.println("Lista original: " + numeros);
        System.out.println("Lista ordenada: " + numerosOrdenados);
    }
}
```

##### ↘ Resultado no console

```console
Lista original: [3, 1, 4, 1, 5, 9, 2, 6, 5]
Lista ordenada: [1, 1, 2, 3, 4, 5, 5, 6, 9]
```
