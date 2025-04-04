# 🔢 Combinação de Soma Meta

Este repositório contém um script em **Python** que encontra combinações de números dentro de uma lista que somam exatamente a um valor-alvo. O código utiliza a biblioteca `itertools` para testar todas as combinações possíveis e retorna a primeira que atinge o objetivo.

## 🚀 Como funciona?
1. O usuário define uma **lista de números** e um **valor-alvo** (meta).
2. O script percorre todas as combinações possíveis de elementos dessa lista.
3. Se uma combinação cuja soma seja igual à meta for encontrada, ela será exibida.
4. Caso contrário, uma mensagem será exibida informando que nenhuma combinação foi encontrada.

## 🖥 Exemplo de Uso

```python
from itertools import combinations

def encontrar_combinacao(numeros, meta):
    for r in range(1, len(numeros) + 1):  # Testa combinações de diferentes tamanhos
        for combinacao in combinations(numeros, r):
            if sum(combinacao) == meta:
                return f"Combinação encontrada: {combinacao}"
    return "Combinação não encontrada"

# Exemplo
numeros = [2, 4, 6, 8, 10]
meta = 14
resultado = encontrar_combinacao(numeros, meta)
print(resultado)
