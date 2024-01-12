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
