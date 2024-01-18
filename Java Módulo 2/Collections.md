# Collections 

Em Java, as Collections (Coleções) são **estruturas de dados** que fornecem maneiras eficientes e convenientes de armazenar e manipular grupos de objetos. As Collections fazem parte do framework Collections Framework, que é uma parte fundamental da API Java para manipulação de dados.
É essencial que os desenvolvedores conheçam a API. Elas estão em todos os lugares.

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


## Links Auxiliares

- [Collections Java](https://www.alura.com.br/conteudo/java-collections?utm_term=&utm_campaign=%5BSearch%5D+%5BPerformance%5D+-+Dynamic+Search+Ads+-+Artigos+e+Conte%C3%BAdos&utm_source=adwords&utm_medium=ppc&hsa_acc=7964138385&hsa_cam=11384329873&hsa_grp=111087461203&hsa_ad=687448474447&hsa_src=g&hsa_tgt=dsa-810524869174&hsa_kw=&hsa_mt=&hsa_net=adwords&hsa_ver=3&gad_source=1&gclid=Cj0KCQiAtaOtBhCwARIsAN_x-3JCZeY4rbShhhQrLe79WgDuUhsCGHIDbEpNWsxm9b3zCfzv00sEb1QaAmBrEALw_wcB)