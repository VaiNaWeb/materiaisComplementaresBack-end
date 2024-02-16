# 📚 Lambda

Para falar de Expressões Lambda é preciso entender o conceito de **Programação Funcional**

##📖  Programação Funcional
Um paradigma de programação que se baseia na expressaão e na aplicação de funções matemáticas. Em vez de usar estados mutáveis e compartilhar dados, ela se baseia na ideia de que a computação é a avaliação de funções.

>Apesar de funções matemáticas serem associados com cálculos, no conceito aqui ela é muito mais ampla, trabalhando com dados que se possam produzir um valor

As caracteristicas desse paradigma são:
 - **Composição de função**: Criação de uma nova função combinando outras funções 
 - **Funções Puras**: São funções que produzem o mesmo resultado se receberem os mesmos argumentos. Não dependendo de valores mutáveis
 - **Imutabilidade**: Significa que uma vez que a variável recebe um valor ela o possui para sempre.
  
Inspirada nos conceitos de matemática, oferece soluções elegantes, concisas e poderosas para lidar com sistemas complexos.


## 🤯 Expresssões Lambda
É um pequeno bloco de código que recebe parâmetros e retorna um valor. Também pode ser vista como uma função anônima. Uma função que não tem nome e não pertence a nenhuma classe. Muito semellhante aos métodos, sua diferença é que não precisam de nome e podem ser implementadas diretamente em um método. Auxilia na construção de códigos mais limpors e enxutos

✒ **Sintaxe:**
``` 
parâmetros -> corpo da função
```
 Consiste em 3 componentes:
 - **Lista de parâmetros**: Pode receber ou não argumentos;
 - **Expressão Lambda**: A seta `->` é usada para separar o corpo da função
 - **Corpo**: Contém as instruções 

---

### 💫 Características 

  - **Declaração de tipo**: A declaração é opcional. Se não declarar o tipo do parâmetro, o compilador consegue descobrir (inferir)
  
  - **Exemplo com 2 parâmetros**:
  ``` 
  (10,2) -> corpo da função
  ``` 
  >*Detalhe: Os parentese são obrigatórios somente se tiverem mais de um parâmetro. Chaves também são obrigatórias quando se tem mais de uma linha de instrução*

  - **Exemplo com 1 parâmetro**:
  ```
  5 -> corpo da função
  ```
  - **Exemplo de Expressão Lambda com várias instruções**:
  ```
  numero -> {
        instrução 01
        instrução 02
        instrução 03
        };
  ```
- **Expressão Lambda com retorno**:

```java
numero -> {
    int retorno = numero * numero;
    return retorno;
}
```

## ❌ Exemplo de código sem Expressão Lambda:
```java
public class Lambda {
	public static void main(String[] args) {
        List<Integer> numeros = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);

		System.out.println("Exibindo itens: ");
		for (Integer numero : numeros) {
			System.out.println(numero);
		}
		System.out.println("----------------------------------");

		System.out.println("Somando os números com eles mesmos");
		for (Integer numero : numeros) {
			System.out.println(numero + numero);
		}

		System.out.println("----------------------------------");

		System.out.println("Exibindo os numeros impares:");
		for (Integer numero : numeros) {
			if (numero % 2 != 0) {
				System.out.println(numero);
			}
		}
    }
}
```
##  ✅ Exemplo de código com Expressão Lambda:

```java

public class Lambda {
	public static void main(String[] args) {
        List<Integer> numeros = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);

			List<Integer> numeros = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);

		System.out.println("Exibindo itens: ");
		numeros.forEach(numero -> System.out.println(numero));

		System.out.println("----------------------------------");

		System.out.println("Somando os números com eles mesmos");
		numeros.forEach(numero -> System.out.println(numero + numero));

		System.out.println("----------------------------------");

		System.out.println("Exibindo os numeros impares:");
		numeros.forEach(numero -> {
			if (numero % 2 != 0)
				System.out.println(numero);
		});
    }
}
```
##### ↘ Resultado no console de ambos exemplos:
 ```console
 Exibindo itens: 
1
2
3
4
5
6
7
8
9
10
----------------------------------
Somando os números com eles mesmos
2
4
6
8
10
12
14
16
18
20
----------------------------------
Exibindo os numeros impares:
1
3
5
7
9
 ```

 Comparando os dois códigos é notável que a segunda versão se tornou bem menos verboso e mais direto. As expressões foram inseridas no método `forEach()` da classe **Collections**, porque as Expressões Lambda dependem de uma interface funcional 

 O `forEach()` que é utilizada para iterar a coleção utiliza uma classe que implementa a **interface Consumer** que é passada como argumento. Já que a **interface Consumer** é uma interface funcional a ação será enviada na forma de expressão lambda


 ## 🔗 Links auxiliares
 - [Como usar Funções Lambda em Java](https://www.devmedia.com.br/como-usar-funcoes-lambda-em-java/32826)
 - [Como utilizar notações Lambda](https://www.dio.me/articles/java-como-funciona-a-notacao-lambda)
- [Interfaces Funcionais](https://www.sensedia.com.br/post/interfaces-funcionais-com-java-8#:~:text=Interfaces%20funcionais%20s%C3%A3o%20interfaces%20que,se%20automaticamente%20uma%20interface%20funcional)