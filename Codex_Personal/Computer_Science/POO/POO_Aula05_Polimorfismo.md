---
topic: Polimorfismo
---

# 🧠 POO - Polimorfismo (Aula 5)

## 🎭 1. O que é?
É a capacidade de uma **mesma referência/chamada de método** se comportar de forma diferente dependendo do **objeto real** que está por trás dela — cada subclasse executa a sua própria versão sobrescrita.

```java
Funcionario f = new Gerente(); // referência Funcionario, objeto real é Gerente
f.exibeDados(); // executa o exibeDados() do Gerente, não o de Funcionario
```
O Java decide **em tempo de execução** qual versão do método rodar, olhando pro objeto real, não pro tipo da referência. Isso é a base de exercícios como "Veterinario examina diferentes Animais" ou "Piloto pilota diferentes Veiculos" — o mesmo método chama comportamentos diferentes dependendo do objeto passado.

---

## 🔄 2. Casting
Converter uma referência de um tipo pra outro **dentro da mesma hierarquia**.

```java
Funcionario f = new Gerente();
Gerente g = (Gerente) f;  // casting: "garanto que f é um Gerente"
```
Cuidado: se o objeto real **não for** do tipo pro qual você está convertendo, o programa quebra em tempo de execução (`ClassCastException`).

---

## 🔍 3. instanceof
Verifica se um objeto é de um determinado tipo **antes** de fazer o casting — evita o erro acima.

```java
if (f instanceof Gerente) {
    Gerente g = (Gerente) f;
    // seguro fazer o casting aqui
}
```

---

## ⚖️ 4. Sobrecarga x Sobrescrita (não confundir!)

| | Sobrecarga (overload) | Sobrescrita (override) |
|---|---|---|
| Onde | Mesma classe (ou construtor) | Subclasse redefinindo método da superclasse |
| Nome do método | Igual | Igual |
| Parâmetros | **Diferentes** | **Iguais** (mesma assinatura) |
| Quando decide qual rodar | Em tempo de **compilação** (pelos parâmetros passados) | Em tempo de **execução** (pelo objeto real) — isso é polimorfismo de verdade |

> Pegadinha clássica: os slides mostram dois trechos de código parecidos e perguntam "qual está certo?" — geralmente um muda só o tipo de retorno (errado, isso **não é** sobrecarga válida nem sobrescrita válida) e o outro muda os parâmetros corretamente ou mantém a assinatura idêntica.

---

## 🏋️‍♂️ Exercícios Práticos da UFMT
- [ ] `Pagamento` (valor, `calcularValorFinal()`) → `PagamentoCartao` (+2%) e `PagamentoBoleto` (-5%); main com array de `Pagamento` misturando os dois tipos.
- [ ] `Animal` (`fazerSom()`) → `Cachorro`, `Gato`, `Passaro`; classe `Veterinario` com `examinar(Animal animal)` chamando `animal.fazerSom()`.
- [ ] `Veiculo` (`mover()`) → `Carro` e `Aviao`; classe `Piloto` com `pilotar(Veiculo)` chamando `.mover()`.
- [ ] `Funcionario` (nome, salarioBase, `calcularVencimento()`) → `Gerente` (+bonusFixo) e `Vendedor` (+comissao); `Empresa` com `ArrayList<Funcionario>` e `gerarFolhaPagamento()` que soma via polimorfismo.