---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# Big O Notation

## Introdução à complexidade de algoritmos no tempo e no espaço

---

# Conceitos básicos

## Algoritmo

## Função

## Complexidade

---

# Algoritmo

Um algoritmo é uma **sequência ordenada** de instruções e/ou operações sistemáticas afim de obter um **resultado específico**.

---

# Função

É uma relação entre dois conjuntos: entradas e saídas.

Exemplo: **f(x) => x \* 2 + 1**

```
1 => 3
2 => 5
3 => 7
4 => 9
10 => 21
[...]
```

---

# Anatomia da função

## f(x) => r

**f** = função - ou metódo
**x** = argumento de entrada - ou parâmetro
**r** = resultado da função - ou saida

---

# Complexidade

Descreve o número de operações executadas por um algoritmo em relação ao tamanho do argumento de entrada.

Por exemplo:

Um algoritmo que recebe com argumento uma lista, pode consumir mais ou menos **recursos** de acordo com o número de items nessa lista.

---

### Recursos:

**Tempo**: duração da execução. Influenciado pelo número de operações realizadas e o tempo que cada uma delas leva.

**Espaço**: alocação de memória durante a execução. Influenciado pelas informações armazenadas pelo algoritmo.

---

# O que é Big O Notation?

É uma notação - **uma forma de expressar** em termos matemáticos - as **limitações** de uma função em relação aos argumentos que ela recebe.

É utilizado para **categorizar** problemas e algoritmos baseado no **uso de recursos** de acordo com o **tamanho** dos argumentos de entrada.

---

# Características do Big O Notation

- Considera apenas as repetições, ignorando o custo de operações individuais;
- Descreve a complexidade no pior caso possível;
- É descrito em termos de uma função **O** que, normalmente, recebe o argumento **n** que representa o tamanho do argumento de entrada.
- Pode apresentar outros argumentos em casos mais elaborados.

---

# Porque isso importa?

- Eficiência
- Escalabilidade
- Entrevistas de emprego
- Diversão (????)

---

# O(1) complexidade constante

É a mais simples possível. Independente do tamanho do input a execução não varia.

```
function double(n: number) {
  return n * 2
}
```

```
function min(n1: number, n2: number) {
  if(n1 > n2) return n2

  return n1
}
```

---

# O(n) complexidade linear

São funções em que a complexidade cresce na mesma proporção que o tamanho do input.

```
function findIndex(word: string, unorderedList: string[]) {
  for(let i = 0, i < unorderedList.lenght, i++) {
    if(unorderedList[i] === word) return i
  }

  return null
}
```

---

# O(n²) complexidade quadrática

São funções em que a complexidade cresce elevado à potencia de 2 em relação ao tamanho do input.

Exemplo:

```
function logAllPairs(list: number[]) {

  for (let i = 0; i < list.length; i++) {
    for (let j = 0; j < list.length; j++) {
      console.log(list[i], list[j])
    }
  }
}
```

---

# O(log(n)) complexidade logarítimca

```
function(n:number, sortedList: number[]) {
  let [left, right] = [0, sortedList.length - 1]

  while(left <= right){
    let mid = Math.floor((left + right) / 2)
    if (sortedList[mid] === n) {
      return mid
    } else if (sortedList[mid] > n) {
      right = mid - 1
    } else {
      left = mid + 1
    }
  }
  return null
}
```

---

# Referências

[Big-O Algorithm Complexity Cheat Sheet](https://www.bigocheatsheet.com/)

[Algorithm Visualizer](https://tamimehsan.github.io/AlgorithmVisualizer/#/sort)

[Why The Logarithm Is So Important For Algorithms & Data Structures](https://www.youtube.com/watch?v=ho1eFp1nDEo)

[Big-O Notation - Full Course](https://www.youtube.com/watch?v=Mo4vesaut8g)

[Algorithms and Data Structures Tutorial - Full Course for Beginners](https://www.youtube.com/watch?v=ho1eFp1nDEo)

[LeetCode](https://leetcode.com/)
