
# 🧠 Herança (Aula 4)

## 🌳 1. O que é?
Uma classe (**subclasse**) herda atributos e métodos de outra (**superclasse**), representando uma relação **"é um"**.

`Gerente` herda **diretamente** de `Funcionario` e **indiretamente** de `Pessoa` (herda o que `Funcionario` já herdou).

Pessoa (nome, idade, cpf)  
├── Estudante (curso)  
└── Funcionario (salario)  
└── Gerente  
└── Analista (area)

---

## 🧩 2. Sintaxe
```java
public class Funcionario extends Pessoa {
    double salario;
}
```
`extends` = "estende" a superclasse. `Funcionario` ganha automaticamente `nome`, `idade`, `cpf` de `Pessoa`, além do que é próprio dele (`salario`).

---

## 🏗️ 3. Construtor na herança
O construtor da subclasse pode chamar o construtor da superclasse com `super(...)` (passando o que é da superclasse), e depois inicializa o que é próprio dela.

---

## ✍️ 4. Sobrescrita (Override)
A subclasse redefine um método que já existe na superclasse, com a **mesma assinatura**, mudando o comportamento.

```java
public class AnimalSelvagem {
    void cacar() {
        System.out.println("O animal selvagem está caçando.");
    }
}

public class Leao extends AnimalSelvagem {
    void cacar() {   // sobrescrita
        System.out.println("O leão persegue sua presa na savana.");
    }
}
```

---

## 🔑 5. Regra importante (cai em prova)
> Em Java **não existe herança múltipla**: uma superclasse pode ter várias subclasses, mas **uma subclasse só tem uma superclasse direta**.

(Diferente de interface, que você já viu — lá uma classe pode implementar várias ao mesmo tempo.)

---

## 🔍 6. Criação de objetos
Pode criar o objeto direto da subclasse, **ou** atribuir uma instância da subclasse a uma referência do tipo superclasse:
```java
Funcionario f = new Gerente(); // referência Funcionario, objeto real é Gerente
```
Isso é a base do **polimorfismo**, que vem no próximo tópico.

---

## 🚨 Pegadinha de Prova
Olha com atenção pra exercícios tipo "dadas essas classes, qual o resultado desse código" — eles costumam testar **o que a referência enxerga vs. o que o objeto realmente é**. Guarda essa ideia pra quando chegarmos em Polimorfismo.

---

## 🏋️‍♂️ Exercícios Práticos da UFMT
- [ ] `Conta` → subclasses `ContaPoupanca` (rendimento) e `ContaEspecial` (limite).
- [ ] `Funcionario` → `Assistente` (sobrescreve `exibeDados()`) → `Tecnico` e `Administrativo` (sobrescrevem `ganhoAnual()`).
- [ ] `Imovel` → `Novo` (adicional no preço) e `Velho` (desconto no preço).
- [ ] `Conta` → `ContaCorrente` e `ContaPoupanca` (atributo `variação`).
- [ ] `AnimalSelvagem` (método `caçar()`) → `Leao` e `Lobo` sobrescrevendo.
- [ ] `Forma` (método `desenhar()`) → `Circulo` e `Retangulo` sobrescrevendo.
- [ ] `Veiculo` (marca, modelo, ano) → `Carro` e `Moto` com atributos próprios + tempo de vida do veículo.