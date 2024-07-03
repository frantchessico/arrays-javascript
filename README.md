# Arrays

Em JavaScript, um array é uma estrutura de dados usada para armazenar múltiplos valores em uma única variável. Um array pode conter uma lista de elementos, que podem ser de qualquer tipo, incluindo números, strings, objetos e até mesmo outros arrays.



JavaScript oferece uma ampla gama de métodos para manipular arrays. Aqui está uma lista completa dos métodos de arrays em JavaScript, junto com suas explicações e exemplos:

### Métodos de Manipulação de Elementos

1. **`push()`**: Adiciona um ou mais elementos ao final do array e retorna o novo comprimento.
    ```javascript
    let frutas = ["maçã", "banana"];
    frutas.push("laranja"); // ["maçã", "banana", "laranja"]
    ```

2. **`pop()`**: Remove e retorna o último elemento do array.
    ```javascript
    let frutas = ["maçã", "banana", "laranja"];
    let ultimaFruta = frutas.pop(); // "laranja"
    ```

3. **`shift()`**: Remove e retorna o primeiro elemento do array.
    ```javascript
    let frutas = ["maçã", "banana", "laranja"];
    let primeiraFruta = frutas.shift(); // "maçã"
    ```

4. **`unshift()`**: Adiciona um ou mais elementos ao início do array e retorna o novo comprimento.
    ```javascript
    let frutas = ["maçã", "banana"];
    frutas.unshift("laranja"); // ["laranja", "maçã", "banana"]
    ```

### Métodos de Reordenação

5. **`reverse()`**: Inverte a ordem dos elementos no array.
    ```javascript
    let numeros = [1, 2, 3];
    numeros.reverse(); // [3, 2, 1]
    ```

6. **`sort()`**: Ordena os elementos do array.
    ```javascript
    let frutas = ["banana", "laranja", "maçã"];
    frutas.sort(); // ["banana", "laranja", "maçã"]

    let numeros = [4, 2, 5, 1, 3];
    numeros.sort((a, b) => a - b); // [1, 2, 3, 4, 5]
    ```

### Métodos de Manipulação de Subconjuntos

7. **`splice()`**: Adiciona/remova elementos de um array.
    ```javascript
    let frutas = ["maçã", "banana", "laranja"];
    frutas.splice(1, 1, "kiwi"); // ["maçã", "kiwi", "laranja"]
    ```

8. **`slice()`**: Retorna uma cópia superficial de uma parte do array.
    ```javascript
    let frutas = ["maçã", "banana", "laranja"];
    let novasFrutas = frutas.slice(1, 3); // ["banana", "laranja"]
    ```

### Métodos de Pesquisa

9. **`indexOf()`**: Retorna o primeiro índice em que um elemento pode ser encontrado no array.
    ```javascript
    let frutas = ["maçã", "banana", "laranja"];
    let indice = frutas.indexOf("banana"); // 1
    ```

10. **`lastIndexOf()`**: Retorna o último índice em que um elemento pode ser encontrado no array.
    ```javascript
    let frutas = ["maçã", "banana", "laranja", "banana"];
    let indice = frutas.lastIndexOf("banana"); // 3
    ```

11. **`includes()`**: Verifica se um array contém um determinado elemento.
    ```javascript
    let frutas = ["maçã", "banana", "laranja"];
    let temBanana = frutas.includes("banana"); // true
    ```

12. **`find()`**: Retorna o primeiro elemento no array que satisfaz a função de teste fornecida.
    ```javascript
    let numeros = [1, 2, 3, 4];
    let primeiroPar = numeros.find((num) => num % 2 === 0); // 2
    ```

### Métodos de Iteração

13. **`forEach()`**: Executa uma função para cada elemento do array.
    ```javascript
    let frutas = ["maçã", "banana", "laranja"];
    frutas.forEach((fruta) => console.log(fruta));
    ```

14. **`map()`**: Cria um novo array com os resultados de chamar uma função para cada elemento do array.
    ```javascript
    let numeros = [1, 2, 3];
    let dobrados = numeros.map((num) => num * 2); // [2, 4, 6]
    ```

15. **`filter()`**: Cria um novo array com todos os elementos que passaram no teste implementado pela função fornecida.
    ```javascript
    let numeros = [1, 2, 3, 4, 5];
    let pares = numeros.filter((num) => num % 2 === 0); // [2, 4]
    ```

16. **`reduce()`**: Aplica uma função contra um acumulador e cada elemento do array (da esquerda para a direita) para reduzi-lo a um único valor.
    ```javascript
    let numeros = [1, 2, 3, 4];
    let soma = numeros.reduce((total, num) => total + num, 0); // 10
    ```

17. **`reduceRight()`**: Aplica uma função contra um acumulador e cada elemento do array (da direita para a esquerda) para reduzi-lo a um único valor.
    ```javascript
    let numeros = [1, 2, 3, 4];
    let soma = numeros.reduceRight((total, num) => total + num, 0); // 10
    ```

### Outros Métodos Úteis

18. **`some()`**: Verifica se ao menos um elemento no array passa no teste implementado pela função fornecida.
    ```javascript
    let numeros = [1, 2, 3, 4];
    let temPar = numeros.some((num) => num % 2 === 0); // true
    ```

19. **`every()`**: Verifica se todos os elementos no array passam no teste implementado pela função fornecida.
    ```javascript
    let numeros = [1, 2, 3, 4];
    let todosPositivos = numeros.every((num) => num > 0); // true
    ```

  

20. **`findIndex()`**: Retorna o índice do primeiro elemento no array que satisfaz a função de teste fornecida.
    ```javascript
    let numeros = [1, 2, 3, 4];
    let indicePrimeiroPar = numeros.findIndex((num) => num % 2 === 0); // 1
    ```

21. **`from()`**: Cria um novo array a partir de um objeto semelhante a um array ou iterable.
    ```javascript
    let arrayLike = {0: "a", 1: "b", length: 2};
    let arr = Array.from(arrayLike); // ["a", "b"]
    ```

22. **`isArray()`**: Verifica se um valor é um array.
    ```javascript
    let valor = [1, 2, 3];
    Array.isArray(valor); // true
    ```

23. **`of()`**: Cria uma nova instância de Array com um número variável de elementos.
    ```javascript
    let arr = Array.of(1, 2, 3); // [1, 2, 3]
    ```

24. **`concat()`**: Mescla dois ou mais arrays.
    ```javascript
    let arr1 = [1, 2];
    let arr2 = [3, 4];
    let novoArray = arr1.concat(arr2); // [1, 2, 3, 4]
    ```

25. **`join()`**: Junta todos os elementos de um array (ou um array-like object) em uma string e retorna essa string.
    ```javascript
    let frutas = ["maçã", "banana", "laranja"];
    let listaDeFrutas = frutas.join(", "); // "maçã, banana, laranja"
    ```

### Métodos de Chave e Valor

26. **`keys()`**: Retorna um novo Array Iterator que contém as chaves para cada índice no array.
    ```javascript
    let frutas = ["maçã", "banana"];
    let chaves = frutas.keys();
    for (let chave of chaves) {
        console.log(chave); // 0, 1
    }
    ```

27. **`values()`**: Retorna um novo Array Iterator que contém os valores para cada índice no array.
    ```javascript
    let frutas = ["maçã", "banana"];
    let valores = frutas.values();
    for (let valor of valores) {
        console.log(valor); // "maçã", "banana"
    }
    ```

28. **`entries()`**: Retorna um novo Array Iterator que contém pares chave/valor para cada índice no array.
    ```javascript
    let frutas = ["maçã", "banana"];
    let entradas = frutas.entries();
    for (let entrada of entradas) {
        console.log(entrada); // [0, "maçã"], [1, "banana"]
    }
    ```

