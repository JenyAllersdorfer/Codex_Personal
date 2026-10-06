---
topic: Paradigma Estrutural, Classes e Objetos
---

# 🧠 POO - Introdução ao Paradigma e Abstração

## ⚙️ 1. O que é um Paradigma?
Um **paradigma** define um padrão ou modelo conceitual a ser seguido no desenvolvimento de software. 

*   **Programação Imperativa:** Baseia-se em comandos sequenciais que alteram o estado de variáveis (Ex: C, Pascal). O foco é *como* fazer.
*   **Programação Orientada a Objetos (POO):** Baseia-se na composição e interação entre **objetos** independentes. O foco é aproximar o código da cognição humana de forma intuitiva.

---

## 🧱 2. Os Elementos de Fundação
O processo de mapear o mundo real para o código chama-se **Abstração**. Ele seleciona características relevantes e descarta detalhes inúteis.

*   **Classe:** É a definição abstrata, o **molde ou projeto** que representa um conjunto de características comuns.
*   **Objeto:** É uma **instância concreta** de uma classe na memória do computador. 
    *   *Exemplo:* Da classe `Humano`, nós indivíduos reais somos os objetos instanciados.
*   **Atributo:** Característica ou propriedade de um objeto (dados/estado).
*   **Método:** Operação, função ou procedimento que dita as ações que o objeto pode realizar.

### ⚖️ Coesão vs. Acoplamento (Essencial para a Prova!)
*   **Coesão (Deseja-se ALTA):** Mede se a classe possui uma finalidade única e bem definida. Classes coesas fazem apenas uma coisa e fazem bem feito.
*   **Acoplamento (Deseja-se BAIXO):** Mede o nível de interdependência e conhecimento entre classes. Se alterar a Classe A quebra a Classe B, o acoplamento está perigosamente alto.

---

## 💻 3. Anatomia do Código Java (Interpretação)

Toda classe executável em Java necessita obrigatoriamente do método de inicialização **`main`**.

```java
// O nome da classe DEVE ser rigorosamente idêntico ao nome do arquivo .java
public class HelloWorldConsole {
    
    // Ponto inicial de execução do algoritmo
    public static void main(String args[]) {
        // Imprime uma string na saída padrão do console
        System.out.println("Hello, World!!!");
    }
}
```

### 🚨 Pegadinhas de Código Comuns:
1. **Case Sensitivity:** Java diferencia estritamente maiúsculas de minúsculas (`String` funciona, `string` gera erro de compilação).
2. **Arquivos Incompletos:** Se uma classe não possuir a assinatura `public static void main(String[] args)`, ela é tratada apenas como uma classe conceitual e não pode ser executada de forma direta.

---
## 🏋️‍♂️ Exercício Prático da UFMT
Crie classes conceituais básicas para representar o comportamento de um conjunto de `Quadrados` e de `Clientes`.

- [ ] Resolver exercício conceitual de Quadrados no caderno.
