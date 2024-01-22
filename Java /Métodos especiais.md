# Métodos especiais
---
Para construir nossas classes precisamos de alguns Métodos especiais
___

#### Método Construtor

Para a instanciação de um novo Objeto de uma Classe, precisamos de um método que nos auxilia na construção. O responsável ? Método Construtor

**Um construtor é um Método especial que é definido para cada classe**

E já que ele é um método especial, ele possui algumas caracteristicas que o deferncia dos outros

- Um construtor é um método especial em uma classe que é chamado automaticamente quando um objeto é criado a partir dessa classe
- Usado para inicializar os atributos do objeto e realizar outras tarefas de inicialização.
- O construtor tem o mesmo nome da classe a que pertence.
- Um construtor não tem um tipo de retorno explícito. Ele cria e inicializa objetos, mas não retorna um valor.
- **O nome do construtor deve ser o próprio nome da classe.**
- O construtor pode receber argumentos, como qualquer Método. Geralmente ele recebe variáveis com o mesmo nome doa Atributos da Classe.
- **Toda Classe deve ter menos um Método construtor definido**, mesmo que de forma implícita.
- **Se nenhum construtor for explicitamente definido pelo programador da classe, um construtor default (0 para tipos numéricos primitivos, false para boolean e null para referências), que não recebe argumentos, é criado pelo compilador Java.**
- Se a pessoa desenvolvedora criar pelo menos um método construtor, o construtor default não será criado automaticamente - se ele o desejar, deverá criar um construtor sem argumentos explicitamente (Construtor de Objetos Nulos).
- Usando o mecanismo de Sobrecarga (veremos este assunto no próximo tópico), mais de um construtor pode ser definido para oferecer diversas maneiras de inicializar os objetos dessa classe. 

## Exemplo de um construtor da classe Bolo

```
public class Bolo {

    //Atributos da Classe Bolo
    private String sabor;
    private int tamanhoEmCentimetros;
    Private String cobertura;

    //Exemplo de construtor vazio
    public Bolo() {

    }

    //Exemplo de construtor com parâmetros
    public Bolo(String sabor, int tamanhoEmCentimetros, String cobertura) {
        this.sabor = sabor;
        this.tamanhoEmCentimetros = tamanhoEmCentimetros;
        this.cobertura = cobertura;
    }

}

```

O construtor está definido como **public** para que outras classes acessem e possam instanciar novos Objetos da classe Bolo

---

### Getters e Setters
São métodos GET e SET padronizados para o acesso dos atributos. A partir deles conseguimos acessar (getters) e alterar (setters) os Atributos privados.

##### SET
É um Método  utilizado para modificar os atributos. Eles são conhecidos como setters. **Abaixo temos um exemplo de declaração do método set do Atributo sabor**

```
    public void setSabor (String sabor) {
        this.sabor = sabor;
    }

```
Ele é um método **Público (public), sem tipo de retorno (void), seguido do identificador setNomeDoAtributo, seguido do parenteses (tipoDoAtributo identificadorDoAtributo)**. 
Dentro do seu corpo temos a palavra reservada **this**, pois o nome da váriavel do método set é o mesmo do Atributo da classe. 

>Você cria um set para cada Atributo que será modificado

##### GET
Os métodos GET servem para ler os dados dos atributos. Eles também são chamados de getters. 
**Abaixo temos um exemplo de declaração do método get do Atributo sabor**
```
    public String getSabor () {
        return sabor;
    }

```
Diferente do **SETTER** ele tem um tipo de retorno ja que ele deve retornar um valor do atributo;

>Se um objeto criado tem o valor do Atributo sabor como "Cenoura", ao chamar o getSabor() vai retornar o valor **Cenoura**.

>##### IMPORTANTE: assim como o setter, você cria o getter para retornar os valores desejados.

<br/>

##### Como devo usar ?
1. Caso não queira que um atributo seja modificado, remova o setter daquele atributo
2. Se não quiser que o atributo seja lido, remova os getters
3. Os setters permitem a validação dos dados antes de armazená-los, evitando que dados incorretos sejam armazenados
4. O getter permite esconder o tipo de dado do atributo


### Classe Bolo com Atributos, construtores, Getters e Setters

public class Bolo {

    //Atributos da Classe Bolo
    private String sabor;
    private int tamanhoEmCentimetros;
    Private String cobertura;

    //Exemplo de construtor vazio
    public Bolo() {

    }

    //Exemplo de construtor com parâmetros
    public Bolo(String sabor, int tamanhoEmCentimetros, String cobertura) {
        this.sabor = sabor;
        this.tamanhoEmCentimetros = tamanhoEmCentimetros;
        this.cobertura = cobertura;
    }

    public String getSabor(){
        return sabor;
    }

    public void setSabor(String sabor){
        this.sabor = sabor;
    }


    public String getTamanhoEmCentimetros(){
        return tamanhoEmcentimetros;
    }

    public void setTamanhoEmCentimetros(int tamanhoEmCentimetros){
        this.tamanhoEmCentimetros = tamanhoEmCentimetros;
    }


    public String getCobertura(){
        return cobertura;
    }

    public void setCobertura(String cobertura){
        this.cobertura = cobertura;
    }
}
