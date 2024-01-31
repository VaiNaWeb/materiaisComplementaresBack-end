# Programação Orientada a Objetos - 01
---
## Classes, Objetos
___

Ao aprendermos uma nova linguagem, descobrimos o paradgima utilizado no seu desenvolvimento. 

Um paradigma é nada mais nada menos do que uma maneira de programarmos, um modo de fazer aquele programa.

Ao escolhermos a linguagem, nos deparamos com esse paradigma (Orientação a objetos, estruturado, imperativo e outros mais).

Com o Java, utilizamos o paradigma Orientado a Objetos.

Há anos atrás, desenvolvedores passavam por certas dificuldades em grandes projetos de software, tornando também mais complexo o processo de desenvolvimento. 
O problema dessa abordagem é que, de tempos em tempos, as empresas desejam mudar alguns processos e procedimentos. Logicamente, o software também passaria por mudanças. ( Ao menos que utilizassem recurso alternativos, vulgo gambiarras para que tudo se mantenha funcional).

Então, com esse problema em mente, belas cabecinhas pensaram: "Se os processos de uma empresa mudam constantemente, não devemos usá-las como base para a organização da minha aplicação". Com isso, veio a grande tacada "Vamos basear tudo nos objetos envolvidos no processo e não nos processos em si"..

**POO (Programação Orientada a Objetos)** é um paradigma de Programação que se baseia em objetos reais, podendo ser abastratos ou não. **O intuito é simular o que acontece e o que existe no mundo real, dentro do mundo virtual.**

>**Abstrato:** algo que não é concreto; opera com ideias ou algo associado a esses ideis, não com a realidade em si. Algo totalmente generalizado.

<br />

## Objetos
No nosso mundo, os objetos podem ser animados ou inanimados e  **todos eles possuem caracteristicas(atributos) e comportamentos**

<a href="https://imgur.com/ZxqXvYN"><img src="https://i.imgur.com/ZxqXvYN.png" title="Objetos com certo nível de abstração" /></a>

>Percebam que na imagem acima, os objetos tem um nível de abstração, ou seja, todos tem uma forma genérica.

## E o que são Objetos em programação ? 

São instâncias de classes que possuem dados(Atributos) e comportamentos (Métodos). São usados para organizar as informação de uma maneira mais organizada e modular.

É similar a uma estrutura de dados, porém, além de dados, um objeto tambem armazena os métodos.

>Em um objeto, seus dados se chamam atributos e as funções são chamadas de métodos

## Classes
Uma classe pode ser vista como molde de um objeto. Nela estão presentes todos os atributos e métodos essenciais. 

<a href="https://imgur.com/dOr0BB3"><img src="https://imgur.com/dOr0BB3.png" title="Objetos com certo nível de abstração" /></a>

Repare que a classe **(Forma redonda)** é algo mais abstrato, é um molde e a partir disso temos a criação de objetos **(BoloLimaoRedondo)** e **(BoloChocolateRedondo)**. Cada um com seus devidos atributos

>Essa criação também é chamada de **instanciação da classe**

Como todo programa, uma classe é composta por algumas variáveis que chamamos de atributos e funçãos que são métodos.

>Atributos são responsáveis pela caracteristica do objeto. no exemplo dos bolos, podemos criar um atributo cobertura. **BoloLimaRedondo com chantily rodelas de limão** e **BoloChocolateRedondo com cobertura de chocolate com morango**

Nesse ponto, ja entendemos que temos um molde(classe) que possui algumas caracteristicas (atributos). Com isso passamos para os **Métodos**. 

**Métodos são as ações que irão modificar e/ou interagir com os Atributos.**

Vou utilizar como exemplo, a classe Pessoa 

<a href="https://imgur.com/a/MVDUv3j"><img src="https://i.imgur.com/io8E1h3.png" title="Objetos com certo nível de abstração" /></a>

Observe na imagem acima que Pessoa tem ações(Métodos) como **andar(), falar() e trabalhar()**.
<br />
#### IMPORTANTE

| Elemento         | Padrão de Identificação | Exemplo        | Como declarar
|------------------|-------------------------|----------------|-------------------|
| Classe           | PascalCase              | `MinhaClasse`  | por substativos
| Atributo         | camelCase               | `meuAtributo`  | por substativos |
| Método           | camelCase               | `meuMetodo()`  | por verbos |

> Ao criar Classes, atributos e métodos, prefira usar esses padrões para nomenclaturas

<br />

---

### Modificadores
---
 Os modificadores são palavras-chave da Linguagem Java, que servem para definir a visibilidade e algumas propriedades de uma Classe, Método ou Atributo.

<br />

 ---

### Modificadores de Visibilidade
---
Modificadores de Visibilidade ou Modificadores de acesso determinam como o Método, Atributo e a própria Classe serão manipulados no decorrer do desenvolvimento do programa, ou seja, qual (is) Classes podem chamar uma determinada Classe, chamar um determinado Método e acessar os Atributos.

Um conceito importante, que interfere diretamente no conceito de visibilidade, é o conceito de Pacotes. 


####  Modificadores de Acesso - Classes
As classes possuem apenas 2 modificadores de acesso: 

| **Modificador** | **Descrição**                                                |
| --------------- | ------------------------------------------------------------ |
| **padrão**      | Uma Classe padrão ou friendly (identificado pela ausência de modificadores), poderá ser acessada por todas as Classes que estiverem **no mesmo pacote**. |
| **public**      | Uma Classe public poderá ser acessado por qualquer classe em qualquer pacote. |

<br />

#### Modificadores de acesso - Métodos e Atributos


 Os métodos e os Atributos possuem 4 modificadores de acesso: 
 <br/>

 | **Modificador** | **Descrição**                                                | UML  |
| --------------- | ------------------------------------------------------------ | :--: |
| **padrão**      | Um Método ou Atributo padrão (identificado pela ausência de modificadores) poderá ser acessado por todas as classes que estiverem **no mesmo pacote**, que a classe que possui o Atributo. |      |
| **public**      | Um Método ou Atributo são acessíveis de qualquer lugar, dentro ou fora da classe. |  +   |
| **protected**   | Um Método ou Atributo protected é protegido e pode ser chamado por todas as classes do mesmo pacote **package** e subclasses (Herança). |  #   |
| **private**     | Um Método ou Atributo private só são acessíveis dentro da prórpia classe |  -   |

Nível de visibilidade dos Atributos e Métodos, do nível de acesso mais restrito (Private) ao nível de acesso total e irrestrito (Public). Na tabela abaixo temos um resumo:
| Modificador   | Classe | Pacote | Sub Classe | Mundo |
| ------------- | :----: | :----: | :--------: | :---: |
| **public**    |   ✔    |   ✔    |     ✔      |   ✔   |
| **protected** |   ✔    |   ✔    |     ✔      |   ❌   |
| **padrão**    |   ✔    |   ✔    |     ❌      |   ❌   |
| **private**   |   ✔    |   ❌    |     ❌      |   ❌   |


> Os Modificadores de Acesso de um Atributo definem quais Classes poderão acessar o atributo, dessa mesma forma os Modificadores de um Método definem quais Classes terão acesso a esse mesmo Método.

<br/>

####Modificadores Non-Access
O modificador Non-Access permite especificar algumas propriedades específicas de uma Classe, Método ou Atributo, determinando como as Classes que herdarão uma Classe, Método ou Atributo, podem ou não instanciar uma Classe, redefinir e/ou alterar um Método ou Atributo.

<br/>

#### Modificadores Non-Access - Classes

As classes possuem apenas 2 modificadores Non-Access: 

| Modificador  | Descrição                                                    |
| ------------ | ------------------------------------------------------------ |
| **abstract** | Uma classe abstrata não pode ser usada para criar objetos, ou seja, instanciar objetos de forma direta. Para acessar uma classe abstrata, ela deve ser herdada por outra classe e instanciada por meio desta herança. |
| **final**    | Uma Classe final não pode ser Herdada (estendida) por outra Classe. |

<br />

#### Modificadores Non-Access - Métodos
Os Métodos possuem 3 modificadores Non-Access principais:

| Modificador  | Descrição                                                    |
| ------------ | ------------------------------------------------------------ |
| **abstract** | Um  método abstrato não implementa nenhuma funcionalidade, somente  assina o  método e faz com que a primeira subclasse concreta seja  obrigada a  implementar o método. Uma classe que possua um método  abstrato deve  obrigatoriamente ser abstrata. |
| **final**    | Um  método final define que ele não pode ser sobrescrito e/ou modificado. |
| **static**   | Um método **static** é um método da Classe, ou seja, são métodos que não dependem de um Objeto, quando eles são invocados, executam uma função sem a dependência de um objeto ou instância de uma classe,  conseguindo chamar direto qualquer Método da classe. |

Na tabela acima, destacamos os principais modificadores Non-Access da Linguagem Java. 

**Observações importantes:**

- Um método nunca poderá ser abstract e final
- Um método nunca poderá ser abstract e private
- Um método final nunca poderá ser sobrescrito ou sobrecarregado
- Um método abstrato nunca poderá ser implementado
- Se um método for abstrato a classe também será abstrata

<br />

Os Atributos possuem 2 modificadores Non-Access principais:

| Modificador | Descrição                                                    |
| ----------- | ------------------------------------------------------------ |
| **final**   | Um atributo final é uma constante, ou seja, não pode ser modificado. |
| **static**  | Um atributo **static** é um atributo da Classe, ou seja, não dependem de um Objeto ou instância de uma classe. |

Na tabela acima, destacamos os principais modificadores Non-Access da Linguagem Java.

Para se aprofundar mais no conteúdo, sugerimos a leitura da <a href="https://www.w3schools.com/java/java_modifiers.asp" target="_blank"><b>Documentação: Modificadores Non-Access</b></a>

<br />

# Exemplo de uma classe Bolo com seus Atributos e Modificadores de acesso


```
public class Conta {

    //Atributos da Classe Conta
    private String sabor;
    private int tamanhoEmCentimetros = 25;
    Private String cobertura;
}
```

