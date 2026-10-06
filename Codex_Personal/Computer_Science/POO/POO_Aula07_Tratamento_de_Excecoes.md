---
topic: Tratamento de Exceções
---

# 🧠 POO - Tratamento de Exceções (Aula 7)

## ⚠️ 1. O que é uma Exceção?
É um **erro que acontece durante a execução** do programa e quebra o fluxo normal (ex: dividir por zero, acessar índice inválido de um vetor, converter texto inválido pra número).

---

## 🧰 2. Try / Catch
```java
try {
    int resultado = a / b;
    System.out.println(resultado);
} catch (ArithmeticException e) {
    System.out.println("Erro: Divisão por zero não é permitida.");
}
```
- O Java tenta rodar o `try`. Se uma exceção acontece, ele **para ali** e procura um `catch` compatível com o tipo de exceção lançada.
- Se achar um `catch` compatível → trata o erro e **o programa continua** rodando dali pra frente (não volta pro ponto exato do erro).
- Se **não** achar `catch` compatível → o programa (ou a thread) é encerrado abruptamente.

Pra repetir a entrada até o usuário acertar, normalmente usa-se um `while` em volta do `try/catch`:
```java
boolean valido = false;
while (!valido) {
    try {
        int indice = scanner.nextInt();
        System.out.println(vetor[indice]);
        valido = true;
    } catch (ArrayIndexOutOfBoundsException e) {
        System.out.println("Erro: Índice fora dos limites do vetor.");
    }
}
```

---

## 🎯 3. Lançando uma Exceção (`throw`)
Você mesmo pode disparar uma exceção quando uma regra de negócio é violada:
```java
if (nota < 0 || nota > 10) {
    throw new NotaInvalidaException("Erro: A nota deve estar entre 0 e 10.");
}
```

## 📤 4. Propagando uma Exceção (`throws`)
Um método pode **não tratar** a exceção e só avisar que ela pode acontecer, repassando a responsabilidade pra quem chamou ele:
```java
void processar() throws NotaInvalidaException {
    // ...
}
```

---

## 🪜 5. Hierarquia de Exceções
Todas as exceções derivam de `Throwable` → `Exception` (tratáveis, ex: `IOException`) ou `Error` (erros graves do sistema, não deveriam ser tratados). Dentro de `Exception` existem subclasses prontas do Java (`ArithmeticException`, `ArrayIndexOutOfBoundsException`, `NullPointerException`, etc.).

## 🏗️ 6. Criando sua própria Exceção
Herda de `Exception` (ou de uma subclasse dela):
```java
public class NotaInvalidaException extends Exception {
    public NotaInvalidaException(String mensagem) {
        super(mensagem); // passa a mensagem pro construtor da superclasse
    }
}
```

---

## 🚨 Pegadinha de Prova
Depois que um `catch` trata o erro, o programa **não volta** pra linha onde a exceção aconteceu — ele segue a partir do fim do bloco `try/catch`. Se você precisa repetir a ação (ex: pedir a entrada de novo), **tem que colocar o `try` dentro de um loop**, o catch sozinho não repete nada.

---

## 🏋️‍♂️ Exercícios Práticos da UFMT
- [ ] Vetor com 5 contas bancárias (da Aula 4) — tratar exceções nas operações de saque, saldo e depósito.
- [ ] Ler um `float` do teclado; se inválido, pedir de novo; após 3 tentativas inválidas, encerrar com "Excedeu o limite de tentativas."
- [ ] Ler dois inteiros e dividir; capturar `ArithmeticException` em divisão por zero, repetindo a pergunta até um divisor válido.
- [ ] Vetor de 5 inteiros; pedir um índice; capturar `ArrayIndexOutOfBoundsException` se fora de 0 a 4, repetindo até um índice válido.
- [ ] Criar `NotaInvalidaException extends Exception`; ler nota exigindo 0–10, lançando a exceção customizada se inválida, até um valor válido ser dado.