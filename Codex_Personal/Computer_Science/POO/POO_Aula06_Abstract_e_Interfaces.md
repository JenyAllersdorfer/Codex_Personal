---
topic: Classes Abstratas e Interfaces
---

# 🧠 POO - Classes Abstratas e Interfaces (Aula 6)

## 🏛️ 1. Classe Abstrata
**Não pode ser instanciada** (não dá pra fazer `new` dela), porque possui pelo menos um **método abstrato** (declarado, mas sem corpo/implementação).

```java
public abstract class Forma {
    private String cor;

    public abstract double calcularArea(); // sem corpo!

    public String getCor() {
        return cor;
    }
    public void setCor(String cor) {
        this.cor = cor;
    }
}
```
- Serve como **molde/superclasse modelo** pra várias subclasses — seu propósito não é criar objetos, é obrigar que todas as subclasses "falem a mesma língua".
- Quem estende `Forma` é **obrigado** a implementar `calcularArea()`. Quem implementa e deixa de ser abstrata vira **classe concreta**:

```java
public class Retangulo extends Forma {
    private int base;
    private int altura;

    public Retangulo(int base, int altura) {
        this.base = base;
        this.altura = altura;
    }

    public double calcularArea() {
        return base * altura; // implementação obrigatória
    }
}
```

---

## 🔌 2. Interface
Classe **sem nenhuma implementação** — só especificação dos métodos (o "contrato").

```java
public interface Ponto {
    float x();
    float y();
    void move(float dx, float dy);
    float distancia(Ponto p);
}

public class PontoImpl implements Ponto {
    private float x, y;
    public float x() { return x; }
    public float y() { return y; }
    public void move(float dx, float dy) { x += dx; y += dy; }
    public float distancia(Ponto p) {
        return (float) Math.sqrt((x - p.x())*(x - p.x()) + (y - p.y())*(y - p.y()));
    }
}
```

**Características:**
- Usa `interface` em vez de `class`.
- **Não tem construtores.**
- Métodos são sempre **públicos e abstratos** — não precisa declarar isso, já é implícito.
- Uma classe pode **implementar várias interfaces ao mesmo tempo** (`implements I1, I2, I3`).
- Uma interface pode **estender outra interface**.
- **Não pode ser instanciada** — assim como classe abstrata.

---

## ⚖️ 3. Herança x Interface — quando usar cada uma

**Use herança quando:**
- A relação é **"é um"** (não "tem um").
- Você quer **reaproveitar código** da superclasse.
- Quer fazer alterações globais nas subclasses mudando só a superclasse.

**Use interface quando:**
- Tipos **possivelmente não relacionados** precisam oferecer a mesma funcionalidade (ex: `Voador` pode ser implementado por `Passaro` e por `Aviao`, que não têm nada a ver entre si).
- Quer mais flexibilidade: uma classe pode implementar várias interfaces, mas só estende **uma** superclasse.
- Não é necessário herdar implementação nenhuma, só o "contrato" dos métodos.

---

## 🚨 Pegadinha de Prova
Pergunta clássica dele: *"Defina o que é Classe Abstrata e Interface e dê exemplos"* — repare que ele quer a **diferença** entre as duas, não só uma definição genérica de "molde". O ponto chave: classe abstrata **pode** ter método já implementado + método abstrato misturados; interface **não implementa nada**, só especifica.

---

## 🏋️‍♂️ Exercícios Práticos da UFMT
- [ ] Organizar numa hierarquia: Avião, Fórmula 1, Ferrari F430, Ferry, Barco de Cruzeiro, Submarino Nuclear, Veículo, Veículo Terrestre, Veículo Aquático, etc.
- [ ] Hierarquia `OperacaoMatematica` → `Soma`, `Subtracao`, `Multiplicacao`, `Divisao`, todas com método `calcula()`.
- [ ] Classe abstrata `CartaoWeb` (atributo `destinatario`, método abstrato `showMessage()`) → subclasses `DiaDosNamorados`, `Natal`, `Aniversario`; array de `CartaoWeb` no main chamando `showMessage()` em loop.
- [ ] Interface `Forma` (perímetro e área) → classe abstrata `Quadrilatero` (recebe os 4 lados, implementa perímetro) → `Retangulo` e `Quadrado` → classe `Circulo` (recebe raio); vetor com todas as formas, imprimindo dados, perímetros e áreas.