
# 🧠 Modificadores de Acesso (Aula 3)

## 🔐 1. O que são?
Definem o **escopo/visibilidade** de um atributo ou método — ou seja, quem no sistema pode enxergar e usar aquele atributo/método. É o que cria a "interface" entre a classe e o mundo externo.

---

## 🚦 2. Os 4 tipos

| Modificador | Símbolo (UML) | Quem acessa |
|---|---|---|
| `public` | `+` | Qualquer classe do sistema, de qualquer pacote |
| `protected` | `#` | Classes que têm relação de **herança** com ela, mesmo em pacote diferente |
| *(nenhum, "package")* | `~` | Só classes do **mesmo pacote** |
| `private` | `-` | Só a **própria classe** |

> Não existe a palavra-chave `package` — quando você **não escreve nenhum modificador**, o Java já entende que é `package` por padrão.

---

## 🧩 3. Onde ficam no código
O modificador vem **antes do tipo** do atributo, ou antes do tipo de retorno do método.

```java
public class Cliente {
    private String nome;
    private int idade;

    public void setNome(String nome) {
        this.nome = nome;
    }

    public String getNome() {
        return this.nome;
    }

    protected void setIdade(int idade) {
        if (idade >= 0) {
            this.idade = idade;
        }
    }
}
```

- `nome` e `idade` são `private` → **encapsulados**, ninguém de fora mexe direto.
- `setNome`/`getNome` são `public` → **interface** da classe com o mundo externo.
- `setIdade` é `protected` → só quem herda de `Cliente` pode chamar.

---

## 🔍 4. Regra de ouro
> `public` = a classe **interage** com o meio externo (é uma interface pra ele).
> `private` = está **encapsulado**, não existe comunicação com o meio externo.

Normalmente: **atributos → private**, **métodos → public** (pra permitir o acesso via gets/sets).

---

## 🚨 Pegadinha clássica de prova
```java
public class C {
    private void m(int x) {
        x = x + 5;
    }
    public void t() {
        int x = 10;
        m(x);
        // qual o valor de x aqui?
    }
}
```
Pergunta: *quem pode chamar `m()`?* Resposta: só a própria classe `C` — mas isso inclui chamar **de dentro de outro método da mesma classe**, como `t()` está fazendo. `private` bloqueia acesso de **fora** da classe, não de dentro dela.

E sobre o valor de `x`: como `int` é passado **por valor** (cópia), o `x` dentro de `t()` continua `10` depois de chamar `m(x)` — a alteração dentro de `m` não volta pro `x` de fora.

---

## 🏋️‍♂️ Exercícios Práticos da UFMT
- [ ] Classe `Produto` (código, nome, preço) com sets/gets — classe executável registra 5 produtos e acha o maior/menor preço (usar vetor + `Scanner` pra ler do console).
- [ ] Classe `Data` (dia, mês, ano) com construtor que valida consistência, gets/sets, método que avança pro dia seguinte, e método que retorna string `"dd/mm/aa"`.