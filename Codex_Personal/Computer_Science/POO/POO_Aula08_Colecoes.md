
# 🧠 Coleções (Aula 8)

## 📦 1. Tipos de Coleção

| Interface | O que é | Implementação comum |
|---|---|---|
| `List` | Lista ordenada, **permite duplicados**, acesso por índice | `ArrayList` |
| `Set` | Conjunto, **não permite duplicados** | `HashSet` |
| `Map` | Pares chave-valor, **chave única** | `HashMap` |
| `Queue` | Fila: primeiro a entrar, primeiro a sair (FIFO) | — |
| `Stack` | Pilha: último a entrar, primeiro a sair (LIFO) | — |

---

## 📋 2. List (ArrayList)
```java
ArrayList<String> carrinho = new ArrayList<>();
carrinho.add("Arroz");
carrinho.add("Feijão");
carrinho.size();        // quantidade de itens
carrinho.remove(1);     // remove pelo índice (int!)
for (String item : carrinho) {
    System.out.println(item); // for-each
}
```
> Repare: `.remove(int)` remove pelo **índice**; se a lista fosse de inteiros, `.remove(Integer)` (objeto) removeria pelo **valor** — é um detalhe que costuma confundir.

---

## 🎯 3. Set (HashSet)
```java
HashSet<String> convidados = new HashSet<>();
convidados.add("Ana");
convidados.add("Bruno");
convidados.add("Ana"); // ignorado, já existe
convidados.size(); // conta só os únicos
```
- Não garante manter a ordem de inserção.
- Útil quando você precisa **eliminar duplicatas** automaticamente.

---

## 🗺️ 4. Map (HashMap)
```java
HashMap<String, String> agenda = new HashMap<>();
agenda.put("Ana", "9999-0000");
agenda.get("Ana");              // busca o valor pela chave
agenda.containsKey("Ana");      // true/false
```
Padrão clássico de prova — **contar ocorrências** com `Map<String, Integer>`:
```java
HashMap<String, Integer> contagem = new HashMap<>();
for (String palavra : palavras) {
    if (contagem.containsKey(palavra)) {
        contagem.put(palavra, contagem.get(palavra) + 1);
    } else {
        contagem.put(palavra, 1);
    }
}
```

---

## 🚶 5. Queue (Fila)
FIFO — quem entra primeiro, sai primeiro. `peek()` olha o próximo da fila **sem remover**.

## 🥞 6. Stack (Pilha)
LIFO — quem entra por último, sai primeiro.
- `push()` → insere no topo
- `pop()` → remove e devolve o topo
- `peek()` → olha o topo **sem remover**
- `empty()` → pilha está vazia?

> Pegadinha clássica: converter uma `Stack` pra uma `Queue` inverte a ordem de saída — o topo da pilha (último a entrar) vira o **primeiro** a sair da fila também, mas o resto da ordem interna muda porque pilha e fila percorrem em sentidos opostos.

---

## 🚨 Pegadinha de Prova
Quando a coleção guarda **objetos** (não tipos primitivos nem `String`), comparar dois objetos exige que a classe implemente `equals()` (e geralmente `hashCode()`), senão `Set`/`Map` não sabem identificar duplicatas corretamente — e um `for-each` simples não resolve ordenação por um critério específico (precisa de `Comparable`/`Comparator`).

---

## 🏋️‍♂️ Exercícios Práticos da UFMT
- [ ] `ArrayList<String>` com 4 itens, `.size()`, remover o 2º item, imprimir com for-each.
- [ ] `List<Integer>` de 1 a 10 → filtrar pares pra uma segunda lista.
- [ ] `HashSet<String>` com nomes repetidos → ver tamanho e observar que duplicatas somem.
- [ ] `HashMap<String,String>` agenda de contatos com `.put()`, `.get()`, `.containsKey()`.
- [ ] Array fixo de strings repetidas → `HashMap<String,Integer>` contando ocorrências.
- [ ] Ler nomes até "FIM", remover repetições e informar quantas remoções por nome + total.
- [ ] Classe que recebe uma `Stack` no construtor e tem método `toFila()` que devolve como `Queue`.