# Encapsulamento
---

**Encapsular** é nada mais nada menos que esconder detalhes internos de uma classe e permitir o acesso controlado aos seus membros. 

### Vantagens
- "Escondendo" vocẽ protege a integridade dos dados evitando alterações diretas
- Permite a implementação de lógica de validação e controlar o acesso e a modificação
- Facilita manutenção do código, já que os detalhes podem ser alterados sem impactar o código.

Ao utilizarmos do encapsulamento evitamos qualquer acesso indevido. Para isso, precisamos de uma pequena estrutura contendo métodos publicos que nos permitem ter o controle no desenvolvimento

Na prática, utilzamos de Getters e Setter + modificadores de acesso.

### Exemplo de encpasulamento na classe Pessoa.

```
public class Pessoa {
    private String nome;
    private int idade;
    private String email;

    // Construtor
    public Pessoa(String nome, int idade, String email) {
        this.nome = nome;
        this.idade = idade;
        this.email = email;
    }

  
    public String getNome() {
        return nome;
    }

    public void setNome(String novoNome) {
        this.nome = novoNome;
    }

    public int getIdade() {
        return idade;
    }

    public void setIdade(int novaIdade) {
        if (novaIdade > 0) {
            this.idade = novaIdade;
        }
    }

    public String getEmail() {
        return email;
    }

    public void setEmail(String novoEmail) {
        // Poderia ser adicionada validação de e-mail aqui
        this.email = novoEmail;
    }

}

```
Repare que no **Setter** do Atributo **idade** tem uma validação. Claro, não tem como você ter menos de 0 anos.


<div align = "center">

# Imutabilidade 

</div>

O conceito de imutabilidade é a propriedade de objetos cujo não permitem alteração depois de criados.

Então, uma vez criado, nunca mais modificado, tornando-o contante e previsivel durante toda a sua existência.

## Por que a imutabilidade é importante ? 

- Segurança: Como não podem ter alteração, os objetos se tornam mais seguros evitando os mesmos a serem corrompidos ou inconsistentes, algo que ocorrem quando muitas partes alteram o mesmo objeto simultaneamente

- Facilidade no raciocinio: Com objetos imutaveis você confia que o estado não será mudado em qualquer lugar do projeto

- Concorrência: Em ambientes concorrentes ela é valiosa. Se os objetos estão imutáveis, não há necessidade de sincronização ou locks para protegê-lo, tornando o código mais seguro e eficiente em termos de concorrência.

- Cache e performace: Se são imutaveis, são facilmente armazenados em cache, pois seu estado nunca muda. Isso leva melhorias no desempenho, especialmente em objetos que são acessados repetidas vezes

- Passagem de argumentos: Em Java, os parametros são passados por valor. Quando algo mutável é passado corre o risco de ser alterado dentro do método, levando a comportamentos inesperados. Utilizando a imutabilidade, vocẽ garante que ele está preservado

### Como criar objetos imutaveis ?
De acord com Joshua Bloch no livro Effective Java (Bloch,2001) temos 5 regrinhas para tornar a classe imutável: 

- Não forneça nenhum método que modifique o estado do objeto
- Assegure que a classe não possa ser estendida
- Defina todos os atributos como **final**
- Faça com que todos os atributos sejam privados
- Assegure acesso exclusivo a quaisquer composição com objetos mutáveis


## Desvantagens
Claro que assim como vantagens, algo também possui suas desvantagens. Embora valiosa, ela traz esses problemas dependendo do contexto em que ela esta inserida. Como: 

- **Overhead de memória**: Como temos as cópias de objetos para realizar alterações, isso leva ao consumo alto da memória, especialmente nos cenários de muitas operações de cópia.

- **Custo de criação**: Quando usados extensivamente o custo será o desempenho, principalmente em dispositivos com recurso limitados.

## Links auxiliares
- [Encapsulamento](https://www.alura.com.br/artigos/o-que-e-encapsulamento#:~:text=Encapsulamento%20%C3%A9%20um%20princ%C3%ADpo%20de,(normalmente%20m%C3%A9todos%20e%20fun%C3%A7%C3%B5es).)

- [Imutabilidade](https://diogomoreira.gitbook.io/padroes-de-projeto/orientacao-a-objetos/conceitos-basicos-de-orientacao-a-objetos/imutabilidade)
## The END

