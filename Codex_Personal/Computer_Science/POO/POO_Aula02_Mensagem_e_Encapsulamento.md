
# 🧠 Método e Encapsulamento (Aula 2)

## 📨 1. Mensagem
É a forma como os objetos se comunicam entre si: um objeto "manda uma mensagem" pra outro chamando um dos seus métodos (ex: `joao.setNome("João")` é uma mensagem mandada pro objeto `joao`).

---

## 🧱 2. Anatomia de um Método

```java
public class Triangulo {
    float area(int base, int altura) {
        return (base * altura) / 2;
    }
}
```

- `float` → **tipo de retorno**
- `area` → **nome do método**
- `(int base, int altura)` → **parâmetros**, com tipo e separados por vírgula
- `return (base * altura) / 2;` → o valor que o método devolve

Quando o método **não devolve nada**, o tipo de retorno é `void`.

---

## 🏗️ 3. Método Construtor
Método especial, com o **mesmo nome da classe**, chamado automaticamente quando você usa `new`. Serve pra inicializar o objeto.

```java
public class Triangulo {
    int lado1;
    int lado2;
    int lado3;

    Triangulo(int lado1, int lado2, int lado3) {
        this.lado1 = lado1;
        this.lado2 = lado2;
        this.lado3 = lado3;
        System.out.println("Um triangulo foi criado!");
    }
}
```
```java
Triangulo t1 = new Triangulo(3, 4, 5); // chama o construtor
```

- `this.lado1 = lado1;` → `this` referencia **o próprio objeto** que está sendo criado, distinguindo o atributo da classe do parâmetro recebido (ambos se chamam `lado1`).

---

## 🔁 4. Sobrecarga de Métodos (Overload)
Vários métodos com o **mesmo nome**, desde que os parâmetros sejam diferentes — em **tipo**, **quantidade** ou **ordem**.

```java
public class Triangulo {
    float area(int base, int altura) {
        return (base * altura) / 2;
    }
    float area(float base, float altura) {   // mesmo nome, tipos diferentes
        return (base * altura) / 2;
    }
    float area(int lado1, int lado2, int lado3, float raio) { // outra quantidade
        return (lado1 * lado2 * lado3) / (4 * raio);
    }
}
```
Vale até pro **construtor**: pode existir mais de um construtor, contanto que os parâmetros mudem.

---

## 🔒 5. Encapsulamento e Gets & Sets
Encapsular = deixar os atributos `private` (escondidos) e só permitir acesso através de métodos públicos — os **gets** (pra ler o valor) e **sets** (pra alterar o valor).

```java
public class ClassePrincipal {
    public static void main(String[] args) {
        Cliente joao = new Cliente();   // cria um objeto cliente
        joao.setNome("João");            // atribui valores através dos sets
        joao.setIdade(26);

        System.out.println(joao.getNome() + " " + joao.getIdade()); // lê através dos gets
    }
}
```

---

## 🚨 Pegadinhas de Prova
1. Mudar **só o tipo de retorno** não é sobrecarga válida — tem que mudar os parâmetros.
2. `this` só faz sentido **dentro** da classe, referenciando o objeto atual — não confundir com o nome da classe.
3. Construtor **não tem tipo de retorno**, nem `void` — se colocar `void` na frente, deixa de ser construtor e vira um método comum.

---

## 🏋️‍♂️ Exercícios Práticos da UFMT
- [ ] Classe `Círculo` (nome, raio) com sets, diâmetro, área, circunferência e gets.
- [ ] Classe executável que cria dois círculos e informa qual tem maior área.
- [ ] Classe `ContaBancária` (nome, cpf, saldo) com saque, depósito e saldo — sem saque sem saldo.
- [ ] Classe `UrnaEletrônica` (votos brancos, nulos, 2 candidatos) com votar, votar em branco, anular voto e apurar eleição.