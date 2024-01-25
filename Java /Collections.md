# Collections 

Em Java, as Collections (Coleções) são **estruturas de dados** que fornecem maneiras eficientes e convenientes de armazenar e manipular grupos de objetos. As Collections fazem parte do framework Collections Framework, que é uma parte fundamental da API Java para manipulação de dados.
É essencial que os desenvolvedores conheçam a API. Elas estão em todos os lugares.

<a><img src = "./assets/estruturaCollection.jpeg"/></a>

Em seu core existem interfaces , as principais são:

| Nome| O que é |
|----------|----------|
| Collection | A interface raiz na hierarquia de coleções   |
| List  | Representa uma lista ordenada   |
| Set  | Representa um conjunto que não permite modificações   |
| Map  | Representa o mapeamento chave-valor   |
| Queue| Representa uma fila|

>Os nomes acima são suas implementações genéricas.  

Mais concretas:


|Nome | O que é |
|---------|------------|
|ArrayList|Implementação de uma lista redimensionável|
|LinkedList|Implementação de uma lista duplamente encadeada|
|HashSet|Implementação de um conjunto baseado em tabela de dispersão|
|TreeSet|Implementação de um conjunto ordenado|
|HashMap|Implementação de um mapa baseado em tabela de disperção|
|TreeMap|Implementação de um mapa ordenado|

### Iteração e Acesso aos Elementos
As coleções fornecem métodos para acessar e iterar sobre seus elementos. O loop *for-each* é frequentemente utilizado para percorrer coleções

Exemplo: 
```
List<String> nomes = new ArrayList<>();
nomes.add("Samuel");
nomes.add("João");
nomes.add("Joy");
nomes.add("Dandara");

for(String elemento: lista){
    System.out.println(elemento);
}
```
>Importante destacar que as Collection não aceitam tipos primitivos, apenas Wrapper Classes. *Notem que dentro do <>(diamante) tipamos a nossa ArrayList como String.* 

## Interface List
É uma extensão (herdando) da interface Collection. Como caracteristica tem os elementos ordenados como uma sequência. A interface é como uma array de tamanho varíavel, pois tem total controle sobre elementos inseridos nas lista, já que em sua utilização podemos acessar um determinado elemento através do índice. 

## Principais Caracteristicas: 
| |  |
|----------|----------|
| Ordenação | Os elementos em uma lista são mantidos em uma ordem específica.|
|Índices  | Cada elemento na lista é acessado por um índice inteiro, começando do zero. |
| Duplicatas | Permite a existência de elementos duplicados. |

## Métodos mais utilizados
| |  |
|----------|----------|
| add(elemento) | Adiciona um elemento ao final da lista.|
| remove(index)  |  Remove o elemento na posição específica da lista.|
| get(index): |  Retorna o elemento na posição especificada.|
| indexOf(element)|Retorna o índice da primeira ocorrência do elemento na lista.|
| size():|Retorna o número de elementos na lista.|


## Implementações conhecidas

| |  |
|----------|----------|
| ArrayList | Baseado em arrays dinâmicos, eficiente para acesso direto aos elementos|
| LinkedList | Implementação baseada em uma lista duplamente encadeada, eficiente para inserções e remoções no meio da lista |


## Array List
```

public static void main(String[] args) {
		List<String> nomes = new ArrayList<>();
		nomes.add("Samuel");
		nomes.add("João");
		nomes.add("Joy");
		nomes.add("Dandara");
		
		//Percorrendo a lista
		for(String nome: nomes) {
			System.out.println(nome);
		}
		System.out.println("--------------------------------");
		
		// Removendo a primeira posição
		nomes.remove(0);
		
		//Acessando a primeira posição
		System.out.println(nomes.get(0));
		
		System.out.println("--------------------------------");
		
		//Pegando a posição do elemento
		System.out.println(nomes.indexOf("Joy"));
		
		System.out.println("--------------------------------");
		
		//Trazendo o tamanho da lista 
		System.out.println(nomes.size());
	}

```

### Saída no console
```
Samuel
João
Joy
Dandara
--------------------------------
João
--------------------------------
1
--------------------------------
3

```


## Linked List


```

// Criando uma lista encadeada
        List<String> nomes = new LinkedList<>();

        // Adicionando elementos à lista
        nomes.add("Samuel");
        nomes.add("João");
        nomes.add("Joy");
        nomes.add("Dandara");

        // Exibindo a lista
        System.out.println("Lista original: " + nomes);

        // Obtendo o elemento na posição 2 (índice 1)
        String elementoNaPosicao2 = nomes.get(1);
        System.out.println("Elemento na posição 2: " + elementoNaPosicao2);

        // Encontrando o índice do elemento "Joy"
        int indiceJoy = nomes.indexOf("Joy");
        System.out.println("Índice de 'Joy': " + indiceJoy);

        // Removendo o elemento "João"
        nomes.remove("João");
        System.out.println("Lista após remover 'João': " +  nomes);

        // Tamanho da lista após remoção
        int tamanhoLista =  nomes.size();
        System.out.println("Tamanho da lista: " + tamanhoLista);

        // Iterando pela lista
        System.out.println("Iteração:");
        for (String elemento :  nomes) {
            System.out.println(elemento);
        }

```
### Saída no console

```
Lista original: [Samuel, João, Joy, Dandara]
Elemento na posição 2: João
--------------------------------------------------------
Índice de 'Joy': 2
--------------------------------------------------------
Lista após remover 'João': [Samuel, Joy, Dandara]
--------------------------------------------------------
Tamanho da lista: 3
--------------------------------------------------------
Iteração:
Samuel
Joy
Dandara

```
## Links Auxiliares

- [Collections Java](https://www.alura.com.br/conteudo/java-collections?utm_term=&utm_campaign=%5BSearch%5D+%5BPerformance%5D+-+Dynamic+Search+Ads+-+Artigos+e+Conte%C3%BAdos&utm_source=adwords&utm_medium=ppc&hsa_acc=7964138385&hsa_cam=11384329873&hsa_grp=111087461203&hsa_ad=687448474447&hsa_src=g&hsa_tgt=dsa-810524869174&hsa_kw=&hsa_mt=&hsa_net=adwords&hsa_ver=3&gad_source=1&gclid=Cj0KCQiAtaOtBhCwARIsAN_x-3JCZeY4rbShhhQrLe79WgDuUhsCGHIDbEpNWsxm9b3zCfzv00sEb1QaAmBrEALw_wcB)
