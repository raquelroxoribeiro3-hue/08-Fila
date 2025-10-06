# Fila

---

## 🎯 Objetivos

Ao concluir esta atividade, você deverá compreender e aplicar os seguintes conceitos fundamentais:

* Estrutura de dados do tipo **FIFO (First In / First Out)**.
* Funcionamento de uma **fila dinâmica** implementada com **ponteiros**.
* Manipulação de memória na **inserção** e **remoção** de elementos.
* Relação entre os ponteiros **início** e **fim** no controle da estrutura.

---

## 🧠 Conceito de Fila

Uma **fila** é uma estrutura linear onde o **primeiro elemento a entrar é o primeiro a sair**.
A inserção é feita **no final da fila**, e a remoção ocorre **no início**.

Esse comportamento é semelhante a uma fila de pessoas em um atendimento:
quem chega primeiro é atendido primeiro.

| Operação        | Descrição                                          |
| --------------- | -------------------------------------------------- |
| **Inserir**     | Adiciona um novo elemento ao final da fila.        |
| **Remover**     | Retira o elemento que está no início da fila.      |
| **Inicializar** | Limpa toda a estrutura, liberando a memória usada. |

---

## 🧩 Estrutura do Código

O código utiliza uma **estrutura de nó** contendo um valor e um ponteiro para o próximo elemento.
Dois ponteiros globais controlam a fila:

* **início** → aponta para o primeiro elemento (o próximo a ser removido).
* **fim** → aponta para o último elemento (onde novos dados são inseridos).

Esses ponteiros são atualizados a cada operação, garantindo o funcionamento dinâmico da fila.

---

## 🎬 Funcionamento da Fila

### 📥 Inserção de Elementos (Operação: *insere*)

Cada novo elemento é inserido **no final da fila**.
Veja a sequência abaixo:

#### Situação inicial — fila vazia:

```
inicio → NULL
fim → NULL
```

#### Inserindo o valor 10:

```
inicio → [10] → NULL
fim ────────┘
```

#### Inserindo o valor 20:

```
inicio → [10] → [20] → NULL
               ↑         ↑
             primeiro   último
```

#### Inserindo o valor 30:

```
inicio → [10] → [20] → [30] → NULL
```

---

### 📤 Remoção de Elementos (Operação: *remove*)

A remoção ocorre sempre **no início da fila**.
O elemento removido é aquele que entrou há mais tempo.

#### Fila atual:

```
inicio → [10] → [20] → [30] → NULL
```

#### Após remover um elemento:

```
Removido: 10
inicio → [20] → [30] → NULL
```

#### Após remover novamente:

```
Removido: 20
inicio → [30] → NULL
fim ───────┘
```

#### Fila vazia novamente:

```
inicio → NULL
fim → NULL
```

---

## 🧰 Atividade Proposta

Faça um **fork** deste repositório e realize as seguintes tarefas no arquivo `Fila.cpp`:

1. **Completar a função `insere`**

   * Deve incluir um novo elemento no final da fila.
   * Se a fila estiver vazia, o novo elemento será o primeiro e o último.
   * Caso contrário, ele deve ser conectado ao final, e o ponteiro **fim** atualizado.

2. **Implementar a função `remove`**

   * Deve exibir o valor do primeiro elemento e removê-lo.
   * Se a fila estiver vazia, deve exibir a mensagem **"Fila Vazia"**.
   * Após remover o último elemento, o ponteiro **fim** deve ser ajustado para indicar que a fila está vazia.

---

## 🧪 Testes sugeridos


1. Inicialize a fila.
2. Insira alguns valores.
3. Remova os elementos um a um.
4. Verifique se a ordem segue corretamente o princípio **FIFO** — o primeiro elemento inserido deve ser o primeiro removido.

---
## 💾 Entrega

* Faça o **fork** do repositório.
* Implemente as funções `insere()` e `remove()` conforme descrito.
* Realize **commits** explicativos (por exemplo: “Implementação da função insere()”).
* Envie o link do repositório no **Teams** 

