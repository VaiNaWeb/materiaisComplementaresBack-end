# Polimorfismo

Polimorfismo, no sentido da palavra, é "qualidade ou estado de ser capaz de assumir diferentes formas". Na orientação a objetos, o polimorfismo denota uma situação na qual um objeto pode se comportar de maneiras diferentes ao receber uma mensagem (chamada de método). Podem ser de dois tipos: estático ou dinâmico.

**Polimorfismo Estático ou Sobrecarga**

Ocorre onde o mesmo método é implementado várias vezes na mesma classe. Métodos sobrecarregados são escritos com o mesmo nome, mas com uma lista de argumentos diferentes. São geralmente usados dentro de uma mesma classe.
É importante notar que existem algumas regras para a sobrecarga acontecer.

**Polimorfismo Dinâmico ou Sobrescrita**
Acontece ao utilizarmos herança ou realizar uma interface, quando a subclasse sobrepõe ou implementa o método original. O método escolhido se dará em tempo de execução e não mais em tempo de compilação. Os métodos são implementados/modificados nas subclasses, ganhando corpo de acordo com as necessidades específicas de cada uma. A sobrescrita de métodos consiste basicamente em criar um novo método na classe filha contendo a mesma assinatura e mesmo tipo de retorno do método sobrescrito.